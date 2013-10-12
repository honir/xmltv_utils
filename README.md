xmltv_utils
===========

Miscellaneous tools for use with XMLTV


tv_count
--------

Count (and print) the number of channels and programmes in an XMLTV file


tv_merge
--------

I only found one program which will intelligently merge two XMLTV files (rather than just concatenate them). I guess most people just grab the *whole* schedule every day.  8)  That seems wasteful - much better to just re-get the next 2-3 days and add a new day on at the end, rather than getting the whole 14 days every time.

The only script I found was xmltvmerger.py but that has a couple of flaws, the biggest one being it won't *add* new programmes which aren't in the primary file. IIRC it also has a bug in the handling of overlaps (e.g. where 2 programmes are now replaced by 1) and doesn't delete the old programme.

So I wrote tv_merge.

This works with multiple channels, inserts any new programmes and deletes any overlapping programmes.

To use it the input files must be pre-sorted into datetime within channel order by using the "--by-channel" option to tv_sort
  e.g. tv_sort --by-channel --output FILE  FILE


