# Programming Language Options
There are a variety of programming languages that could be used to create the CYOA product, and the platform that it's hosted on will impose some restrictions on which language could be used.

## Swift
Swift is a programming language developed by Apple, made to replace Objective-C[^1]; it attempts to combine influences from languages across all [paradigms](https://en.wikipedia.org/wiki/Programming_paradigm), such as [Haskell](https://www.haskell.org), [Python](https://www.python.org) and [C#](https://en.wikipedia.org/wiki/C_Sharp_(programming_language)).\
It's strongly typed[^2], and is compiled to LLVM (after a number of optimisations have been performed on the code); this makes the language quite fast. It has an IDE in the form of XCode and many community-developed tools to assist in the development process.
Use of this language isn't necessary to develop IOS apps, but it makes it much easier; you could use Objective-C, but it's older and slower - Swift was made to replace it, and does a much better job overall. Other languages can be used (e.g. Dart, C#, Javascript), but Swift's Objective-C compatibility (for legacy codebases) and support by Apple just makes it much easier to develop IOS apps.

I think that Swift would be a decent choice of language for the product, but purely if the task was to make an IOS app for the product; while it's a good language, it's outperformed by other languages when the topic isn't IOS development - for example, it has good memory safety but a language like Rust is just better in that regard.\
If the topic is IOS development, however, I think that it should be the first choice - Apple's extensive support for the language makes it the obvious choice for such a route. Swift is also a fairly popular language, so it wouldn't be too difficult to find developers who are highly competent at using it.

[^1]: This is a superset of the C programming language, making it more object-oriented than base C is.
[^2]: Simply put, variables of one type can be implicitly (no `cast` statement required) cast to another type.
