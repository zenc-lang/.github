<div align="center">

## **Modern Ergonomics. Zero Overhead. Pure C.**

[![Sponsor](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86)](https://github.com/sponsors/Zuhaitz-dev) [![Discord](https://img.shields.io/discord/1460350343966887970?label=Discord&logo=discord&color=5865F2)](https://discord.com/invite/q6wEsCmkJP) [![Website](https://img.shields.io/badge/Website-zenc--lang.org-blue)](https://zenc-lang.org)

</div>

---

## Welcome to the Zen C Ecosystem

**Zen C** is a modern, compiled systems programming language that seamlessly extends C11. It is designed for developers who love the raw performance and ubiquity of C, but want the modern ergonomics of languages like Rust, Go, or Swift.

Zen C is not just a wrapper; it is a full language toolchain that compiles down to clean, human-readable standard C. 

### Why Zen C?

* **Modern Ergonomics:** First-class support for Type Inference (`let`), Pattern Matching (`match`), Traits (`impl`), and Operator Overloading.
* **Native Interoperability:** Zero-cost bindings to C. Seamlessly compile to C++ to use `<vector>` or OpenCV, write CUDA GPU kernels directly in Zen C syntax, or use Objective-C linkage for macOS apps.
* **Pragmatic Memory Safety:** Manual memory management made safe with `defer`, `autofree`, and strict **Move Semantics** by default. No heavy runtime, no garbage collector.
* **Universal Binaries:** Native support for compiling to **APE** (Actually Portable Executable)—build once, run anywhere.

```zc
import "std/vec.zc"
import "std/net.zc"

struct User { id: int; name: string; }

async fn fetch_user(id: int) -> User {
    // Async/Await syntax built on native pthreads/coroutines
    return User{id: id, name: "Alice"};
}

fn main() {
    let users = Vec<User>::new();
    
    match fetch_user(101) |> await {
        User(id, name) => println "Got user: {name}", // Pattern destructuring
        _              => println "Failed"
    }
}
```

---

## Organization Directory

Zen C is a growing ecosystem. Navigate our core repositories here:

| Repository | Description | Status |
| :--- | :--- | :--- |
| **[zenc](https://github.com/zenc-lang/zenc)** | The core Zen C compiler (`zc`), CLI, and Standard Library. | Active Development |
| **[docs](https://github.com/zenc-lang/docs)** | The official documentation and language specification. | Active |
| **[rfcs](https://github.com/zenc-lang/rfcs)** | The Request for Comments (RFC) repository. Shape the future of the language. | Active |
| **[vscode-zenc](https://github.com/zenc-lang/vscode-zenc)** | Official VS Code extension (Syntax Highlighting, Snippets). | Alpha |
| **[www](https://github.com/zenc-lang/www)** | Source code for `zenc-lang.org`. | Active |
| **[awesome-zenc](https://github.com/zenc-lang/awesome-zenc)** | A curated list of awesome Zen C examples | Growing |

---

<div align="center">



## Meet Zibi

<img src="https://raw.githubusercontent.com/zenc-lang/.github/main/profile/zibi.svg" width="180" alt="Zibi the Ogre">

<br>

**Zibi is the tiny green ogre that guards your memory.**
<br>
He started life as a random GitHub identicon, reminded us of an ogre, and became our official mascot. 

| **Zibi Likes** | **Zibi Hates** |
| :--- | :--- |
| **Zen C** (obviously) | `void*` casting |
| Move Semantics | Segfaults |
| Stack allocation | Garbage Collection pauses |
| Onions (layers!) | Complex build scripts |

<br>
<i>If your code compiles and runs on the first try, Zibi is happy.</i>

</div>

---

## Join the Community

We are actively looking for contributors! Whether you want to write compiler optimizations, build standard library features, write documentation, or create tutorials, there is a place for you here.

* **[Read the Contributing Guide](https://github.com/zenc-lang/zenc/blob/main/CONTRIBUTING.md)**
* **[Join the Discord](https://discord.com/invite/q6wEsCmkJP)**
* **[Sponsor the Core Team](https://github.com/sponsors/Zuhaitz-dev)**
