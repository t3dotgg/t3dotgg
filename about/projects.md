# Projects

## Personal

### Dogecoin Simulator

Dogecoin Simulator is a web game heavily inspired by [Universal Paperclip](https://www.decisionproblem.com/paperclips/). I was curious how my "tech stack" held up under the load of a high thrash game engine, and had a lot of fun pushing the limits of the tech I was consuming.

Dogecoin Simulator uses React and Zustand to define all game logic and UI. Zustand's state model allowed me to centralize all the complex game logic into a [simple, typesafe state machine](https://github.com/TheoBr/dogecoin-simulator/blob/main/src/engine/game.ts).

I'm really proud of the quality of this project and the performance it maintains. [All of the code is open source, so please give it a look!](https://github.com/TheoBr/dogecoin-simulator)

### Chrometana

Chrometana is poorly maintained Chrome extension I released on the launch of Windows 10. I was frustrated as hell by Cortana only searching Bing, so I hacked together a script to redirect those searches. This extension has had over 1 million installations and is still regularly featured in reporting from The Verge, Wall Street Journal, and more. All that said, it's a tiny script that redirects Bing searches that I wrote 5 years ago and haven't touched much since.

### Personal Site and Blog

I've always enjoyed using my [personal site](https://t3.gg/) and [blog](https://t3.gg/blog) as a place to experiment with new tech and ideas. The most recent rendition is a [Next.JS](https://nextjs.org/) and Typescript site with mdx integrations for the blog (via [mdx-bundler](https://github.com/kentcdodds/mdx-bundler)), all hosted on [Vercel](https://vercel.com/). Oh also - the animations are vanilla JS this time :)

Previously, my personal site was built using [Gatsby](https://www.gatsbyjs.com/) and Typescript, with [PaperJS](http://paperjs.org/) for animation. I found this setup oddly frustrating to build and maintain, enough so that I [published a template to prevent others from having the same issues](https://github.com/TheoBr/minimal-gatsby-typescript-starter)

## Turntable - tt.fm

### Turntable Web

_January 2021 - Now_

Role: Engineering Lead, majority code contributor

The new Turntable website is a modern rethinking of the classic shared music experience from the late 2000's. It was super exciting to bring back an experience from my childhood. I lead the effort to build the new site, from hiring to architecture to CDN.

Turntable is built on React and Typescript. I lead us to adopting the most minimal viable modern solutions for problems instead of buying into bigger ecosystems - i.e. using [Zustand](https://github.com/pmndrs/zustand) and [React Query](https://react-query.tanstack.com/) over my previous choices of [Redux](https://react-redux.js.org/) and [Apollo](https://www.apollographql.com/). The majority of the experience is managed through a [Socket.io](https://socket.io/) service that is managed and persisted using these same tools.

A large amount of the effort put into Turntable was the integrations with various streaming services. I had to deobfuscate and reverse engineer Apple's MusicKit JS to add basic features like track skimming and queueing. I built track ID matching APIs to allow Spotify users to play Apple Music songs (and vice versa). We even got track provider interoperability with Soundcloud mixed in :)

### Turntable Mobile (iOS and Android)

_January 2021 - Now_

Role: Engineering Lead, majority code contributor

Excited about my success with the Moonlight project at Twitch, I wanted to push [React Native](https://reactnative.dev/) and [Expo](https://expo.io/) as far as I could. In under a month, I delievered a multi-platform Turntable experiece for iOS and Android with native Apple Music integration on both. I was lucky to have an awesome Android and iOS engineer to partner with, building Swift and Kotlin integrations that I could shim into the React Native world, seamlessly integrating the two.

The coolest part of betting on React and Typescript was the amount of interoperability with the web version. I built the React Native app first, and was able to re-use over 80% of our work in creating the website. To this day, the vast majority of state management, socket connection, routing, and API integration code is shared between both the web and mobile versions of the app.

These decisions allowed me and 2 other engineers to deliver Turntable across all platforms in under 2 months.

## Twitch

### Mod View

_August 2019 - April 2020_

Role: Technical Lead, Moderation Tools within Safety

[Mod View](http://twitch.tv/moderator) is a new channel viewing experience for moderators on Twitch that allows for full customization of the experience. Moderators can resize, remove, or dock any of a dozen widgets tailored to the moderation experience.

Mod View was the first project of for the newly formed Moderation Tools team within Safety at Twitch. I took on the role of technical lead, helping us architect a modular design that allowed for all components to be "movable" without losing state.

With Mod View, I was able to build an awesome user experience while also improving best practice for front end at Twitch. We built a modular Widget architecture that was adopted in the Stream Manager to allow for sharing of widgets between experiences. We wrote the entire feature without adding a single class, and we used Apollo's GraphQL hooks to fetch and modify all data requested. We introduced a reverse-portal pattern to allow for dragging and dropping of widgets to not trigger a re-mount, allowing for state preservation during drag and drop events.

This project is the single accomplishment I am most proud of at Twitch. We raised the bar for moderation experience and power user web tools.

### Twitch Studio

_April 2020 - now_

Role: Front End Engineer, Creator Broadcast

[Twitch Studio](https://www.twitch.tv/broadcast/studio) is a desktop streaming application built by Twitch. Studio's goal is to lower the bar for entry to make great streaming content live on Twitch.

My work on Studio has been focused on two key areas, performance and customization. I was able to use my experience with React to push this app far in both of these areas.

For performance, I was able to identify UI elements that caused a lot of render thrash. By rewriting these components with more optimized patterns, I reduced CPU usage on Mac by as much as 40%.

I was excited to apply my learnings about customizable UI from Mod View into my work on Studio. When I joined the team, the Studio UI was nearly static. I rewrote the entire UI layer with [react-mosaic](https://github.com/nomcopter/react-mosaic) and [react-dnd](https://github.com/react-dnd/react-dnd) in mind. The result is a fully customizable experience with complexity that scales to the user's unique needs

### Twitch Creator Dashboard/Stream Manager

_April 2020 - now_

Role: Front End Engineer, Creator Broadcast

The [Twitch Creator Dashboard](https://dashboard.twitch.tv/) is the home-page for streamers when live. The Stream Manager includes a fully customizable UI with addable panels for all creator-focused features across Twitch.

Dashboard is as much a platform as it is a feature, getting dozens of contributions every week from teams across the company. Most of my role on the Dashboard was related to these contributions. From the day I joined the team, I quickly became the go-to eng for all issues, incidents, and inquires from external teams who owned features within the Dashboard. I worked regularly with the core browser clients and platforms teams to push best practice and level up the quality of our code across the company. I helped push the Creator Dashboard from a new feature to a well maintained contributor platform.

### Channel Points

_March 2019 - August 2019_

Role: Full Stack Engineer, Communication & Safety

[Channel Points](https://help.twitch.tv/s/article/channel-points-guide?language=en_US) is a customizable reward system that allows creators to reward viewers for their participation.

I joined the Channel Points team to help them hit their tight deadline that was near slipping. I was originally expected to fulfill the safety requirements for the project, but ended up contributing much more, eventually creating the [Reward Queue](https://help.twitch.tv/s/article/making-the-most-of-channel-points?language=en_US#manage) used to manage Channel Points requests when the streamer is live.

### Aegis - internal safety tooling

_March 2018 - August 2019_

Role: Front End lead and Full Stack engineer, Sitewide Safety

Aegis is the internal set of web tools used by Safety Operation Specialists to review and investigate reports filed by Twitch users. Aegis was written to be flexible to enable agile development, but also designed to be compliant with the core Twitch website (a React monolith) to allow for sharing components between the two projects.

I maintained the Aegis front end project starting soon after it was created. I built and maintained our Webpack config, maintained compatibility with internal and third party packages, and designed a scaleable architecture to allow for contributors across the company to create and improve Safety tooling.

I was able to use Aegis to "test pilot" new and exciting developments in the front end world. We were one of the first projects to move to functional component design, generated typescript definitions, Mobx state management, portaled modals, graphql hooks, and much more. Almost all of these efforts resulted in the core Twitch web repo adopting them as well.

### Mission Control for Marathons

_February 2017 - March 2018_

Role: Full Stack engineer, Creative and Emerging Content team

Mission Control was an elixir-based toolset for maintaining and streaming marathon-style content on Twitch. These tools were used to run all the marathons on Twitch from Bob Ross to Pokemon until March 2019.

The tools I created were used to injest content from various broadcasting networks, transcode them to standardized formats, and stream them to twitch. Our schedules expected the ability to cut mid-asset to insert video ads, so our architecture dumped all video content into chunked transport streams, which were fed into FFMPEG to stream to Twitch. One of our engineers [gave an awesome talk at ElixirConf on this architecture](https://www.youtube.com/watch?v=eNe5dmRP9Cc)

## RPI

### Rensselaer Center for Open Source (RCOS)

I was a mentor for RCOS starting early in my time at RPI. I was disappointed by how dated most of RPI's coursework was, and how it abstained from teaching important technologies like git, linux, and even basic javascript. I used RCOS to learn and mentor others in modern, open source technologies, helping hundreds of students contribute to dozens of open source projects.

### MetPetDB

I was a full stack developer for MetPetDB during my time at RPI. MetPet is an open source geology database. I helped create the front end and get the project onto modern service architecture
