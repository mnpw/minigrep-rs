# minigrep-rs
A less jacked version of [`grep`](https://en.wikipedia.org/wiki/Grep) written in Rust! Follows [chapter 10](https://doc.rust-lang.org/stable/book/ch12-00-an-io-project.html) of The Rust Book.

## Notes
- Guideline for splitting the separate concerns (see more [here](https://youtu.be/6sNmJtoKDCo?t=1121)) of a binary program when `main` starts getting large: 
    - Split your program into a _main.rs_ and a _lib.rs_ and move your program’s logic to _lib.rs_.
    - As long as your command line parsing logic is small, it can remain in _main.rs_.
    - When the command line parsing logic starts getting complicated, extract it from _main.rs_ and move it to _lib.rs_.
- Call to `panic!` is more appropriate for a programming problem than a usage problem.
