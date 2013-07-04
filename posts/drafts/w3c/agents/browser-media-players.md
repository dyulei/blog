BROWSERS, MEDIA PLAYERS

current status：
+ Security or User Agents
+ DOM
+ HTML
+ HTML for User Agents
+ User Agent Accessibility Guidelines (UAAG)
+ Plugins
+ Web IDL

'User agents' - web browsers, media players, browser extensions, on-the-fly converters, plug-ins, bots, aggregators and mobile browsers - provide a human or machine interface to the web. At their best, they allow all of us to explore a universal space of web content.

Examples of user agent standards issues

User agent developers need to pay particular heed to issues surrounding use of their agents by people in other parts of the world, speaking other languages, using other devices and with a variety of assistive technologies that allow users to use different modes of input and output (such as speech input, tactile displays, semantic navigation, and a variety of display preferences).

Example 1: An online app developer wants to provide context-sensitive help in a tooltip that is displayed when the user (with a mouse) hovers over or (with a keyboard) focuses a "Help" icon. In most browsers, the functionality automatically works for hover; the title element is displayed. However, most browsers don't provide the same functionality for keyboard users on focus. To compensate for the missing functionality in the browsers, the developer has to create scripts to provide it for her content. Unfortunately most developers don't do this - and indeed, they shouldn't have to because the browser should provide the same functionality for people who cannot use the mouse.

Example 2: A developer uses the css declaration text-transform: lowercase to style a magazine headline (about fresh orange juice) originally composed in caps. The content is then internationalised for a Turkish-language audience, and a language of Turkish declared using the attribute lang="tr". The lower case of the Turkish character İ (a capital I dotted) should return a i. Major browsers, however convert the Turkish character I to i. An innocuous headline "Squeeze Often" suddenly becomes rather rude...

W3C staff documented some Common User Agent Problems in a Team Submission, still a useful document although it was published in 2003.

Accessibility Guidelines for User Agents

W3C publishes guidelines for creating accessible authoring tools: User Agent Accessibility Guidelines (UAAG). UAAG 2.0 is intended for the current and future generation of user agents. You can implement the latest draft of the User Agent Accessibility Guidelines (UAAG 2.0) by following Implementing UAAG 2.0 - a guide to implementing and understanding the guidelines.

You may also wish to consult the current formally approved, stable and referenceable technical recommendation for accessibility is UAAG 1.0.

Browser developers need some help at making the web readable by all; extension developers can respond to limitations of particular browser functionality, and the best extensions can be incorporated into the browsers' standard functionality. Whether you develop browsers, extensions, bots, aggregators, media players or an as-yet undreamed of way of reading the web, to create that web that is readable by all, the User Agent Accessibility Guidelines provide the place to start.