---
layout: post
title:  "TDD and Code Coverage"
categories: code
author: groundh0g
---

I've always had a bad taste in my mouth for code coverage tools. It just feels like it encourages developers to write tests solely to trigger code paths in an effort to reach 100% coverage. Even if those are low-quality, do nothing tests.

I've seen the value on my current project, though. I'm taking the opposite stance now. When the coverage shows that a given path isn't executed, I reevaluate the need for that code. I tend to write very defensive code. My philosophy has always been, "If it can happen, the code should account for it."

Using a strongly-typed language like TypeScript makes a lot of that code unnecessary, though. If designed properly, the compiler will ensure that a parameter for your method isn't null, or empty, or undefined, or of the wrong type. 

ßIf a library you use catches exceptions and only returns valid values (some of which indicate failure), then trying to catch errors that will never occur is just adding more unreferenced code. There are other examples, but the basic idea is that I'm using code coverage to keep myself from writing dead code. 100% coverage would be ideal, but I don't want to satisfy a test without evaluating why it was failing in the first place.

Of course, if I were truly following TDD principles, I'd never write dead, defensive code paths in the first place. I've been coding for 30+ years, but I still have a lot of growing to do as a developer. That's part of what draws me to the craft. You're always learning.

![Joe's Signature]({{ "/assets/images/signature-joe.png" | relative_url }})
