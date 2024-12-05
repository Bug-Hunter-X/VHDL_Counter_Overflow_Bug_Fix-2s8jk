# VHDL Counter Overflow Bug

This repository demonstrates a common error in VHDL code: an integer counter that overflows without proper handling. The `counter` entity increments a count value on each clock edge. However, it lacks a mechanism to prevent the counter from exceeding its defined range (0 to 15). This can result in unexpected behavior or simulation errors.

The solution demonstrates how to implement a safe counter by adding overflow checks.

## Bug

The provided VHDL code shows a simple counter.  However, when the `internal_count` reaches 15 and increments again, it wraps around to an unexpected value, producing undefined behavior.