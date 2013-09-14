# f and t

Two motion commands I enjoy a lot in Vim's normal mode are `f` and `t`.

For example `fx` will move the cursor to the next `x` on the line.
The opposite command is `Fx`, it will move the cursor to the previous `x` on
the line.

(I think of `f` as 'find' and of `t` as 'till').

Similarly `tx` will move the cursor to the character just before the next `x`
on the line. And `Tx` to the character just after the previous `x`.

These commands are useful to move around, and also when used in conjunction
with commands such as the change (`c`) or delete (`d`) commands.

For example if my cursor is at the begining of a variable called
`smallPlasticOnion`.
I can change the first 'word' of the variable with `ctPmedium` and the variable
becomes `mediumPlasticOnion`.

`;` will repeat the motion command in the same direction, `,` in the opposite
direction.
