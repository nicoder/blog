# how to edit Vim macros

Usually when I record a Vim macro and do something wrong I will just :
 * stop recording (with `q`)
 * undo my changes (one or more `u`)
 * record the macro over (`qa` + changes / movements + `q`)

But there are ways to change a recorded macro if it does not do exactly what
you want.

The simplest way is if you only have forgotten to do something at the end of
the macro. For example it happened to me recently that I recorded the change I
wanted to make but not the `n` at the end to go to the next occurrence of the
repeated thing I wanted to change.

In that case, if you recorded the macro in the `a` register you can type `qA`
to record the end of the macro.

If you want to change the macro elsewhere than at the end, here is a way to do
it (assuming again that you recorded the macro in the `a` register with `qa`):
 * copy the macro in the file with `"ap`
 * make the desired change to the macro 'code'
 * yank the macro description back into register `a` (for example by visually
 selecting it with `v` plus a movement, and then `"ax`)

The description of the macro can look a bit strange if you are not used to
looking at things like that, but it is just literally what was typed during the
recording.
