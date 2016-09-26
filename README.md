# misc
Various scripts and small bits that I need to store somewhere public

# Nagios Check_Iostat
At work we needed to monitor the IO Usage of our file and backup servers. 
Since both our RHEL4 and SLES10 installations comes with iostat I wrote a small Nagios plugin that wraps around the iostat binary. 
It is written in perl and uses Regexp::Common and the new Nagios::Plugin modules (available at CPAN) - the plugin reports perfdata in a format easy to parse with NagiosGrapher which is our preferred graphing extension. 
As someone on the Nagios Mailing list pointed out this script only monitors *IO Wait*, and not so much the IO usage. So maybe it should be called *Check_IOWait*

## Warning
This was written back in 2007, its not exactly new any more and im not sure Nagios even supports this plugin/checker format any longer.