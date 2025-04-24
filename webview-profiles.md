# Application Profiles for Web Engine Diversity 

<!-- TOC -->

- [Application Profiles for Web Engine Diversity](#application-profiles-for-web-engine-diversity)
    - [Abstract](#abstract)
    - [Challenge: full-fledged web engines are too heavy](#challenge-full-fledged-web-engines-are-too-heavy)
    - [Proposal: modular web engines?](#proposal-modular-web-engines)
        - [Use cases to explore](#use-cases-to-explore)
        - [Why a modular Web?](#why-a-modular-web)
        - [What do we should consider?](#what-do-we-should-consider)
    - [Background](#background)
        - [Early discussions at _WebEvolve_ seminar](#early-discussions-at-_webevolve_-seminar)
        - [Discussion at W3C Breakout Day 2025](#discussion-at-w3c-breakout-day-2025)
        - [Previous attempts to modularize the Web](#previous-attempts-to-modularize-the-web)

<!-- /TOC -->

## Abstract

This proposal aims to discuss **profile standards** (subsets of current specifications) to increase efficiency and optimize the user experience on **WebView-based apps** while maintaining **compatibility with existing standards** to diversify the ecosystem of Web user agents and spread the adoption of the Web platform in new scenarios. Standard profiles and modularity must facilitate the implementation of lighter and more efficient engines for specific-scenario purposes when a full-fledged WebView (or embedded browser) is not required (e.g., MiniApps, WoT edge apps, and apps for wearables or constrained infotainment systems) and may serve as common ground for cross-platform development frameworks. Furthermore, establishing standard-based profiles may facilitate the development roadmap of new Web user agents from scratch.  

## Challenge: full-fledged web engines are too heavy  

In the last 35 years, the Web has grown unstoppably (and successfully) to cover the broadest use cases and scenarios, making _the only one_ universal platform. Consequently, web engines have evolved to support this evolution with a subsequent increase of size and device requirements. In some specific cases and applications, Web-based content or applications do not need full-fledged Web browsers or WebViews, just a reduced part of it.

**MiniApps** is a concrete example of WebView-based content, that does not require a full implementation of Web standards. Indeed, MiniApp platforms use hybrid technologies but are close to Web standards (e.g., CSS modules, something like HTML, standard JavaScript and APIs). Still, these platforms are fragmented, so publishers cannot develop once and distribute the app to other platforms unless they use cross-platform solutions (e.g., [Taro](https://docs.taro.zone/en/docs/)).  

Other examples are WebViews for apps running on **devices with limited capabilities**, like e-ink interactive appliance controls or non-visual interfaces. In this case, the WebView must be lighter and align with the available resources.    

In the early phases of **new web engines** development, teams must prioritize what features will be developed first to continuously improve the product. Could these teams benefit from pre-defined application profiles to evolve the new browsers? Every release could support new types of apps.    

## Proposal: modular web engines?

To diversify the ecosystem of Web user agents, enabling **profile standards** (subsets of current specifications) to increase efficiency and optimize the user experience on WebView-based apps while maintaining **compatibility with existing standards**. Standard profiles and modularity must allow the implementation of lighter and more efficient engines for specific-scenario purposes when a full-fledged WebView (or embedded browser) is not required (e.g., MiniApps, WoT edge apps, and apps for wearables or constrained infotainment systems) and may serve as common ground for cross-platform development frameworks. Furthermore, establishing standard-based profiles would facilitate the development roadmap of new Web user agents (e.g., Servo and Ladybird) from scratch.  

These standard profiles aim to help enrich the Web ecosystem by opening new possibilities in unexplored scenarios and supporting innovation on the Web while protecting the principles of universality and interoperability.    

### Use cases to explore 

1. __Web of Things__: Specific profiles for IoT devices which often have limited resources (e.g., performance, UI mechanisms, etc.). Concrete WoT app profiles may facilitate the implementation and deployment of user agents in low-computational power devices with restricted user interaction capabilities while maximizing user experience and accessibility.
2. __MiniApps__: The MiniApp WG has worked with the pioneer ecosystems of MiniApps, detecting close similarities with the Web and aiming to make the most of the Web standards to avoid fragmentation in the MiniApps platforms while enabling convergence with the Web. Most MiniApps development environments use HTML-like domain-specific languages, a profile of (almost standard) CSS and restricted ECMAScript execution. However, there are no standards for designing and programming MiniApp content, which could be directly solved with specific profiles of the existing standards.
3. __New user agents__: New user agents: Incremental profiles could motivate the development of alternative Web engines by facilitating and simplifying the design (e.g., a profile that includes specific CSS modules and avoids specific APIs at the first iterations).


### Why a modular Web?

- To guarantee the competitivity of web technologies against native environments, guaranteeing the evolution of Web functionalities rapidly while maximizing accessibility and user experience. 
- To enable interoperability in fragmented scenarios by facilitating development guidelines based on well-established web standards (e.g.,  MiniApps with similar requirements and using different domain-specific languages and APIs).
- To increase the adoption of Web technologies in new scenarios like WoT lite applications (e.g., user interfaces for sensors and actuators based on WoT that will guarantee accessibility and usability of edge devices).
- To increase user agent diversity and enable a broader ecosystem of web engines, facilitating modular development based on scenarios and target devices. 

### What do we should consider?

First, and foremost, __avoid breaking the web architecture__ and preserve the foundations of the Web, including accessibility, privacy, security and internationalization. 

We should leverage the Progressive Web Apps (PWAs) principles and growth, supporting features such as offline functionality and using the App Manifest for homogeneous metadata and profile descriptions. A richer, RDF-based manifest should not be discarded either. 

We aim to connect and get early feedback and insights from communities like WoT, Web engines under early development, and specific hybrid platforms and embedded browsers (e.g., SuperApps).  

Of course, we need close alignment with other incubation groups working on similar topics, including but not limited to the following:

- [WebDX CG](https://www.w3.org/community/webdx/), 
- [WebViews CG](https://www.w3.org/community/webview/), 
- [MiniApps WG](https://www.w3.org/groups/wg/miniapps/),
- [WinterTC](https://wintertc.org/)


## Background 

### Early discussions at _WebEvolve_ seminar

On 10 January, W3C China Host organized a successful event for the W3C community in China as part of its regular WebEvolve seminars, where W3C Members are invited to learn about the latest W3C technologies and explore new opportunities on the Web. This seminar, titled _WebAI and High-Performance Web Application Technology_, gathered about 50 experts who discussed the evolution of the local and global industry through W3C standards. Speakers from Bytedance, Huawei, Intel, Microsoft, Tencent and W3C, among others, presented the current and future standardization activities around __AI__ and discussed the __need to enhance the Web for performance and better UX__.

In the high-performance topic, __Yao Vic (Tencent)__ and __Wang Zuo (Huawei)__ presented interesting insights about the real usage and implementation of Web standards in terms of HTML elements, CSS modules, APIs, and DOM properties and methods by cross-platform frameworks and popular Web apps. Motivated by these early findings and looking for innovative and efficient solutions in the future, we discussed the possibility of launching a new incubation activity in W3C to collect more insights and explore the topic. Of course, we also discussed previous similar attempts (i.e., [media profiles](https://dvcs.w3.org/hg/webtv/raw-file/tip/media-profile/Overview.html#app-environment), [EPUB](https://www.w3.org/TR/epub-overview-33/), [AMP](https://amp.dev/about/), [CSS TV Profile](https://www.w3.org/TR/css-tv/),  and others), but also about fragmentation, interoperability, and preserving the "one web". 

We launched an exploratory Community Group as a placeholder during the event, initially named [High-Performance Baseline for Web Apps CG](https://www.w3.org/groups/cg/high-perf-baseline/), but still to determine the final denomination, scope and objectives. __This first proposal is a starting point of discussion__ of the target and details of this potential new activity.  

### Discussion at W3C Breakout Day 2025

The discussion continued on 26 March 2025. During the [W3C Breakouts Day 2025](https://www.w3.org/2025/03/breakouts-day-2025/), we organized a session titled [More performant, diverse Web engines](https://www.w3.org/2025/03/breakouts-day-2025/#b-47c8159d-9fea-4778-9b04-bd28a479a7c2), to widely discuss this with the community. There, we asked for the first impressions about this potential work to enhance Web apps' performance and increase Web technologies' usage to deliver apps and services.

Two different perspectives were presented:

1. Vic Yao presented a [proposal for developing a new engine](https://docs.google.com/presentation/d/1f0fm5OpE7vwqQkKfNwvYuzH7O3WyPsK4xSIiegLplbg/edit#slide=id.p) for apps, based on: 
  - Distributed packages, like in native apps and MiniApps;
  - Extensibility, Mixing binary code and script code;
  - Mobile-Friendly by default;
  - Reuse of CSS and Web APIs but redesigning components

2. Martin Alvarez (me), presented a [proposal based on modularity](https://espinr.github.io/talks/2025/0326-Web-Engines-Breakout/#s6), to cover concrete use cases and scenarios where the Web is not yet there and might be a qualified platform to deliver accessible and universal services __through reduced WebViews__. Inspired by [successful cases like EPUB](https://www.w3.org/TR/epub-33/#sec-contentdocs) (for e-readers) and [Web Media APIs](https://w3c.github.io/webmediaapi/) (for TV and media consumer electronics), this proposal aims to develop profiles of Web standards to cover cases like MiniApps, simple WoT (Web of Things) apps, or support the development of new Web engines from scratch based on target priorities.             


### Previous attempts to modularize the Web

In the past, specific industries have created profiles and subsets of web standards targeting the unique requirements for concrete scenarios and devices. Among the successful examples, we highlight the well-established [EPUB](https://www.w3.org/TR/epub-overview-33/) format for digital publications and documents and the [Hybrid Broadcast Broadband TV (HbbTV)](https://www.hbbtv.org/overview/#hbbtv-overview) for broadcast and broadband delivery of entertainment services through connected TVs, set‐top boxes and multiscreen devices. Newer standards superseded early initiatives like CE HTML (Consumer Electronics HTML), developed within the Consumer Electronics Association (CEA), as part of the [CEA-2014 standard](https://en.wikipedia.org/wiki/Universal_Plug_and_Play#AV_standards) or Web4CE (Web for Consumer Electronics), defined subsets of HTML, CSS, and JavaScript for limited-resource devices. Closed in 2010, the [Compound Document Formats (CDF)](https://www.w3.org/2004/CDF/) Working Group also defined a lightweight web standard for devices with limited processing power and memory. A Compound Document is the W3C term for a document that combines multiple formats, such as XHTML, SVG, SMIL and XForms. 

During the 2000s, the W3C's Mobile Web Best Practices provided guidelines for using the basic web standards on mobile devices, at that time, with limited processing power, memory, screen size, and UI capabilities. This specification was not a profile but offered guidance to serve content differently to maximize performance and user experience on the go - a novelty at that time. 

HbbTV is based on Web standards like HTML5 (structure of the content), CSS (styling and layout), ECMAScript (interaction), DOM (content manipulation), Fetch API (network communication), Media Source Extensions (adaptive video streaming), and Encrypted Media Extensions (content protection). HbbTV also needed extensions for the concrete use cases (e.g., W3C's [TV Control Working Group](https://www.w3.org/2016/03/tvcontrol.html) activities).

The objective of these initiatives was the same: specifying the behaviour of some format and protocol combinations and addressing the needs for an extensible and interoperable Web across specific vertical use cases.

Google's [AMP](https://amp.dev/about/) or Baidu's [MIP](https://baike.baidu.com/item/MIP/19895149) (Mobile Instant Pages) are also built on HTML, CSS, and ECMAScript standards, restricting the use of these technologies and introducing custom elements to increase performance. Facebook Instant Articles uses a subset of HTML and CSS for fast loading articles in the platform. 

