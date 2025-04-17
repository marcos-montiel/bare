# 🥩 Bare — The *Least Worst* Programming Language (fr fr)

Welcome to **Bare** — a weird little side project trying to answer:  
> *"What would a low-level, statically typed language look like if it prioritized clarity, predictability, and zero magic… but still wanted to be fun?"*

Bare is **simple** — not necessarily **easy**. It’s about **knowing exactly what your code does, where your data lives, and when things happen**. If that sounds like your jam, or you just wanna vibe with a language that says *nope* to garbage collectors and hidden control flow — you’re in the right place.

![Built with Zig (for now)](https://img.shields.io/badge/Built%20with-Zig-0c6ba0?logo=zig&logoColor=fff)
![Bare Project](https://img.shields.io/badge/Language-Bare-e91e63?logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHdpZHRoPSczMicgaGVpZ2h0PSczMic+PHJlY3Qgd2lkdGg9JzMyJyBoZWlnaHQ9JzMyJyBmaWxsPSIjZTkxZTYzIiByeD0nNCcvPjx0ZXh0IHg9JzE2JyB5PScyMScgZm9udC1zaXplPScxMScgZmlsbD0nI2ZmZicgdGV4dC1hbmNob3I9J21pZGRsZSc+Qg==)
![No Magic fr fr](https://img.shields.io/badge/No%20Magic-fr%20fr-4caf50?logo=42)
![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)

---

### **VIBE CHECK**:
"Clear code is good code, but *Bare* code is *better* code. No magic, no nonsense."

---

## ✨ Core Principles
- **Clarity over cleverness**  
- **No magic, no hidden rules, fr fr**  
- **Everything is explicit, even if it’s verbose**  
- **Memory management without GC or ownership complexity**
- **Compile-time code runs like normal code, just… at compile-time**
- **The syntax should tell you what happens under the hood**
- **Build your own “syntactic sugar” by design**

---

## 📚 The Language: Bare Basics

```bare
block Vec2 {
    x: i32,
    y: i32
}

func add(ref a: Vec2, ref b: Vec2) -> ref Vec2 {
    let result: ref Vec2 = alloc(Vec2)
    result.x = a.x + b.x
    result.y = a.y + b.y
    return result
}

import { print } from "std:log.br"
import { add } to add2D from "./src/math.br"

func main() {
    let a: ref Vec2n = alloc(Vec2)
    a.x = 5
    a.y = 10

    let b: ref Vec2 = alloc(Vec2)
    b.x = 3
    b.y = 7

    let c: ref Vec2 = add(a, b)
    print(c.x)
    print(c.y)

    free(a)
    free(b)
    free(c)
}
```

> ✅ **No stack/heap guesswork — you control where things live.**  
> ✅ **Imports are literal file paths, no magic.**  
> ✅ **Functions return refs? Then freeing memory is *your* job.**  
> ✅ **Compile-time execution? Just slap a `compiletime` keyword and it runs when you build.**  

---

## 📦 Bare Project Structure

```
my-app/
├── src/
│   ├── main.br
│   ├── math.br
├── lib/
│   └── libmath.bb
├── inc/
│   └── thirdparty/
│       └── coolstuff.br
├── build/
├── tests/
│   └── test_math.br
├── bare.toml
└── README.md
```

**Special Prefixes for Imports**
- `std:` → Standard library files  
- `inc:` → Included (non-compiled or 3rd-party) modules  
- `lib:` → Compiled `.bb` Bare Binary libraries  

Example:
```bare
import { add } to add2D from "lib:libmath.bb"
import { Vec2 } from "inc:thirdparty/coolstuff.br"
```

You can also import local code with a filepath with relative or full path:
```bare
import { Vec2 } from "/src/share/some/library/lib.bb"
import { cool } from "./inc/someother/library/you/dont/own.br"
    
```

---

## 🛠️ Toolchain

| Tool | Description |
|:------|:-----------------------------------|
| **`naked`** | The Bare compiler — turns `.br` files into executables or `.bb` libraries |
| **`rough`** | The Bare LSP — editor integration, type checking, error highlights |
| **`.bb`** | "Bare Binary" files — compiled libraries, your program's little "babies" |
| **`bare.toml`** | Project config file, dependency declarations |

---

## 💻 naked CLI Usage

```bash
# Build executable
naked build src/main.br -o build/my-app

# Build a library
naked build src/math.br --lib -o lib/libmath.bb

# Run directly
naked run src/main.br
```

---

## 🛠️ Bootstrapping: Why Zig?

We're building **`naked`** and **`rough`** in **Zig** for now because:
- No hidden memory allocations
- Compile-time execution
- Super portable, clean error handling
- Bare’s future compiler could borrow Zig's best ideas
- When Bare’s ready, we’ll rewrite everything in Bare (obviously 😎)

---

## 🤘 Why Does This Exist?
Because languages today follow too many old ideas without questioning them.  
**Bare isn’t here to replace anything.**  
It’s a thought experiment, a playground, a dare.  
A language where:
- You **see the cost** of everything.
- You **control memory** with clear syntax.
- You **build tools that respect you** by being honest.

If that sounds fun — hop in. If not, no worries. Either way: **brrrrr…**

---

## 🚧 Disclaimer
This language is experimental, pre-alpha, undefined, probably broken, and might go nowhere.  
But we’re vibin' anyway.

---

## 📎 Wanna Contribute?  
Go to [contributing](https://github.com/marcos-montiel/bare/blob/main/.github/CONTRIBUTING.md) and see what you can do! We like fresh and cool ideas.  

**Stay bare. Stay real.**
