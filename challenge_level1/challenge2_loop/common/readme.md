
The error was continuous loop.

the following was the fix in the code. The code was fixed by adding a limit to the no. of loops taking place by decrementing the already given variable t5

loop:
    lw t1, (t0)
  lw t2, 4(t0)
  lw t3, 8(t0)
  add t4, t1, t2
  addi t0, t0, 12
  addi t5, t5, -1
  beqz t5, test_end
  beq t3, t4, loop
  j fail
