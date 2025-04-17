# 🗺️ Bare Language Roadmap

This is what we’re thinking right now. It can (and will) change as we vibe.

---

## 🟢 Phase 1 — “brrrrr…”
- [x] Language spec v0.1 (core concepts, blocks, functions, imports)
- [x] `naked` compiler prototype (Zig)
- [x] Compile executables and `.bb` libraries
- [x] `bare.toml` project config
- [x] Import system with `std:`, `inc:`, `lib:` prefixes
- [x] Memory model spec (no GC, no ownership rules, no magic)
- [ ] Basic LSP support (`rough` prototype)

---

## 🟡 Phase 2 — “slightly less bare”
- [ ] Compile-time `compiletime` keyword execution
- [ ] Type system improvements
- [ ] Array and string support
- [ ] Custom syntactic sugar using blocks + compile-time code
- [ ] Unit test system (`bare test`)
- [ ] `naked link` for linking multiple binaries
- [ ] Error reporting polish

---

## 🟠 Phase 3 — “baby’s first stdlib”
- [ ] Minimal standard library (`std:core`)
- [ ] Basic math, strings, files, memory utilities
- [ ] `.bb` library format stabilization
- [ ] Prebuilt libs in `lib:`
- [ ] Package manager concept (`bare.toml` deps)

---

## 🔵 Phase 4 — “Bare 1.0 beta”
- [ ] Rewriting compiler in Bare (bootstrapping)
- [ ] Replace Zig compiler
- [ ] Fully self-hosted compiler build
- [ ] Docs + tutorials
- [ ] LSP polish (`rough` 1.0)
- [ ] Open pre-release to wider public

---

**Optional wild ideas**
- [ ] Bare WebAssembly target
- [ ] Bare VM sandbox mode
- [ ] Embeddable Bare runtime in other apps

---

**Vibe First. Ship Weird Stuff.**
