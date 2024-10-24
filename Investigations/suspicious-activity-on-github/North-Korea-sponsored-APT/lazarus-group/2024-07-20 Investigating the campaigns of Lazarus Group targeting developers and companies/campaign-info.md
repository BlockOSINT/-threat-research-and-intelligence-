# Investigation

This investigation focus into suspicious campaigns targeting developers, employers, and companies, which have been linked to the North Korean state-sponsored hacking group, Lazarus. The findings were published on Medium

The primary goal of this investigation was to capture and document as much information as possible before it was removed. A significant portion of the data was not published in the Medium article, as following the release of our previous investigation, many of the accounts disappeared within days

- (https://medium.com/coinmonks/investigating-the-activity-of-lazarus-group-targeting-developers-and-companies-182611f89cf0)

# Source

The accounts listed here are part of an investigation into malicious actors on GitHub. Much of this activity, related to fake recruiters and employees, has been primarily associated with the Lazarus Group.

The accounts were manually scraped, with specific characteristics filtered, such as:

- Creation date: account creation, activity 

- Follow/Follower: these accounts follow each other like a network

- Suspicious repository activity: "forker", "stars other empty profiles", identical repositories, same "projects"

- Bio: many of these profiles have similar descriptions

- Context: Accounts with broken links, AI-generated images, profiles in Latin America with an Asian appearance, and accounts with no history

- Logical pattern: activity not related to account, knowledge scope, skill-set

# Update

No update

# Details

This investigation aims to uncover the suspicious activity related to fake profiles of developers, companies, and recruiters, primarily focused on GitHub. While this attack vector has already been mentioned, our recent findings show an evolution, aiming to give more credibility to these fake identities through the creation of more coherent profiles, including their own websites.

The discovered structure seem related to the Contagious Interview (CL-STA-0420) and Wagemole (CL-STA-0421) campaigns. Both campaigns are linked to the North Korean state-sponsored advanced persistent threat (APT38) known as the Lazarus Group.

The first campaign, is called “Contagious Interview,” involves threat actors posing as employers — often with anonymous or vague identities — to entice software developers into installing malware during the interview process. This malware has the potential to facilitate various forms of theft.

The second campaign, named “Wagemole,” involves threat actors seeking unauthorized employment with organizations in the US and other global locations, aiming for both financial gain and espionage.

This is the second part of a comprehensive investigation into large-scale fraudulent activity targeting GitHub and LinkedIn.

GitHub reported this suspicious activity with high confidence, attributing the campaign to a group supporting North Korean objectives. This group is tracked by the cybersecurity industry under various names, including Lazarus Group, APT38, Jade Sleet, BlueNoroff, TraderTraitor, and Stardust Chollima

# Key:

It’s important to highlight that the Lazarus Group’s campaigns are diverse, with evolving tactics, tools, and targets. Likewise, it should be detailed that these campaigns, associated with malware distribution or infiltration through various methods, have been documented since 2019 under different names (Operation Dream Job, also known as DeathNote or NukeSped). Therefore, the findings mentioned here are a sample of Lazarus Group’s most recent sophisticated social engineering campaign.

The initial investigation highlighted massive activity on GitHub, including the creation of fake recruiter profiles on a large scale. This activity was also linked to other recruiters on GitHub. The investigation uncovered much of the infrastructure used to conduct these campaigns.

- On one hand, it revealed the creation of websites that redirect to both legitimate and fake profiles on GitHub, as well as phishing sites impersonating GitHub.

- Over 4,000 phishing websites were found redirecting to fake and real GitHub profiles.

- Additionally, at least 1,000 fake websites were identified, simulating developers.

- Similarly, at least 600 phishing websites were found that mimic real companies, with other domains redirecting to legitimate sites.

- Much of the activity related to these domains is interconnected, and numerous documents reported as trojans or malware were found communicating with these websites.

- The investigation also revealed the threat actor’s preference for uploading npm packages, with the distribution of these packages recently associated with campaigns by threat actors linked to Lazarus.

- The campaign, linked to the North Korean Lazarus hacking group, involves a low-volume social engineering effort identified by GitHub that targets personal accounts of technology firm employees using a mix of repository invitations and malicious npm package dependencies, according to GitHub’s security advisory. The North Korean hackers reportedly compromise legitimate accounts or create fake personas on GitHub and social media, posing as recruiters and developers, and initiate contact with the intention of moving conversations to other platforms

- All of the above was evident in this investigation, where much of the infrastructure used to carry out these campaigns was uncovered.

- From this investigation, suspicious traffic was observed related to the creation of fake profiles on HubSpot and phishing websites mimicking Meta. Additionally, thousands of betting sites were identified, mostly impersonating Bet365 and other betting platforms. Many of these sites and their infrastructure are reported to be hosted in Hong Kong.



# Links:

- [kaspersky](https://www.kaspersky.com/about/press-releases/2023_evolution-of-lazarus-deathnote-cluster-from-cryptocurrency-attacks-to-the-defense-sector)
- [Criticalstart](https://www.criticalstart.com/lazarus-group-updates-operation-dream-job-campaign/)
- [Securelist](https://securelist.com/the-lazarus-group-deathnote-campaign/109490/)
- [Socket.dev] https://socket.dev/blog/social-engineering-campaign-npm-malware
- [The hacker news](https://thehackernews.com/2023/04/lazarus-hacker-group-evolves-tactics.html)
- [Palo Alto](https://unit42.paloaltonetworks.com/two-campaigns-by-north-korea-bad-actors-target-job-hunters/)
- [GitHub](https://github.blog/security/vulnerability-research/security-alert-social-engineering-campaign-targets-technology-industry-employees/)
- [Tayvano](https://github.com/tayvano/lazarus-bluenoroff-research)
- [Mitre](https://attack.mitre.org/groups/G0082/)
- [CISA](https://www.cisa.gov/news-events/cybersecurity-advisories/aa22-108a)
- [The Bundesamt für Verfassungsschutz (BfV) of the Federal Republic of Germany](https://www.verfassungsschutz.de/SharedDocs/publikationen/DE/cyberabwehr/2024-02-19-joint-cyber-security-advisory-englisch.pdf?__blob=publicationFile&v=2)
