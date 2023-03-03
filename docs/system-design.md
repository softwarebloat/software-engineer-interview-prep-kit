## Intro

System Design interview questions are quite challenging.  
They are open ended questions with the objective to design an architecture for a software system.

The questions are usually very big scoped and vague and there is no certain pattern to follow.

The meaning of this kind of interviews is to evaluate the interviewee on how he/she analyzes a vague problem and how solves the problem step by step


## Advices

Don't rush and try to be organized and structured.  
Explore the problem and ask questions to clarify the use cases.  
Do some quick analysis and if needed try to do some estimation

If you are particularly strong in one area, try to direct the conversation towards that! (e.g.: DB choice)


Try to divide the process into __4 steps__:

1. Understand the problem and establish design scope
-  Propose high-level design and get buy-in
-  Design deep dive
-  Wrap up

#### Example Questions
To better understand the problem and gather requirements, we should ask some questions related to the problem we are facing.  

!!! question "Examples"
    - Which functionality are we designing?
    - Is it an MVP?

    - Who will use the system?
    - How will the system be used?
    - How many users do we expect to use the system?
    - Where are they located? Globally? Nationally?

    - Do we know how many reads per second?
    - How much data is queried per second?
    - How many {data/image/video/resource} are processed per second?

    - Should the design minimize the cost of Development?
    - Should the design minimize the cost of Maintenance? 
		
Back of the envelope estimation


#### Follow up Questions
Once you finished your design, the interviewer could ask some followup questions like:

!!! question ""
    - what if we want to add <this> functionality?
    - What will you improve?

Usually this doesn't mean that we should redesign our application but it's just a way to have more discussions about it, understand how you solve those challenges and your knowledge.  

!!! tip
    Generally speaking, you could improve an application by adding things like:
    
    - multi Availability Zones (to improve availability and redundacy)
    - [monitoring/observability](../glossary/#monitoring)
    - [CDNs](../glossary/#cdn)

## Topics
Be prepared to talk about things like __DB__ choice, __cache__, __async__ vs __sync__ processing, __REST__, __Load Balancers__, etc
Some of the most commong topics are pointed out in the [Glossary](../glossary)  

!!! question "Some Common Problems"
    - Design a URL Shortening service
    - Designe Instagram
    - Design Twitter
    - Design Youtube/Netflix
    - Design an API Rate Limiter
    - Design a messaging app

## Questions
At the end of the interview, you should have time to ask some question on topics you are interested in.  
Here's some examples of questions you could ask after a System Design interview:

!!! question ""
    - It’s the infra/software self-hosted or do you use some cloud provider, or both?
    - Do you have “on call”? How does it work?
    - How do you handle the sw fragmentation
    - Do you need to align with other squads? If yes, how do you do that?

## Resources

__Reads__:  

- [ByteByteGo Blog](https://blog.bytebytego.com/)
- [System Design Interview - An Insider's Guide](https://www.goodreads.com/hu/book/show/54109255-system-design-interview-an-insider-s-guide)
- [System Design Interview – An Insider's Guide: Volume 2](https://www.goodreads.com/book/show/60631342-system-design-interview-an-insider-s-guide)
- [Cloudflare Learning Center](https://www.cloudflare.com/it-it/learning/)
- [System Design Primer](https://github.com/donnemartin/system-design-primer)
- [Interviewing.io - A Senior Engineer's Guide to the System Design Interview](https://interviewing.io/guides/system-design-interview)

__YouTube Channels/Playlists__:  

- [System Design Interview](https://www.youtube.com/c/SystemDesignInterview/videos)
- [System Design by Gaurav Sen](https://www.youtube.com/playlist?list=PLMCXHnjXnTnvo6alSjVkgxV-VH6EPyvoX)
- [System Design by Narendra L](https://www.youtube.com/playlist?list=PLkQkbY7JNJuAhePp7E_WSpfFqjQp6RniV)
- [IBM Technology](https://www.youtube.com/c/IBMTechnology)
