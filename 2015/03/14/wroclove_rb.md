# My talk on Sonic Pi at Wroc_love.rb 2015

Today I gave my first conference talk. Funny, today is Pi Day (3.14), and the
talk was an introduction to [Sonic Pi](http://sonic-pi.net/). My goal was to try
and share my excitement about that piece of software. I hope some of the
participants will try playing with it and have fun or teach somebody programming
with its help.

The talk went incredibly well (from my perspective, that is). I feared that
people would not be able to read the code on the screens or that the sound
would be horrible, but it seemed to me that it went smoothly. I was even
surprised by the live code I produced. For example when introducing samples I
gradually arrived to something like this :

```ruby
live_loop :drums do
    sample :drum_bass_hard if one_in 2
    sample :drum_snare_hard if one_in 3
    sample :drum_cymbal_closed unless one_in 12
    sleep 0.25
end
```

and it sounded much better than when I practiced that at home. Of course you
experience things differently when you are practicing alone than when you are
facing a lot of people, but I did not expect it to feel so good.

I am not good at improvising talks, but I do not like having a script either,
so I practiced a lot with different versions of the talk, and that gave me a
good enough base to sort of improvise during the talk.

It was a lot of fun to watch the reactions of the audience during the live
coding.

I noticed after the fact that I forgot to mention cool things like `with_fx`,
but I do not mind that much because the goal was to get people excited about
Sonic Pi, not show them everything about it, and I heard nice reactions from
people afterwards.

I just put up the slides on
[the web](http://nicoder.github.io/20150314_wrocloverb_sonic_pi).
They are probably not very interesting on their own, if you missed the talk I
encourage you to watch one of Sam's talks instead, for example ["Our Shared Joy
of Programming" by Carin Meier and Sam
Aaron](https://www.youtube.com/watch?v=3_zW63dcZB0)

Thank you Sam for creating Sonic Pi and inspiring me to give this talk.

Thanks also to the organizers of the conference for their hard work making this
event happen and for accepting my talk proposal.

Edit: here is
[the video](https://www.youtube.com/watch?v=5cZfqXiivdA&list=PLoGBNJiQoqRAv7J_2_lZvl47_1Wg7bIPD&index=11).
