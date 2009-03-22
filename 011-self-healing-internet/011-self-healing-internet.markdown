{{
categories:
  - web
}}

# Self-Healing Internet (2007/06/23)

I love the fact that the best source of answers to internet-related problems is the internet itself. If that seems like an obvious statement, just think about it a bit longer...can other things tell you how to fix themselves? Does you car or your microwave or your lawnmower or your dog allow you to find a solution internally and then apply that solution to effect a repair?

After setting up my new MacBook I was having a small problem with the blogging bundle for [TextMate](http://macromates.com/) -- for some reason I couldn't fetch posts from or add new posts to this blog, which uses [WordPress](http://wordpress.org/). I was getting this error: "XML-RPC server accepts POST requests only". I couldn't find the answer on the [TextMate blogging bundle](http://macromates.com/blog/2006/blogging-from-textmate/) page, but there were a few comments there from others with the same problem.

Next stop, Google. Put in "wordpress XML-RPC server accepts POST requests only" and I'm led (no surprises here) to this page: [Wordpress "XML-RPC server accepts POST requests only"](http://will.hughesfamily.net.au/20070513/wordpress-xml-rpc-server-accepts-post-requests-only/). Someone else with the same problem and the same webhost -- and a solution: add the following line to the top of the xmlrpc.php file (in the wordpress directory):

    $HTTP_RAW_POST_DATA = file_get_contents('php://input');

(Turns out, the problem is related to the version of PHP used on the webserver.)

So, that's done now.

What makes all this work is that people keep a record on the internet about what they do with the internet. Search the internet and I have a solution to my problem, which was about getting my stuff onto the internet. 

Using the internet has fixed my problem and allowed me to use the internet. It's self-healing.
