# minigrep-rs
A less jacked version of [`grep`](https://en.wikipedia.org/wiki/Grep) written in Rust! Follows [chapter 10](https://doc.rust-lang.org/stable/book/ch12-00-an-io-project.html) of The Rust Book.

## Notes
- Guideline for splitting the separate concerns of a binary program when `main` starts getting large:
    - Split your program into a `main.rs` and a `lib.rs` and move your program’s logic to `lib.rs`.
    - As long as your command line parsing logic is small, it can remain in `main.rs`.
    - When the command line parsing logic starts getting complicated, extract it from `main.rs` and move it to `lib.rs`.

Because you can’t test the main function directly, this structure lets you test all of your program’s logic by moving it into functions in lib.rs

-  Call to `panic!` is more appropriate for a programming problem than a usage problem