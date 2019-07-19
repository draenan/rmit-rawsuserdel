# rawsuserdel - Delete System Users and Database Tables from RAWS

Further evidence that I used to write Perl.  Again I don't claim to have ever
written Perl well.

RAWS was a system that was used to automatically set up a user's web space and
accompanying Wordpress blog on a web server.  It was terrible, and suffered
from many issues; multiple deployments of obsolete Wordpress versions that were
never updated; open to the Internet for ease of drive-by hacking attempts; hard
to support when your support team weren't Web Devs; never, ever cleaned up, so
long-gone users and their abandoned sites hung around; built (at least the
second iteration) on a Solaris server using per-user ZFS file systems with
snapshots and the like, with an apparent misunderstanding of the differences
between "quota" and "refquota" when it came to creating these file systems;
and it suffered from scope creep - one day Corporate content started appearing
on it.  I was not pleased.

The Solaris build happened not long after I joined the Unix Team, but it was
a while before I ended up having to support it and wondering why we weren't
at the very least cleaning up old user accounts.  This Perl script was born out
of me trying to come up with a "simple" way to do all the necessary tasks
required for cleaning old accounts that could also be used by my colleagues.

The RAWS account registration script was shut down in 2012 while people decided
to begin the process of deciding how they would decide what to eventually do
with it, maybe.  I didn't get to drive a metaphorical stake through its black
heart until 2018.  I'm not bitter.  *Much*.

