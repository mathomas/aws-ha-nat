Amazon has a pretty nice write-up about how to create an HA NAT setup in multiple subnets/AZs.  They also offer a CloudFormation template that works pretty well.
See here:  http://aws.amazon.com/articles/6079781443936876

However, the monitor script code that is downloaded  with the template is out of date and is therefore buggy.  Since it's a monitoring script installed on two instances that control each other, much silliness can ensue when there are bugs.  In my case, the NATs would keep shutting each other down and restarting each other.  Fun to debug!

I needed to fix this issue.  Since Amazon controls both code resources, I had little choice but to virtually-clone them into this repo to fix them for future reference in other projects.
