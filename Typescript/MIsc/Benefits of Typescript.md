# Benefits of Typescript

An answer by user [DeUsuahiaALaQuiacc](https://www.reddit.com/user/DeUsuahiaALaQuiaca/)to a post on Reddit about [justifying the introduction of Typescript to a team]([https://www.reddit.com/r/learnjavascript/comments/sdfgh7/checkmate_by_kyle_simpson/](https://www.reddit.com/r/learnjavascript/comments/sdfgh7/checkmate_by_kyle_simpson/)).

---

The problem with this quote is that Kyle is implying the only benefit of TypeScript is to provide linting for bugs strictly related to types.  
  
The fact is that the benefits of TypeScript are much deeper than that. TS gives your editor a better ability to statically analyze your code, to provide better tools and DX. At the same time, TS lets you communicate the intent of your code to other developers (including yourself 6 months later) with a formal syntax that helps with discoverability.  
  
It's not fair to say that TypeScript is just "type-aware linting". Here are some things I regularly take advantage of while writing TS code:-  
  
- Accurate intellisense / code suggestions
- Jump to definition
- Type hints on hover
- Docblock hints on hover
- Refactor > Rename Symbol intelligently across an entire project  
- Show Call Hierarchy intelligently across an entire project
- Compile-time errors when an interface (first or third party) changes and is now being used incorrectly somewhere. This is sort of related to "type-based linting", except I think it's a different case that Kyle isn't considering.  
  
Many of these IDE features are available in vanilla JS code as well (often thanks to the TypeScript engine that's powering them in editors like VSCode). But they all work better and in more places for TypeScript code. They provide a much better developer experience than you'll get without them, without even considering the linting aspect.  
  
Thanks to intellisense, jump to definition, and type hints / documentation on hover, I rarely have to look at the documentation for many third party dependencies. TypeScript just makes it discoverable right from my editor.