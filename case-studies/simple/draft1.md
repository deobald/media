
# Case Study: Simple.org

Simple.org is a story about scale. On the one hand, the tagline "the fast, free app for clinicians to manage their patients with high blood pressure" describes a small mobile app with a singular purpose. On the other hand, Simple's mission is to save the millions of lives currently lost every year to heart attack and stroke. That's a mission which implies huge networks and thousands of moving parts. Can one little app save millions of lives? Certainly not on its own.

## The Problem

When _Resolve to Save Lives_ approached nilenso in May of 2018, the problem they had in hand was seemingly straight-forward: Build an MVP (Minimum Viable Product) of the Simple app and start showing it to users. But even as we claim "build an MVP" to be the problem statement we start to see the different scales at which this project operates. Yes, it's true that the initial task could be summed up as "build an MVP" but from _Resolve's_ perspective, the initial-initial task was actually "find a consulting company in India to build an MVP." Although "Simple" was a front-runner, the product didn't even have a name yet.

Every paid consultant has gone through the "Five Whys" exercise. The exercise is easy: ask "why?" of the problem at hand, then ask "why?" of the answer you uncover. Repeat five times. This exercise often makes inexperienced consultants come across like curious, but incredibly annoying, three-year-olds. When consulting with an organization like _Resolve_, the exercise isn't actually necessary. Or, at least, it's not obviously necessary.

The first meeting at the nilenso office was with Daniel Burka, Director of Product and Design at _Resolve._ The most common appraisal Daniel had among nilenso staff who hadn't met him yet was "the guy who designed the Firefox logo." For those who had started careers early enough to witness the early days of the Firefox web browser, this was no specious laurel. Firefox represented far more than the buzzwords we associate with it today: Open Source, Free Software, a World Wide Web based on Open Standards. Back in 2003, Firefox represented the democratization of the web in a David v. Goliath fight against Microsoft's stagnant and under-performing Internet Explorer, universally hated by software developers the world over. Firefox sat in the intersection of two communities, two ideas. On the left was _Free Software._ On the right was _Design_ With a Capital D. Good Design meant that a product like Firefox had to be approached with Design Thinking. It had to have a brand. It had to be fun. It had to be so much better than everything else you would be a fool not to use it. Firefox was all these things. It was also a Javascript debugger, a CSS reverse-engineering tool, and the doorway millions of developers stepped through to create the web and the internet we all rely on today. The significance of such a tool, and such a brand, is not to be understated. So come, meet Daniel, the guy who designed the Firefox logo.

No one from nilenso remembers a conversation about the Firefox logo but everyone who attended those early meetings remembers that the "why" of the project was very much understood. As far as _Resolve's_ goals were concerned, the "Five Whys" exercise would hardly be necessary. Why was _Resolve_ talking to nilenso? We heard your team was very good and we want to validate that by building an MVP. Why an MVP? We need to build real software, get it in front of our first users in Punjab, and start collecting feedback. Why build this software? Millions of preventable deaths happen worldwide every year due to heart attack and stroke. Many of those deaths aren't only preventable but they are _easily_ preventable. Some countries have this right, some don't. We want to build the tool that will help everyone on the planet prevent these deaths. Why hypertension? What's so special about heart attack and stroke? There are hundreds of possible candidates for attention at this scale, but hypertension is at the top of a lot of lists: It causes a massive number of deaths. It is easy to prevent with simple protocols and affordable medicines. It is well understood --- we aren't waiting for a miracle cure or scientific breakthrough; we just need to help nurses and doctors support their patients.

The reasoning was sound. The project made sense. _Resolve_ and nilenso had barely begun discussions and the team was already excited to get to work. But a project as exciting as Simple permits further reflection. It was an opportunity for nilenso to turn the "Five Whys" on itself.

---

Deepa Venkatraman and Steven Deobald, who paired [^pairing] on project management for Simple, found out early in their working relationship that they shared a common friend in Avishek Sengupta --- affectionately known as "Mojo" to them both. 

This triangle of working relationships was almost perfectly symmetrical. Mojo and Deepa built a computer vision path-tracking robot together for a college project in TODO:year and Deepa and Steven began working together in 2016. In 2006, Steven and Mojo were pairing on some legacy Java code in a tiny office in downtown Vancouver.

Mojo turned to Steven:

"All we have to decide is what to do with the time that is given us."

Steven answered with a blank stare.

"Tolkien." Mojo offered. "Fellowship of the Ring? I just re-read the books. That's sort of... the highest problem statement philosophically possible, isn't it?"

It was common to bump up against such peculiar insights when pairing with Mojo. The Java code in front of him was rarely the most intriguing thing on Mojo's mind during any given workday. At the time, it didn't feel as though this particular insight was going to define the operation of an entire company.

Over a decade later, nilenso was bootstrapped, profitable, and settling in for an identity crisis. An employee-owned worker co-operative has the roles and responsibilities one expects from any corporation: profit centres, administration, executive functions, purchasing. Those roles are not necessarily mapped one-role-for-one-person as they are in large, traditional organizations. [^reinventing-organizations] But there is one role everyone shares to some degree: founder. Whether someone has been a part of nilenso for ten years or ten days, that someone is beginning something _today._ And that thing, whatever it is, is the foundation for _tomorrow._ That means that every member gets to participate in answering the company's existential questions, for better or for worse.

