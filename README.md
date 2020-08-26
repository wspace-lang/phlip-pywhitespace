# pywhitespace

by Phillip Bradbury, licensed under [GPLv2](COPYING)

## Whitespace mailing list

Posted [3 Aug 2004 12:27:27 BST](https://web.archive.org/web/20141011193201/http://compsoc.dur.ac.uk/archives/whitespace/2004-August/000048.html)

I just saw your site and I think whitespace is quite clever ;)

Unfortunately I don't have enough room on my computer for GHC, so I
ported the code to Python.

[http://www.cs.newcastle.edu.au/~c3018900/pywhitespace.tar.bz2](https://web.archive.org/web/20061209092911/http://www.cs.newcastle.edu.au/~c3018900/pywhitespace.tar.bz2)

this has everything from the 0.3 Haskell source, minus the haskell, plus
some python code and two more examples (chr.ws and ord.ws, for
ASCII->Char and vice versa)

the main.py has a #! line, so if you're in linux you can just go

    chmod o+x main.py
    ./main.py program.ws

on Windows you have to go

    C:\Python23\python main.py program.ws

or just

    python main.py program.ws

if python is in your path.

I'm not sure if I implemented Ref correctly - the tutorial doesn't say
whether it's 0-based or 1-based, and I don't know whether Haskell is,
either. I coded it as if it was 1-based, ie Ref 1 is the same as Dup.
Slide should be fine however.

It's got quite nice error reporting (for invalid commands such as
[LF][LF][SP], and things like pop from an empty stack etc) and the code
is quite simple. It also has the ability to (by uncommenting a couple of
lines of code) to dump the code to screen readably (uncomment
Input.py:57) or to run a "trace" through the code (uncomment second-last
line of Program.py)

It's a little slow though - it takes about 20-25 seconds to run hanoi.ws
with 10 discs on my old P150 (I don't have a faster computer to test it
on, unfortunately...)

But anyways, it was fun to make!

Feel free to host this on your site (please credit me, Phillip Bradbury)

Comments are very welcome

=====

Phlip

Christmas comes but once per 31.6887nHz cycle

## Whitespace mailing list, update

Posted [10 Dec 2007 10:07:39 GMT](https://web.archive.org/web/20161009051032/http://compsoc.dur.ac.uk/archives/whitespace/2007-December/000065.html)

Hey, if you're reading through the archive history, and updating the
website, I should probably mention that the link to my python ws
interpreter is broken... I've reuploaded it at
[http://www.mrphlip.com/pywhitespace.tar.bz2](https://www.mrphlip.com/pywhitespace.tar.bz2)

It's changed a little since my post back in August '04... in particular,
I have a non-pathetic computer now, so I could run the Haskell version
and compare... turns out, I implemented Ref wrong (Ref 0 should behave
the same as Dup, not Ref 1), and that's fixed in the above link.

Enjoy!

--

Phlip
