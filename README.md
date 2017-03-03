# git-find-file
Find a file through git history by searching back through the
history of the branch to find it.


As an example, let's pretend that you long ago deleted foo.jpg
from your branch. If you want to find it, use:

    $ git find-file foo.jpg

Filename glob patterns are accepted:

    $ git find-file *.jpg

You can also search from the beginning of time on the branch, until
your point on the branch, with "--first". I.e., to find the
first commit with the appearance of the file.

And, you can invert the search. Instead of looking for the presence
of a file, you an search for its absence with "--missing".

So, for example, to find the first commit that is missing the file:

    $ git find-file --first --missing foo.jpg