Why does nilenso exist? **To make money so everyone can pay down their mortgages, obviously. But also to make software.** Why make software? **Because we are good at it and because it's fun.** Why is it fun? **Because it is satisfying to solve problems.** Why is it satisfying to solve problems? **Because, if we care about it, there is meaning in the problem --- and meaning in its solution.**

Why is there meaning in a problem? Why do you care about it?

Ay, there's the rub.

To ask such questions is to ask a fundamental question of our own existence. Why bother getting up in the morning? Why put on pants? Why am I writing this _particular_ line of JavaScript today? What is the meaning of life?

What exactly is it that makes a task, a project, a job worthwhile? And how do we reconcile the gap between the work we find meaningful with the work that generates revenue? No one's mortgage is paid down in the currency of goodwill.

In the early days with Simple, finding meaning in the problem was not difficult because it was nilenso's first project to fully reconcile this gap. Simple is useful and fun, beautiful and free, well-funded and stable. Simple changes lives for the better. Like Firefox.

But this question of purpose doesn't simply vanish when a potential solution is offered. As we will see, the question itself grows and changes as new answers emerge. As Simple grew, nilenso had a front row seat to this growth and change.

> "All we have to decide is what to do with the time that is given us," said Gandalf. "There are other forces at work in this world..."


## The Solution

### Kickoff

May tipped over into June and the Bangalore spring melted into summer as our friends poured from one month into the next. A team was assembled. _Obvious,_ another Bangalore consultancy, was responsible for Simple's mobile app. The central service was built by nilenso, where Srihari Sriraman and Govind Krishna Joshi staffed themselves on the project as developers and Deepa and Steven similarly self-staffed as project managers. Project management was across teams, working between the nilenso team who would build the central service, the team from _Resolve,_ and the team from _Obvious._ 

As Bangalore melted into puddle marking the very centre of South India, a web of teams and roles took shape in the centre of that puddle. Daily stand-up meetings marked the end of every day (India time) with the teams from nilenso and Obvious sharing their progress with Daniel and _Resolve's_ Director of Engineering, Tim Cheadle. The team was small, distributed, and fast. Communication between designers, mobile app developers, and service developers was immediately productive and the two teams in Bangalore shared an office space as regularly as they could. From one day to the next, entire designs would be considered, attempted, tested, thrown out, and redone. Discussions were open and earnest about exactly what the collective team was trying to build. Even though the MVP was built to validate ideas, it was not an experiment --- with clear goals there were clear rights and wrongs in implementation. With just a handful of weeks available, the team desperately wanted to build The Right Thing. [^hackers]

The Right Thing, of course, is a moving target. What is right in June 2018 certainly won't be right in April of 2019 and the exercise was one of brainstorming, identifying risks, narrowing scope, and executing... all as quickly as possible. For Simple, the twin tasks of brainstorming and identifying risks melded into one long, iterative activity of imagination and research.

Some risks to the project's success were obvious. The initial deployments were to go to nurses in remote parts of rural Punjab, with the intention of distributing the app to every state in India --- and even more remote locations --- if it proved a success. The team needed imagery to create scenarios for users. How remote is "remote", really? India's vast landscape is dotted with cellular towers and dozens of new towers go up every day. What image could possibly exemplify the extremes the Simple software would be subjected to?

Images of the Spiti Valley resemble the sort of ultra-high-resolution photographs one might find in the foyer of Goldman Sachs. Spiti Valley is extreme. High in the Himalayas, Spiti can claim not only the title of mountain valley but also that of a desert. It is breathtakingly beautiful --- and definitely remote. But it is not uninhabited. Those same foyer photos almost always include monasteries, villages, bridges, and flags. Whenever a design choice required thinking about a remote location where nurses might lack internet access for days, the team would recall the Spiti Valley vignette: a desert valley 13,000 feet above sea level with an unmistakable human presence.

With such imagery at hand, the team unanimously agreed the software must be designed "offline first." [^govind-offline-first] Other decisions were less obvious. The first MVP deployment would happen across five clinics in rural Punjab. But would the Punjabi nurses in these clinics insist on a user interface entirely in Punjabi? Would Hindi suffice? Would some nurses be more accustomed to an English keyboard, even if their phones were set to a Punjabi locale? The only way to really get answers to such questions was to fly to Punjab and ask the nurses yourself. The team built the first MVP with both Punjabi and English support.

### Bathinda



## Outcomes

[^pairing]: https://martinfowler.com/articles/on-pair-programming.html#KnowledgeSharing
[^reinventing-organizations]: https://www.reinventingorganizations.com
[^hackers]: https://en.wikipedia.org/wiki/Hackers:_Heroes_of_the_Computer_Revolution
[^govind-offline-first]: https://medium.com/simple-dot-org/offline-first-apps-are-appropriate-for-many-clinical-environments-cddf5a73bb61











