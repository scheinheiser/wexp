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
It works much differently compared to Twine, being based on an extensive scripting language called ink; they also have created multiple tools to make it easier to work with ink, such as [inklewriter](https://www.inklestudios.com/inklewriter/) and Inky (a code editor, which provides error highlighting/hot reloading/etc).

The software is intended for easy integration with existing games, and is made for creating text-based CYOAs - it does, however, provide support for web-based stories.\
You can compile the `.ink` scripts to `.js` files, which can be hosted by the user so clients can access it online.\
They also provide some web-specific functionality - you can include inline images, and they also allow for CSS interoperability (which gives you the ability to add extra styling to certain elements); this gives the user more customisability over what their stories look like.

## [ChoiceScript](https://www.choiceofgames.com/make-your-own-games/choicescript-intro/)
This software is relatively niche, but it still has facilitated the creation of some impressive software.\
It works similarly to Ink, with a big scripting language at its core; this gives the user the power to create complex and extensive stories. It does lack the ecosystem of Ink though, as it doesn't have tooling similar to inklewriter or Inky.\
The language can be compiled to HTML, which does make it web-compatible - they also give you the ability to insert images, making it good for less text-heavy stories.

ChoiceScript has support for basic control flow (like `if` statements), but also provides support for more powerful statements like `goto` and `label`; they also allow the user to define their own mutable variables, and provide support for string interpolation. Overall, it gives the user more than enough to make complex stories that track the user's decisions throughout.

## [Ren'Py](https://www.renpy.org)
Ren'Py has been used to make some very successful games in the past, such as [Slay the Princess](https://store.steampowered.com/app/1989270/Slay_the_Princess__The_Pristine_Cut/) - though it's made to create visual novels, CYOAs have many similarities with such a medium.

The software, similar to ChoiceScript, only provides a scripting language for the user to work with - they chose to model it around being similar to Python, making it easy to approach for beginners. The developers of the software also built GUI customisation into the language, as every game requires a GUI to interact with adventure, giving the maker further customisation over their game.\
The language itself is even more extensive compared to ChoiceScript and Ink, providing even more control flow - it also supports manual management of the screen, camera and current scene to allow for more animated games. As expected, it provides support for images in the language as well.

Ren'Py can be compiled to run on the web as well, allowing it be hosted and embedded into a web page.

## [Inform 7](https://ganelson.github.io/inform-website/index.html)
Like most of the software listed here, Inform 7 works with a scripting language being used to build up a rich story. This product, unlike the others, uses more natural language for the scripting language; statements such as:
```
The Cobble Crawl is a room. "You are crawling over cobbles in a low passage. There is a dim light at the east end of the passage."
```
and
```
Above the Debris Room is the Sloping E/W Canyon. West of the Canyon is the Orange River Chamber.
```
would be valid syntax. This makes it a bit easier to approach story creation, as it sticks quite closely to phrases that you might commonly use.\
Past this, tooling is limited; it lacks a GUI like Twine, or a code editor like Inky. It does have easy web interop though, requiring just a short phrase (`Release along with an interpreter.`) to be able to publish it to a website, making it easy to embed your games into a webpage.

------

The most important aspects to include, I believe, would be a scripting language[^2] along with some web interoperability; at the very least, this allows the user to make their stories and embed them into websites, making it easier to publish games onto sites like [itch](https://itch.io).\
I think that having a code editor would be a good addition on top of this, as it'd allow you to provide features to help development in the language moreso than a generic code editor. It's far from necessary though, as plugins could be developed for existing editors.\
A debugger/tester would be a necessary feature - while manual testing/helpful error messages would serve most user's needs, there would be situations where inspection of the code might not be enough. Having access to the state all variables in the program at any point would be a very useful feature, especially as codebases increase in size.

If you'd want to go down a more GUI-based route, I think that it would be good to try and guide the users more; while Twine's GUI is nice, I think that it is a bit hard to approach. There are adequate tutorials online, but I think that the software should be able to give the user enough information to be able to confidently use it (at least for basic features).

Finally, I think that it'd be a very good idea to have a pane to view/interact with the story as you make updates to the program, similar to Ink's editor Inky. This would make it easier to work on the story, as you'd be able to test each segment as you go on and make changes as needed.

[^2]: Regarding the implementation of the language, I think that it would be best to take a mix of Inform and Ink/ChoiceScript's approach; while natural language makes it easier to approach for the user, it also makes it more difficult to parse the source code.
