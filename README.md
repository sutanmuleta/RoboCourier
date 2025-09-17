# RoboCourier

A simple reinforcement learning environment for training agents to complete delivery tasks on a grid world.  

The agent controls a small robot courier that must:

- Navigate to a pickup location
- Collect a package
- Deliver it to the dropoff point
- Recharge at a charger if the battery runs low
---

## Observation Space
- Shape: `(10,)`
- Normalized values in `[0, 1]`
- Encodes:
  - Robot position (x, y)
  - Pickup location (x, y)
  - Dropoff location (x, y)
  - Charger location (x, y)
  - Battery fraction

## Action Space
- `Discrete(4)`
  - `0` = Move Up
  - `1` = Move Down
  - `2` = Move Left
  - `3` = Move Right

---
## Rewards
- `-0.1` per step (time cost)
- `+10` for successful delivery
- `-5` if battery runs out before recharging
---
## Installation
Install from the Prime Hub:

```bash
prime env install sutan/robocourier
