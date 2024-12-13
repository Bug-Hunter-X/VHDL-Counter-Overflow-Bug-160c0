# VHDL Counter Overflow Bug

This repository demonstrates a common VHDL coding error related to counter overflow. The `buggy_counter.vhdl` file contains a counter that does not handle the case when the counter reaches its maximum value.  The `fixed_counter.vhdl` provides a corrected version.

## Problem

The original counter increments beyond its defined range (0 to 15), causing unexpected behavior or simulation errors.

## Solution

The corrected version uses a modulo operation to wrap the counter back to 0 when it reaches 15, preventing overflow.

## How to Reproduce

1. Synthesize and simulate both `buggy_counter.vhdl` and `fixed_counter.vhdl`.
2. Observe the output of the `count_out` signal in both simulations.  You will see that the buggy version exhibits incorrect values after 15.
