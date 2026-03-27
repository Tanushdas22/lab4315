# Lab 4 Part 1 Experiment Table

## Requirement Snapshot

- Keep acceleration fixed at `150 steps/sec/sec`.
- Keep deceleration fixed at `150 steps/sec/sec`.
- Sweep max speed from `200` to `500 steps/sec` in increments of `50`.
- For each speed, measure time for **one rotation**.

## Live Data Table


| Run | Max Speed (steps/sec) | Accel (steps/sec/sec) | Decel (steps/sec/sec) | Move Command (steps) | Dwell (ms) | Trial 1 (s) | Trial 2 (s) | Trial 3 (s) | Average (s) | Notes |
| --- | --------------------- | --------------------- | --------------------- | -------------------- | ---------- | ----------- | ----------- | ----------- | ----------- | ----- |
| 1   | 200                   | 150                   | 150                   | 2048                 | 0          | 11.40       | 11.12       | 11.34       |             |       |
| 2   | 250                   | 150                   | 150                   | 2048                 | 0          | 09.40       | 09.51       | 09.47       |             |       |
| 3   | 300                   | 150                   | 150                   | 2048                 | 0          | 07.71       | 07.82       | 07.76       |             |       |
| 4   | 350                   | 150                   | 150                   | 2048                 | 0          | 06.36       | 06.45       | 06.41       |             |       |
| 5   | 400                   | 150                   | 150                   | 2048                 | 0          | 06.42       | 06.44       | 06.47       |             |       |
| 6   | 450                   | 150                   | 150                   | 2048                 | 0          | 06.43       | 06.48       | 06.45       |             |       |
| 7   | 500                   | 150                   | 150                   | 2048                 | 0          | 06.52       | 06.40       | 06.43       |             |       |


## How To Run Each Measurement

1. Program FPGA and run app.
2. At CLI prompts, enter:
  - Current position: `0`
  - Speed: `<current test speed>`
  - Acceleration: `150`
  - Deceleration: `150`
  - Destination: `2048`
  - Dwell: `0`
  - Stop entering more positions: press `<ENTER>`
  - Start motion: type `g<ENTER>`
3. Measure time for exactly one move (`0 -> 2048`):
  - Start timer when motor starts rotating (or green LED turns on).
  - Stop timer when motor stops (or green LED turns off).
4. Record Trial 1/2/3 for that speed and compute average.
5. Before next speed, return to menu (`m`) and repeat with the next speed.

## Quick Interpretation Notes (for report)

- Expected trend: higher speed generally gives shorter rotation time.
- At high speeds, acceleration/deceleration limits can reduce effective average speed, so improvement may not be perfectly linear.
- If missed steps or instability appears at higher speeds, note that as approaching motor/driver slew-rate limits.

