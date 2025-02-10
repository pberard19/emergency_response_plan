# <SYSTEM NAME> Emergency Response Plan

This document outlines how to respond to production incidents for the <SYSTEM NAME> system

# Receive the Call

Outline the methods by which the team can be notified of an emergency. Ensure that all responding team members have access to these channels. Ensure that the appropriate audiences can raise issues should they arise. Effort invested in monitoring and alerting will make this easier.

Examples:
- An automated alert triggers a pager notification (best)
- A support contact reaches out to a team member
- A user complains in a forum that something isn't working

## Assess the Situation

Outline the process to confirm the issue. Sometimes a single report is enough, other times multiple stakeholders must confirm if there is indeed a production issue. Effort invested in monitoring and alerting will make this easier.

Examples:
- Check automated monitoring dashboards for service health (best)
- Team member manually checks an integration flow

## Communication

Outline how you will spread the word. Set expectations with your team and stakeholders in advance. Ensure that team members are able to send messages to the avenues of communication.

Determine:
- Who gets notified
- Who will send the message
- What level of information you will tell them
- Through which means you will tell them
- How often you give updates

Examples:
- Team reroutes traffic to a maintenance page and will notify a general channel every 15 minutes with technical status updates
- Team will send out an email every hour with general service status
- The loudest team member will yell across the room when the problem is fixed

## Triage and Fix the Issue

When EMTs are assessing a patient they often use the ABCs: Airway, Breathing, Circulation. These are necessary to keep the patient alive. Similarly, when assessing your application you must check the services you assume to be working for the application to function.

### Strategy

Outline a general strategy to determine what the problem is; the level of detail depends on your system. This can include a checklist to confirm different parts of the system were checked. Engineers should have multiple ways to access and check each part of the system. Engineers should also have contacts for any other teams they may need help from.

Take notes where everyone can see them. At a minimum include screenshots, timestamps, and short descriptions.

Example triage list:

- Foundational components
	- Database
	- Network
	- Servers
	- Identity
	- 3rd party integrations
	- Security threats
- Major application components
	- Which part of the application isn't working?
	- Have there been any recent changes or deployments to your system?
	- Have there been any recent changes or deployments to systems you rely on?
	- Have there been any recent changes to the data?
	- Have there been any recent changes in traffic?
- Integration points
	- There are 3 subsystems - A, B, and C
	- Check that the integration between each is working as expected
		- A <-> B
		- B <-> C
		- A <-> C

### Roles

If your team is large enough, you can create different roles. Sometimes there might be dedicated teams for each role. For long duration incidents there might be handover to another team member.

Some examples:
- Incident Leader - In charge of coordinating the response
- Communications Handler - In charge of sending out updates
- Lead Investigator - In charge of finding and fixing the issue
- Provisions Gatherer - In charge of getting caffeine and sugar into the bloodstreams of the other team members.

### What to do when you are out of ideas

In the best case scenario your alerting will tell you exactly what failed which should inform how to fix the problem. In reality, you may exhaust your easy to check options and be left wondering what else might not be working. In this case, practice the following:
- Follow the scientific method
	- Form and testing hypothesis. Objectively record the results. Through these means you can narrow down the possibilities of what can be failing.
- Ask for help
	- There is no shame in asking for help. For some teams this might be required as not everyone is meant to have access to every system.

## Blameless Post-mortem

Post-mortems are vital to understand what went wrong and how to prevent it from happening in the future.

Blameless post-mortems are vital for maintaining team psychological safety. A culture of blame will kill innovation because no one will take risks for fear of breaking anything. Willfull negligence aside, a culture that values learning will prioritize fixing system flaws and creating an environment where team members can fail safely.
