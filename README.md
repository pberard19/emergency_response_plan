# Emergency Response Plan

In the spirit of "buy a plunger before you need a plunger" this repo hopes to provide teams with an emergency response plan before they need one. This will not fit every use case, but it should provide a skeleton to adapt to general needs. This is intended for software teams, not other emergency response systems (EMT, fire, safety, etc) even though there may be overlap. This template was inspired by the triaging methodology of EMTs.

Emergency Response Plans are not an exhaustive solution to incident response. Other important parts of incident response include:
	- On call responsibility definition
	- Monitoring and observability of software systems
	- Engineering for disaster recovery and high availability (if appropriate)
	- Proper training on tools and technologies

## How to use this plan

1. Copy the template
2. Customize it to your needs (see Considerations below)
3. Share it with the team. The plan is useless if people do not read it.
4. Test it in a live/fake scenario
5. Compare the actual response with the plan. Update the plan and try again. (see Musings below)

## Considerations

- The plan is only useful if people are aware of it. The plan should be written for those who will use it.
- The plan should be digestible and actionable. No one will read it if it is too long.
- Do not detail out every possible scenario in the plan. If your problems and solutions are well defined, then they are not emergencies - they are business as usual. Create runbooks and a normal support flow instead.
- This template uses informal language. This is not to undercut the importance of the emergency but to make the content more consumable.
- Have multiple methods to do things. If there is ever a large-scale outage it is possible that your monitoring and alerting tools will be down. Having other means of interacting with your system will give you options. If your Slack or Discord or [primary communication channel] is down, does your team know how to connect another way?
- Be aware of the risk of false positives and false negatives. Be clear about your observations versus hypothesis. Understand what a [gettier case](https://en.wikipedia.org/wiki/Gettier_problem) is as these are some of the most useful lessons during post mortems.
- Be aware of bias for repeat issues. If something has broken one way (e.g. database got full and broke things), check other similar projects (e.g. that use the same type of database). 
- Remember that the team is human. People need breaks, coffee, food, and eventually sleep.

## Musings

"No plan survives first contact with the enemy."

Unless you have years of experience handling critical situations you will likely make mistakes when handling an emergency. Even with experience, human error is inevitable. When making your plan, it is easy to optimize for time to recovery objectives. This isn't necessarily wrong, but don't forget to include failsafes and sanity checks to minimize human error along the way. It is better to only deal with a single emergency at a time, rather than accidentally causing a second in an attempt to fix the first.

Some engineers are not used to the sudden chaos of a production outage. They are immediately overwhelmed by the amount of data they must sift through, the number of incoming pings, and the sudden (and often angry) pressure coming from leadership. No plan is going to adequately prepare you mentally for this challenge. Mental grit comes with practice and experience, in the meantime:

Don't panic. Breathe. Take notes.

"The opposite of fear is curiosity"

How can you keep panic and fear at bay when customers are angry and the damages seem to be escalating? Stay curious; be a scientist. Write down a hypothesis of what is broken, some methodologies to gather data to prove/disprove the hypothesis, and then go collect that data. Try to use the mindset "Huh, I wonder why that is" instead of "Oh no, everything is broken".
