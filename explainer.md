# Enhancing Web User Agents Performance 

## Background 

On 10th January, W3C China Host organized a successful event for the W3C community in China as part of its regular WebEvolve seminars, where W3C Members are invited to learn about the latest W3C technologies and explore new opportunities on the Web. This seminar, titled _WebAI and High-Performance Web Application Technology_, gathered about 50 experts who discussed the evolution of the local and global industry through W3C standards. Speakers from Bytedance, Huawei, Intel, Microsoft, Tencent and W3C, among others, presented the current and future standardization activities around __AI__ and discussed the __need to enhance the Web for performance and better UX__.

In the high-performance topic, __Yao Vic (Tencent)__ and __Wang Zuo (Huawei)__ presented interesting insights about the real usage and implementation of Web standards in terms of HTML elements, CSS modules, APIs, and DOM properties and methods by cross-platform frameworks and popular Web apps. Motivated by these early findings and looking for innovative and efficient solutions in the future, we discussed the possibility of launching a new incubation activity in W3C to collect more insights and explore the topic. Of course, we also discussed previous similar attempts (i.e., [media profiles](https://dvcs.w3.org/hg/webtv/raw-file/tip/media-profile/Overview.html#app-environment), [EPUB](https://www.w3.org/TR/epub-overview-33/), [AMP](https://amp.dev/about/), [CSS TV Profile](https://www.w3.org/TR/css-tv/),  and others), but also about fragmentation, interoperability, and preserving the "one web". 

We launched an exploratory Community Group as a placeholder during the event, initially named _High-Performance Baseline for Web Apps CG_, but still to determine the final denomination, scope and objectives. __This first proposal is an starting point of discussion__ of the target and details of this potential new activity. 

## About the High-Performance Web Apps Community Group 

The High-Performance Web Apps Community Group aims to diversify the ecosystem of Web user agents by enabling a profile standards to increase efficiency and optimize the user experience on Web and WebView-based apps while maintaining compatibility with existing standards. Standard profiles and modularity allow the implementation of lighter and more efficient engines for specific-scenario purposes when a full-fledged (embedded) browser is not required (e.g., MiniApps, WoT edge apps, and apps for wearables or constrained infotainment systems) and may serve as common ground for cross-platform development frameworks. Furthermore, establishing standard-based profiles would facilitate the development roadmap of new Web user agents (e.g., Servo and Ladybird) from scratch.  

This CG is a forum for vendors of embedded browsers, hybrid cross-platform app frameworks, JS engines and others interested in exploring the modularity of the Web standards. We aim to collect use cases where standard profiles help enrich the Web ecosystem by opening new possibilities in unexplored scenarios and supporting innovation on the Web while protecting the principles of universality and interoperability.   

This group needs close alignment with other incubation groups working on similar topics (i.e., [WebViews CG](https://www.w3.org/community/webview/), [WinterTC](https://wintertc.org/)) and bi-directional conversations with core standardization groups for advice and pushing for new standardization requirements while avoiding fragmentation. We will start with the use case collection and continue with more specific goals, like defining and testing specific scenario profiles to validate the concept.

## Previous attempts to modularize the Web

In the past, specific industries have created profiles and subsets of web standards targeting the unique requirements for concrete scenarios and devices. Among the successful examples, we highlight the well-established [EPUB](https://www.w3.org/TR/epub-overview-33/) format for digital publications and documents and the [Hybrid Broadcast Broadband TV (HbbTV)](https://www.hbbtv.org/overview/#hbbtv-overview) for broadcast and broadband delivery of entertainment services through connected TVs, set‐top boxes and multiscreen devices. Newer standards superseded early initiatives like CE HTML (Consumer Electronics HTML), developed within the Consumer Electronics Association (CEA), as part of the [CEA-2014 standard](https://en.wikipedia.org/wiki/Universal_Plug_and_Play#AV_standards) or Web4CE (Web for Consumer Electronics), defined subsets of HTML, CSS, and JavaScript for limited-resource devices. Closed in 2010, the [Compound Document Formats (CDF)](https://www.w3.org/2004/CDF/) Working Group also defined a lightweight web standard for devices with limited processing power and memory. A Compound Document is the W3C term for a document that combines multiple formats, such as XHTML, SVG, SMIL and XForms. 

During the 2000s, the W3C's Mobile Web Best Practices provided guidelines for using the basic web standards on mobile devices, at that time, with limited processing power, memory, screen size, and UI capabilities. This specification was not a profile but offered guidance to serve content differently to maximize performance and user experience on the go - a novelty at that time. 

HbbTV is based on Web standards like HTML5 (structure of the content), CSS (styling and layout), ECMAScript (interaction), DOM (content manipulation), Fetch API (network communication), Media Source Extensions (adaptive video streaming), and Encrypted Media Extensions (content protection). HbbTV also needed extensions for the concrete use cases (e.g., W3C's [TV Control Working Group](https://www.w3.org/2016/03/tvcontrol.html) activities).

The objective of these initiatives was the same: specifying the behaviour of some format and protocol combinations and addressing the needs for an extensible and interoperable Web across specific vertical use cases.

Google's [AMP](https://amp.dev/about/) or Baidu's [MIP](https://baike.baidu.com/item/MIP/19895149) (Mobile Instant Pages) are also built on HTML, CSS, and ECMAScript standards, restricting the use of these technologies and introducing custom elements to increase performance. Facebook Instant Articles uses a subset of HTML and CSS for fast loading articles in the platform. 

## Standard profiles and extensions for concrete use cases

In some cases, the innovative scenario might require extending the existing standards, as occurred with the TV profile, to enable new ways of user interaction using a TV remote control. For this, the group should incubate a new proposal in the community group (also using WICG or the newly created Incubation IG) while aligning with related W3C groups (e.g., with Web Apps WG if a new manifest member is required). If there are no groups related to the topic, a new WG may be proposed to address the requirement (e.g., the [TV Control API](https://www.w3.org/TR/tvcontrol-api/) was created under the [TV Control Working Group](https://www.w3.org/2016/03/tvcontrol.html))          

## Potential use cases

- __Web of Things__: Specific profiles for IoT devices which often have limited resources, to increase the adoption of WoT in the industry. These profiles may facilitate the implementation and deployment of user agents in low-computational power devices with restricted user interaction capabilities while maximizing user experience and accessibility.
- __MiniApps__: The MiniApp WG has worked with the pioneer ecosystems of MiniApps, detecting close similarities with the Web and aiming to make the most of the Web standards to avoid fragmentation in the MiniApps platforms while enabling convergence with the Web. Most MiniApps development environments use HTML-like domain-specific languages, a profile of (almost standard) CSS and restricted ECMAScript execution. However, there are no standards for designing and programming MiniApp content, which could be directly solved with specific profiles of the existing standards.
- __Performant user agents__: Modularity may facilitate lighter, more efficient web engines addressing specific use cases. Focused on the concrete functionality and rendering options, user agents could be designed to maximize performance and user experience while maintaining compatibility with standards. Digital Publishing activities have demonstrated a clear example of this, targeting profiles for e-book readers.
New user agents: Incremental profiles could motivate the development of alternative Web engines by facilitating and simplifying the design (e.g., a profile that includes specific CSS modules and non-deprecated standard HTML elements).

## Why a modular Web?

To guarantee the competitivity of web technologies against native environments, guaranteeing the evolution of Web functionalities rapidly while maximizing accessibility and user experience. 
To enable interoperability in fragmented scenarios through facilitating development guidelines based on well-established web standards (e.g.,  MiniApps with similar requirements and using different domain-specific languages and APIs).
To increase the adoption of Web technologies in new scenarios like WoT lite applications (e.g., user interfaces for sensors and actuators based on WoT that will guarantee accessibility and usability of edge devices).
To increase user agent diversity and enable a broader ecosystem of web engines, facilitating modular development based on scenarios and target devices. 

What do we need to consider?
First, avoid breaking the web architecture and preserve the foundations of the Web, including accessibility, privacy, security and internationalization. 

The group should leverage the Progressive Web Apps (PWAs) principles and growth, supporting features such as offline functionality and using the App Manifest for homogeneous metadata and profile descriptions. A richer, RDF-based manifest should not be discarded either. 

We aim to connect and get early feedback and insights from communities like WoT, Web browsers under early development (e.g., [Ladybird](https://ladybird.org/) and [Servo](https://servo.org/)), and specific hybrid platforms and embedded browsers (e.g., Super-Apps).  

The group needs close alignment with other incubation groups working on similar topics, including but not limited to the following:

- [WebViews CG](https://www.w3.org/community/webview/), 
- [MiniApps WG](https://www.w3.org/groups/wg/miniapps/),
- [WinterTC](https://wintertc.org/)

