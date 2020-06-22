# PHP-Useful-Scripts
Here we go with another post! 🤘

In the other day I noticed all IPs recorded from visitor on one of my apps were the same, with a very little variation each-other! Aha~ found a bug!

Well, not much! 🙄 After a quick Google search I figured out that those IPs were all from CloudFlare (the CDN provider my apps are behind)! So, CloudFlare replaces the commonly used $_SERVER['REMOTE_ADDR'] variable with their own IP.

Fair enough!

So, if you're reading this, the chances are you are facing a similar problem and are looking for a solution ... or perhaps you're just curious, which is fine too. 🤪

Here's a very simple way to get the (real) client IP address. Note that the sintax used here is PHP7+, which means for earlier versions you're gonna need to apply some chained ifs and elses.
