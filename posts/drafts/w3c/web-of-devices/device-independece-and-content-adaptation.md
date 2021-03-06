DEVICE INDEPENDENCE AND CONTENT ADAPTATION

current status：
+ Device Description Repository
+ Device Independence Authoring
+ CC/PP
+ Content Transformation
+ DCCI

What is Device Independence?

At it's inception, virtually the only way to access the Web was through a personal computer or workstation. While there were lots of variations, accessing the Web almost always involved using a modern computer with a reasonably large color display.

Computers may still be the primary means of accessing the Web, but in recent years the number of different kinds of devices accessing the Web has grown by leaps and bounds. Mobile phones, personal digital assistants, eBook readers, television systems, voice response systems, music players, kiosks, digital picture frames, in-car navigation systems and even domestic appliances are all starting to access the Web more and more.

Device Independence refers to the goal of having a single Web that is accessible from any of these devices.

What is Content Adaptation Used For?

Content Adaptation is a process that based on factors such as the capabilities of the displaying device or network, or the user's preferences, adapts the content that has been requested to provide an optimized user experience. This adaptation can occur in a number of places in the content delivery chain: the author may make choices when writing the content, or intermediary automated content transformation proxies could adapt the content based on heuristics and knowledge of the user, or the adaptation could occur within the browser itself.

Examples

Content that is adapted to the user's device is commonplace on the mobile Web. Two different mobile devices may have radically different display capabilities, for instance one may have a black and white display that is very low resolution, while another mobile device may have a full color 480x320 resolution display. Yet sites that use content adaptation techniques can provide both devices access to the same information.

For example, the content author may wish to use one set of colors when displaying their content on the color display, but may find the results illegible when displayed in black and white. The author could use the following HTML to style the page in full color only when a color display has been detected:

	<link rel="stylesheet" media="screen and (color)" href="color.css" />

This code would cause the browser to evaluate what type of display the content is being rendered on, and determine whether or not to use the style information included in the "color.css" style-sheet.

Learn More

To learn more about authoring content that can be delivered to a wide variety of devices, please see the Authoring Techniques for Device Independence.

The Guidelines for Web Content Transformation Proxies provides guidance to Content Transformation proxies as to whether and how to transform Web content.

And lastly, the Glossary of Terms for Device Independence provides a detailed explanation of all of the terms that are commonly used in the area of Device Independence.