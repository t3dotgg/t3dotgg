# Projects

## Twitch
### Mod View

*August 2019 - April 2020*

Role: Technical Lead, Moderation Tools within Safety

[Mod View](http://twitch.tv/moderator) is a new channel viewing experience for moderators on Twitch that allows for full customization of the experience. Moderators can resize, remove, or dock any of a dozen widgets tailored to the moderation experience.

Mod View was the first project of for the newly formed Moderation Tools team within Safety at Twitch. I took on the role of technical lead, helping us architect a modular design that allowed for all components to be "movable" without losing state.

With Mod View, I was able to build an awesome user experience while also improving best practice for front end at Twitch. We built a modular Widget architecture that was adopted in the Stream Manager to allow for sharing of widgets between experiences. We wrote the entire feature without adding a single class, and we used Apollo's GraphQL hooks to fetch and modify all data requested. We introduced a reverse-portal pattern to allow for dragging and dropping of widgets to not trigger a re-mount, allowing for state preservation during drag and drop events.

This project is the single accomplishment I am most proud of at Twitch. We raised the bar for moderation experience and power user web tools.

### Channel Points

*March 2019 - August 2019*

Role: Full Stack Engineer, Communication & Safety

[Channel Points](https://help.twitch.tv/s/article/channel-points-guide?language=en_US) is a customizable reward system that allows creators to reward viewers for their participation.

I joined the Channel Points team to help them hit their tight deadline that was near slipping. I was originally expected to fulfill the safety requirements for the project, but ended up contributing much more, eventually creating the [Reward Queue](https://help.twitch.tv/s/article/making-the-most-of-channel-points?language=en_US#manage) used to manage Channel Points requests when the streamer is live. 

### Aegis - internal safety tooling

*March 2018 - August 2019*

Role: Front End lead and Full Stack engineer, Sitewide Safety

Aegis is the internal set of web tools used by Safety Operation Specialists to review and investigate reports filed by Twitch users. Aegis was written to be flexible to enable agile development, but also designed to be compliant with the core Twitch website (a React monolith) to allow for sharing components between the two projects.

I maintained the Aegis front end project starting soon after it was created. I built and maintained our Webpack config, maintained compatibility with internal and third party packages, and designed a scaleable architecture to allow for contributors across the company to create and improve Safety tooling.

I was able to use Aegis to "test pilot" new and exciting developments in the front end world. We were one of the first projects to move to functional component design, generated typescript definitions, Mobx state management, portaled modals, graphql hooks, and much more. Almost all of these efforts resulted in the core Twitch web repo adopting them as well.

### Mission Control for Marathons

*February 2017-March 2018*

Role: Full Stack engineer, Creative and Emerging Content team

Mission Control was an elixir-based toolset for maintaining and streaming marathon-style content on Twitch. These tools were used to run all the marathons on Twitch from Bob Ross to Pokemon until March 2019.

The tools I created were used to injest content from various broadcasting networks, transcode them to standardized formats, and stream them to twitch. Our schedules expected the ability to cut mid-asset to insert video ads, so our architecture dumped all video content into chunked transport streams, which were fed into FFMPEG to stream to Twitch. One of our engineers [gave an awesome talk at ElixirConf on this architecture](https://www.youtube.com/watch?v=eNe5dmRP9Cc)

## RPI
### Rensselaer Center for Open Source (RCOS)
I was a mentor for RCOS starting early in my time at RPI. I was disappointed by how dated most of RPI's coursework was, and how it abstained from teaching important technologies like git, linux, and even basic javascript. I used RCOS to learn and mentor others in modern, open source technologies, helping hundreds of students contribute to dozens of open source projects.

### MetPetDB
I was a full stack developer for MetPetDB during my time at RPI. MetPet is an open source geology database. I helped create the front end and get the project onto modern service architecture

## Personal open source
### Chrometana
Chrometana is poorly maintained Chrome extension I released on the launch of Windows 10. I was frustrated as hell by Cortana only searching Bing, so I hacked together a script to redirect those searches. This extension has had over 1 million installations and is still regularly featured in reporting from The Verge, Wall Street Journal, and more. Reminder - it's a tiny script that redirects Bing searches to whatever.
