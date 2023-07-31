The error was :
test.S:15855: Error: illegal operands `and s7,ra,z4'
test.S:25584: Error: illegal operands `andi s5,t1,s0'

Z4 is a special purpose register and andi needs immediate value

The fix is remove the "and s7,ra,z4" line and make the 25583 line 'andi' as 'and'