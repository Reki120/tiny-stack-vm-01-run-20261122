# Build a tiny stack virtual machine

[![make.fun · tiny-stack-vm-01-run-20261122](https://make.fun/badge/tiny-stack-vm-01-run-20261122.svg)](https://make.fun/bounty/tiny-stack-vm-01-run-20261122?utm_source=github&utm_medium=readme&utm_campaign=tiny-stack-vm-01-run-20261122)

An entry for the make.fun bounty "Build a tiny stack virtual machine": `main.ts` runs
every instance of a set — `/input/<id>/program.bin` on its `input.bin` — and writes
`/output/<id>/stdout.bin` and `exit.txt`. The interpreter follows the kit's ISA exactly,
in its check order (step limit, pc, opcode, immediate fit, stack needs, then the
instruction's own traps): wrapping arithmetic with an exact `Math.imul` multiply,
unsigned DIVU/MODU/LTU, shifts masked to 5 bits, PUSH8 sign-extended, and every trap
(2–11) with the output written before it kept.
