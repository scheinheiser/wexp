# Hosting Options
There are two main hosting options for this product on a smartphone; either as a website, or as a native app.\
The product could also be built to work on a feature phone, similar to the recent rise of [dumb phones](https://www.vice.com/en/article/best-dumb-phones/), or it could be modelled around using a specific feature on smartphones (like [USSD codes](https://en.wikipedia.org/wiki/Unstructured_Supplementary_Service_Data)).

## Native Application
The benefits of this option are clear, with some less obvious benefits:
+ It's easier for users to find your product, as it'll be displayed in the App Store for that device.
+ It'd be more convenient for users to just open an app from their home screen, rather than have to use their search engine to access the product.
+ You might have access to more information about the device than if you worked with a web app (i.e. you'd be able to request information about the RAM to see if you'd need to adjust graphics, etc)
+ The product would generally perform better than a web app, as the software can be optimised to work with the device hardware - web apps can't do this, leading to their reduced performance.
+ Users would be able to better integrate the app with their daily life, through functions offered by the devices' OS; for example, you can create Shortcuts on IOS devices to perform certain actions like opening the app or making a GIF.
+ Native apps can be used offline, giving the user more flexibility in how they use it.

There are some downsides to this choice of host, however:
- You have to abide by the vendor's app guidelines, and it the time it takes for the app to be reviewed is quite unpredictable (possibly affecting deadlines).
- Unless you want to limit yourself to just one phone OS, you'd need to either familiarise yourself with mulitple different programming languages to be able to increase your userbase or hire developers that are familiar with those languages. This would be very costly and time consuming, and it'd be combined with the need to also maintain the application on each platform.
- You may need to entirely redesign parts of the application if it relies heavily on APIs that just aren't present/available in the other OS, increasing development time and cost.
- Most platforms require you to pay a fee before you're able to publish the app onto its store; some are more costly than others (e.g. Apple requires you to pay $99 yearly to publish apps).

Overall, I think that this is a solid option that works best if you target a single platform; you get all of the benefits of increased performance, offline usage and a look tailored to the operating system while removing the costly development.\
While this would mean that you lose out on the larger customer base initially, if the product is successful it wouldn't be too difficult to expand the development team to also work on the app for another OS. If the product isn't as successful as hoped, then it would mean that you didn't sink too much money into the app development anyways, reducing the impact of the failure.

## Web Application
This platform can have different advantages, depending on if the site is self-hosted or published using hoster similar to [Squarespace](https://www.squarespace.com) or [GoDaddy](https://www.godaddy.com).\
Being self-hosted does give you more control over the design of your website, along with how the data is managed; it also removes the reliance on a 3rd party to host your site, preventing any issues with their services going down and affecting your website. It does, however, have a lot of upfront costs - purchasing all of the necessary equipment (e.g. a server and cables) is pricey, especially if you expect a lot of traffic.\
It also can be difficult to maintain a server, as it requires a lot of knowledge about the infrastructure to debug issues; you also need to have protection against common cyberattacks like (D)DoS ((Distributed)-Denial-of-Servce) attacks, which could easily take down your website and stop users from accessing the app.

Focusing on the general benefits of web apps:
+ Unlike native apps, the same codebase can be used on many different browsers - all major browsers support Javascript, with the ability to use [WebAssembly](https://webassembly.org)[^1] to run other languages as necessary (given that the language can be compiled to WASM). This removes the need to have specific developers for specific platforms, reduces the size of your overall development team, and overall reduces development/maintenance costs.
+ You're guaranteed to have a large set of possible users, as a huge amount of people use the Internet daily.
+ There's no need to download any apps to start using them, as you can just access the webpage; having to download an app can put off certain users, so this prevents that.
+ If the app is designed with [SEO](https://simple.wikipedia.org/wiki/Search_engine_optimization) in mind, this can increase its prevalence in search results and increase its visibility.

There are drawbacks, as expected:
- You aren't able to deliver the same experience of the website in every browser, and some features might be missing on other browsers; this can prevent some users from being able to access the content of the page if they're on a non-compatible browser.
- Web apps are more likely to be less performant than their native app alternatives, due to relying on the browser to render the UI/communicating with the server; this can worsen the user's experience with the product, and make them more likely to exit the site.
- Not everyone would want to open their browser to access the website - not only is it a slower action than just opening an app already on their home screen, but they may also get distracted by other apps.
- Since the intended target is a phone, it might be difficult to develop a UI for a CYOA maker that also has all options clearly displayed; phones have a small screen, so it's difficult to account for enough space for the UI while also having adequate space to view the rest of the app.

Overall, I think that this platform would be a good idea as a secondary option/a funnel to the native app; while it provides a convenient (at least for the developer) place to host the app, it also is less performant and inconsistent based on the browser.\
I think it does have value as a way to funnel more users to the native app however - more people would encounter the product online, so encouraging the user to download the main app while providing a subset of the real experience could be vaild strategy; that isn't to say that it couldn't function as the main platform for the app, but I believe that it would be better suited with this purpose.\
It could also be useful as a way to play existing CYOAs which have been uploaded by other users, like a display of what the users have been able to achieve with the software; you could then funnel the user onto the main native app in order to be able to create CYOAs. I think that the web would be a suitable platform for playing through the games, as CYOAs tend to be pretty static - there usually isn't much in terms of animation/etc that would require a powerful platform to use. Creation would be better for the native app though, as the improved performance of the native app would make it easier to work in a larger story with more nodes/lines of code.

[^1]: It's a portable assembly format, used to run code developed in another language (e.g. C++, Rust) in the web. This makes it easier to develop websites, as you no longer need to solely use Javascript/HTML for website development.

## Other
Phone features could be an interesting option for the distribution of the product - they aren't suitable for CYOA creation, due to the how little information can be sent in each message. It'd be done through USSD (Unstructured Supplementary Service Data); this is a communication protocol still in use today, typically for things like balance checking, customer service and making transactions. The server can send basic messages to the client (limited to 140 characters), to which the client can send responses back; this makes it a good platform for simple, text-based CYOAs. There could be some difficulty in taking the higher level format of the CYOA maker output and transforming it into a format suitable for USSD though - it also only has support for text (and very little text at that), limiting the complexity of the story that can be told.\
It does present the advantage of being available on phones by default (requiring no external software), reducing the developer's workload and making it more convenient for the client to use; it also works with a session-based system, so it means that the client can receive the information in real-time.\
SMS presents a similar opportunity to USSD, both being text-based protocols; SMS does have a greater character limit at 160 and it utilises a 'store and forward' system (resulting in there being some latency when the message is sent), but it's pretty identical to USSD past that.

While it's far from the most powerful/extensive option, it wouldn't be a bad idea to experiment with simple CYOA distribution in this format; possibly as a extra feature for more dedicated customers.
