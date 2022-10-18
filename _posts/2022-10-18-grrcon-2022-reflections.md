---
layout: post
title:  "GrrCon 2022 Reflections"
date:   2022-10-18 00:00:00 -0500
categories:	reflections security grrcon infosec conference leadership thoughts
---

# GrrCon 2022 Writeup

*These are my personal observations and thoughts about GrrCon 2022. Your mileage may vary. Flames go to /dev/null.*

GrrCon 2022 took place on October 13th and 14th at the Devos Place convention center. Between the two days I attended sixteen (16) different sessions and three (3) keynotes taking notes on fifteen (15) of the sessions. I believe that a keynote is meant to be ingested at full attention. 

1. I firmly believe in the mission of GrrCon and the belief in free speech absolutism outside of targeted harrassment. Being offended is a part of life that **you** need to be OK with. 
2. This is an affordable conference and it is in my hometown. I think next year I do want to upgrade to VIP to get access to some more resources. 
3. I didn't spend much time in the vendor area. The time I did spend did not result in much education. That and the vendors weren't as active or inviting as I was hoping for. 
	1. With that said I do appreciate the vendors!
	2. They **all suck equally** so keep that in mind.
5. There was a good sense of diversity this year. I'll note that in these ways: 
	1. There were SO MANY first timers this year. That surprised me. 
	2. More women, including presenters. 
	3. Several presenters made it a point to remind us that we need to get more diverse people and ideas into our conversations, teams, and organizations.
6. "How to Rob a Bank" was one of the more entertaining sessions and I do wish I took notes on that one. However it being 5pm on Day One I was _fried_. 
7. Ransomware was of course the largest topic of the conference. I learned some new stats but not really new information on prevention and containment. More on that later. 
8. A second theme that I saw was in regards to tooling and baselines. Meaning that we have a ton of tools that we can use to detect malicious activity but it is all worthless without having a baseline of _normal_ for us to refer to. 
	1. I don't believe I can point to a single organization who has this.
	2. I've been talking baselines since my early virtual desktop infrastructure (VDI) days of 2013/2014. That is more than eight years ago and I think the industry has gotten _worse_ at this. 
	3. To me this means that there is opportunity for a consulting firm to offer this as a service: 
		1. Implement a network device scanner to establish device baselines. 
		2. Deploy a standard syslog/SIEM with agents on the established baseline to collect a data baseline. 
		3. Sell this as a fixed fee project with a six-month timeline. Fixed-fee would likely be based on the size of the organization.
9. I really appreciated the "Social Engineer Your Career" session. Out of all the sessions this one focused on soft skills. We need more presenters talking about this. As hackers we already have an image problem and having appropriate soft skills will help with that. 
10. My company had no plan for this conference. There were three of us in attendance - one from our official security team and two from our overall managed solutions team - with no coordination. Considering we had at least five customers in attendance this should have been managed better. Especially considering that we'll send 5+ people to a conference halfway across the country at exorbitant cost. 
11. The Friday keynote by Alyssa Miller was excellent as expected. I follow her on Twitter and did not expect to see her at my local conference. Very happy that I was able to see it. 
12. Our internal support team should have been there and they should have gotten VIP or better tickets. 

OK so here is my one rant. We have a ton of presentations that give useful statistics, data, and experiences. However there is little in the way of practical "here is how we did X and how it worked or didn't work and why" type of content. The closest to this was a presentation on using Terraform to build out some basic cloud assets (note: this was not the presentation that I was hoping for). I think I want to build a talk around this. Something that any organization can take and work with. 

## Practical Methods to Prevent and Mitigate Malicious Activity

1. No more local administrator. 
2. Audit Domain Administrator and Global Administrators. These must be dedicated accounts. 
3. Turn on and use host-based firewalls. Block east-west traffic by default.
4. Log everything practical: 
	1. Workstation and Server event logs
	2. Firewall logs
	3. DNS queries
5. No shared service or user accounts. Each service gets its own! 
	1. Assign minimal priveleges. Never just give it Domain Admin. 
6. All those shared data folders? Remove all user access accept for a specific stakeholder. 
	1. Add in appropriate groups for Read, Read/Write, Read/Write/Delete. 
	2. Use job roles to give out permissions. 
7. Do Data Classification. Public, Confidential, Secret. Yes follow the government classification schedule to an extent. It works believe it or not. 
8. Audit all applications in use. Implement allow lists for applications and make it a policy. 
9. MFA policy. Have a limited set of options and one must be a physical token. 
10. Implement an organization-wide password manager. Employees have their own vault and then there can be shared vaults with auditing. 
11. Get a good inline email security product. Needs to actively scan links, sandbox, etc... If a user clicks a phishing or malicious link then this shouldn't harm the organization. 

OK that's all I have right now based on my lived experience. 

## GrrCon Conclusion

It's already on my calendar for next year. Hopefully I can see more friends there and we can continue to learn and grow in our careers together. 

Cheers,  
Richard

You can find all of my notes from the sessions that I attended at my Bitbucket: [GrrCon 2022 Notes](https://bitbucket.org/rmaloley/grrcon-2022)

