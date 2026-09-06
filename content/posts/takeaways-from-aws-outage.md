+++
title = "My Takeaways from the AWS Outage"
date = "2025-10-27T23:23:56+03:00"
author = ""
authorTwitter = "" #do not include @
cover = ""
tags = ["", ""]
keywords = ["", ""]
description = ""
showFullContent = false
readingTime = false
hideComments = false
color = "" #color from the theme settings
+++


It’s always DNS.
That’s the joke.

But this time, it wasn’t funny because half of the internet went dark, and the punchline cost billions.

When AWS went down, it wasn’t a “server crash.” It was automation turning against itself.

Two systems;
one to plan DNS changes, another to execute them. Started racing.

The result:
Empty DNS records.
No IPs, no routing, no service discovery.
Essentially, the cloud forgot where it lived.

And what that reminds me is simple:
You can’t automate responsibility.
You can script deployments, containerise workloads, set health checks, and monitor uptime 24/7
but you still need to think.
Automation doesn’t understand context. Humans do.

Get Aslihan Akbiyik’s stories in your inbox
Join Medium for free to get updates from this writer.

Enter your email
Subscribe

Remember me for faster sign in

When I read the post-mortem, the problem wasn’t just the bug, it was the trust.
We trusted automation to catch its own fall.
We assumed redundancy meant immunity.
But when both redundant systems share the same logic flaw, they fail together.

It made me ask some questions:
- What if the automation collides with itself?
- What if the safety net is wired to the same node it’s supposed to protect?
- What if redundancy isn’t really redundant?

It might sound like a cliché, but
Quis custodiet ipsos custodes?
sums it up perfectly.

Every incident like this feels like a mirror for infrastructure people.
We spend months building resilience, then forget to design for human curiosity.
We need to question the mechanics, not just the metrics.

Do we test what happens when DNS returns empty?
Do we simulate failure of automation layers?
Do we document what depends on what — and how it dies?

Because when the automation layer fails silently, your entire stack becomes a black box.

Lessons I Drew From It
Keep questioning your assumptions.
Keep doubting your certainty.
Keep asking why something that shouldn’t fail, still can.

Because failure is rarely a lack of redundancy, in fact it’s a lack of imagination.