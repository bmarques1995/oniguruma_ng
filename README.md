# Oniguruma Next Gen (oniguruma_ng)

A modern continuation of the legendary **Oniguruma** regular expression engine.

Oniguruma_NG preserves the elegance, Unicode discipline, and expressive power of the original Oniguruma, while introducing modern build tooling, active maintenance, and a renewed development roadmap.

---

## What is Oniguruma_NG?

Oniguruma_NG is a **forward-looking, actively maintained** evolution of the original Oniguruma library created by **K. Kosako**.

The original repository is now archived and no longer accepting issues or patches, despite the engine still being widely used by language runtimes, libraries, and applications.

Oniguruma_NG continues the work.

---

## Legacy Acknowledgment

This project is based on the original **Oniguruma** ([https://github.com/kkos/oniguruma](https://github.com/kkos/oniguruma)), a masterpiece of regex engine design.

We preserve:

* its API
* its Unicode capabilities
* its matching behavior
* its philosophy

We extend and modernize it where necessary.

---

## Why This Fork Exists

The goals behind Oniguruma_NG are:

### Preserve a historically important regex engine

The original project is archived, but still depended upon by many systems. Oniguruma_NG ensures it does not fade away.

### Provide a modern, maintained version

Active development and patches continue to evolve the engine.

### Adopt modern tooling

We remove outdated build systems and move to **CMake-only**, improving portability and integration with modern environments.

### Improve safety and security

Include exploit analysis, fuzz testing, sanitizer builds, and security fixes.

### Support new languages and runtimes

Oniguruma_NG is ideal for embedders, scripting languages, and VM runtimes.

---

## Key Improvements Over the Original

* **CMake-based build system** (only)
* Cleaner and modernized repository structure
* Active issue tracking and patch acceptance
* Planned support for updated Unicode data
* Additional examples and documentation
* Ongoing security and exploit analysis
* CI and developer-focused improvements (sanitizers, fuzzers, tests)

---

## Building

```bash
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build
```

---

## Examples

Examples will be available under the `examples/` directory and will include:

* Basic matching
* Named captures
* Lookbehind and lookahead usage
* UTF-8 handling
* Reusable compiled patterns

---

## Security & Analysis

Oniguruma_NG will undergo:

* AddressSanitizer testing
* UndefinedBehaviorSanitizer
* MemorySanitizer
* Fuzz testing with libFuzzer
* Review of historical CVEs

Security issues are welcome and will be taken very seriously.

---

## Roadmap

* Update Unicode data
* Add configurable match timeouts or backtracking budgets
* Add more examples and tests
* Improve portability on modern toolchains
* Provide optional safer API wrappers

---

## Contributing

Issues and pull requests are welcome.

Whether it's bug fixes, performance improvements, Unicode support, documentation, or enhancements — your help builds the future of this engine. And i will appreciate a lot, as my first work on a regex engine.

---

## Credits

Original work by **K. Kosako** and contributors.

Oniguruma_NG is a tribute, continuation, and modernization of that extraordinary project. The last readme is available [here](./readme.goodbye.md)

---

## License

Licensed under the same license (BSD 2 Clauses) as the original Oniguruma, ensuring compatibility and continuity.

## Additional notes

As the features were implemented, this readme will be updated, showing the implementations.
