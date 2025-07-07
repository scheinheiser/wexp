# Competition

There's currently a decent amount of existing CYOA software, with a variety of online and free tools.

## [Twine](https://twinery.org)
The most popular/mentioned platform is Twine, which runs on both the browser and desktop.\
It provides users a GUI where they can make and edit nodes, allowing them to slowly build up a story.

Each node can be labelled, and text can be written inside; alongside some text alignment/size/colour manipulation settings, they also offer a macro-based system. It acts similar to a limited scripting language, where you can accept user input, use mutable variables, and have access to very basic control flow[^1].\
They also allow you to embed HTML into the passage.

Twine also offers a builtin story tester and debugger, which allows you to keep track of all of your variables, deactivate certain macros, and more.

[^1]: It only consists of `if` statements, and you can only obscure/show text with the effect; they do provide a variety of conditions though.

## [Ink](https://www.inklestudios.com/ink/)
Ink is less popular than Twine, but still mentioned quite frequently.\
It works much differently compared to Twine, being based on an extensive scripting language called ink; they also have created multiple tools to make it easier to work with ink, such as [inklewriter](https://www.inklestudios.com/inklewriter/) and inky (a code editor, which provides error highlighting/hot reloading/etc).

The software is intended for easy integration with existing games, and is made for creating text-based CYOAs - it does, however, provide support for web-based stories.\
You can compile the `.ink` scripts to `.js` files, which can be hosted by the user so clients can access it online.\
They also provide some web-specific functionality - you can include inline images, and they also allow for CSS interoperability (which gives you the ability to add extra styling to certain elements); this gives the user more customisability over what their stories look like.

## [ChoiceScript](https://www.choiceofgames.com/make-your-own-games/choicescript-intro/)
This software is relatively niche, but it still has facilitated the creation of some impressive software.\
It works similarly to Ink, with a big scripting language at its core; this gives the user the power to create complex and extensive stories. It does lack the ecosystem of Ink though, as it doesn't have tooling similar to inklewriter or inky.\
The language can be compiled to HTML, which does make it web-compatible - they also give you the ability to insert images, making it good for less text-heavy stories.

ChoiceScript has support for basic control flow (like `if` statements), but also provides support for more powerful statements like `goto` and `label`; they also allow the user to define their own mutable variables, and provide support for string interpolation. Overall, it gives the user more than enough to make complex stories that track the user's decisions throughout.

## [Ren'Py](https://www.renpy.org)
Ren'Py has been used to make some very successful games in the past, such as [Slay the Princess](https://store.steampowered.com/app/1989270/Slay_the_Princess__The_Pristine_Cut/) - though it's made to create visual novels, CYOAs have many similarities with such a medium.

The software, similar to ChoiceScript, only provides a scripting language for the user to work with - they chose to model it around being similar to Python, making it easy to approach for beginners. The developers of the software also built GUI customisation into the language, as every game requires a GUI to interact with adventure, giving the maker further customisation over their game.\
The language itself is even more extensive compared to ChoiceScript and Ink, providing even more control flow - it also supports manual management of the screen, camera and current scene to allow for more animated games. As expected, it provides support for images in the language as well.

Ren'Py can be compiled to run on the web as well, allowing it be hosted and embedded into a web page.
