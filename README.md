# VHDL Counter Overflow Bug
This repository demonstrates a common bug in VHDL code: integer overflow in a counter.  The `buggy_counter.vhdl` file contains the buggy code, while `fixed_counter.vhdl` provides a corrected version.

## Bug Description
The original code implements a simple counter. However, it lacks a check to prevent the counter from overflowing past its defined range (0 to 15).  Once the counter reaches 15, the next increment will wrap around to 0, potentially causing unexpected behavior in a larger system.

## Solution
The corrected code in `fixed_counter.vhdl` adds a check to handle the overflow condition. When the counter reaches its maximum value, it remains at 15 instead of resetting.