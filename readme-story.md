
At one day I've noticed that my editor usage skill is not satisfying me anymore.
I've watched how skilled vim users are working and were really impressed. For
selecting a block of text they didn't need mouse, they just press several
keyboard keys like "blabla" and (magic) block was selected, moved, uncommented
and half of current task was complete.

I used mouse and with mouse such microactions tooks significally more time and
I did a lot of mistyping often after mouse usage because my arms had wrong
position over keyboard (I could type without looking at keyboard easily, but it
is hard to move arms at proper place without a glance after mouse usage because
mouse could have different position on a table). At this time I've used sublime
for about 2 years and had only "Autocompletion" and "OpenPath" plugins written
and several plugins installed (like "Terminal").

So I decided to improve my code writing skill. At first, I tried to use vimium
packge more extensevely (before I've used it only if I need to find character in
line with multicursors). But personally I don't like conception of vim modes.

I mean there is 3 modifiers (somebody maps to 4 or even 5 modifiers) that gives
6 combinations for each shortcut (excluding plain "shift+"). And there is about
50 keyboard keys that can be pressed without changing hands position. It is 300
different keys together that can be issued without sequences in one mode. I
think this is enough for all actions that occurs enough often. For other actions
there are sequenced hotkeys (e.g. "ctrl+u, ctrl+a"). And I can use all this this
stuff without editor state hidden under bunch of pixels on display.

So after a while I realized that I don't use vimium anymore because I was not
used to deal with context automatically and (more important) I did't want to get
used to it. By this time I started to use keyboard arrows, page up/down and
home/end keys with ctrl modifiers intensevly.

Soon I've realized that I still have old problem: inproper hands position,
because navigation and typing always comes together when writing code. I
remapped arrows inside keyboard (alt+ijkl) and after period of adaptation felt
great relief because mistyping was finished and I felt myself more confidant and
comform.

Soon I hit another problem: I didn't had proper commands to tell sublime what I
want. I saw that some tasks that I do often could be easely algoritmized so I
started to write a plugin that helps to navigate over code. I was mistaken about
"tasks could be easely algoritmized". I tooks a lot of time and
plugin has been deprected by me in a week after I started to use it (yeap, hello
"sublime-paragraph").

By the time when "sublime-paragraph" was deprectated I saw even more actions
that coulbe be "easily algoritmized". And I started to implement stuff (that
were required to be implemented) without any plan. I didn't intend to do much of
such work I just fixed issues as soon as it appeared. And I primarily though
that plugins is something that is not hard to write and to debug because most of
plugins I've seen consisted of several dozens lines of code and were really
simple. There were my two biggest mistakes.

I should had plan and I should do all stuff with tests. And I should
made some kind of testing framework first. By the time I started to had
dependencies between plugins, bugfixing became really hard task (e.g. one bug
was fixed, but new bugs introduced and even more old bugs reopened) and internal
interfaces became bloated at some point. That is especially refers to
"sublime-expression", "sublime-statement" and "sublime-method" packages. Even
complete rewriting of some parts didn't help (just old bugs disappears but new
unexpected were inroducing; but likely without reopening old bugs; that was a
progress).

I don't know how I was successed to keep motivation to complete everything to
some (still buggy) point. Probably that I didn't count how much time and work
were already spended. And how many plugins were actually written. By the end
of developing my todo list hits point 300 and were still growing. In there I did
feature lock because I realized that it is more like endless meditation than
software development.

Much troubles were introduced because I didn't code python before and I didn't
imagine how some of it language constructions works. Fastinated by the "zen of
python" I hit all mistakes that I could. For now I personally think that "zen of
python" is lying and it is would be better if I not heard about it before I
started to code python.

E.g. I checked "100 == true # is false" in command line and hit "1 == true # is
unexpectengly true" bug that was really hard to debug. I just relied to
"Explicit is better than implicit" line from "Zen of python"; yeap, I explicitly
compared number with boolean (to overload method interface) without expecting
any implicit suggestions from python side; yeap, from all numbers only "1 ==
true # is true"; yeap, it is explicit that is implicit why it is like that;
yeap, likely I'm another stupid developer that should rtfm before using product
(despite size and readability of fm). But I were really disappointed because
python have beautifull philosophy and such contradictions were my another
motivation killers (also "self" in arguments took its part in it).

At some point of todo list (probably, more than 200) some other sublime users
started to ask me to share plugins with them. I initially intended to release
all plugins as open source, but at this point I took thought about release. And
what I saw didn't rejoiced me much. Because I've seen that I can't just threw
out commits to github and say: "Hey! Now you can use almost hundred plugins! You
just need to git clone to you plugins folder and that's it!".

Actually I could but I've seen so many software without proper documentation
(hello, half of ruby gems) and dig so much source code (e.g. in order to know
which value should I specify in "options" variable to achieve result) because of
documentation absention so I think that it is better not to release plugin than
release it with poor docs. I think the instructions to software are essential
(if software don't have ui), otherwise people will be disappointed and unhappy
and will send improper bug reports.

So I've seen that if I want people to be able to use plugins written I really
need to explain how to use this plugins and why some use cases are so shitty
that without documentation and a bit training it is not able to use it all. And
the proper documentation it is still a lot of work.

But in the end I glad that I have all this plugins. And thanks for everybody
who supported this project.