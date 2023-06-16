# An attempt to port a lite version of fsrs4Anki

Torch itself has so many not-used database. So port a lighter version may be easier to even integrate into the Anki.

To reduce the work amount, I choose to use the numpy. Since it's not so slow and "light weight"(compared to torch)

---

## Progress

- [ ] port backward (Maybe hard), Adam, etc.
- [ ] test polyfill generate by GPT (I doubt about them, but temporarily let them be there)
    test method: replace them one by one into the origin implementation.
- [ ] replace nn.Module (The hardest thing maybe)
- [ ] integrate into the Anki.

---

## Some considerations:

1. numpy itself is huge: 80M+!!(but it can be a dep, not necessarily bind to packages)
2. pandas is also huge: 90M+!!
3. but torch is way more huge than these two :), and think of this: It's now polyfill torch with numpy!
4. speed. But I trust numpy.(And maybe even <https://github.com/abetlen/ggml-python>)

---

## If use others, like Rust, C, Cpp

1. it's hard to integrate with current code.
2. hard to code.
