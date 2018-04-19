# hyperdb
[![crates.io version][1]][2] [![build status][3]][4]
[![downloads][5]][6] [![docs.rs docs][7]][8]

Distributed, scalable database. To be implemented.

- [Documentation][8]
- [Crates.io][2]

## Usage
```rust
extern crate hyperdb;

use std::path::PathBuf;

let location = PathBuf::from("./my.db");
let db = hyperdb::HyperDb::new(location);

db.put("/hello", b"world").unwrap();
let nodes = db.get("/hello").unwrap();
println!("/hello --> {}", nodes[0].value);
```

## Installation
```sh
$ cargo add hyperdb
```

## License
[MIT](./LICENSE-MIT) OR [Apache-2.0](./LICENSE-APACHE)

[1]: https://img.shields.io/crates/v/hyperdb.svg?style=flat-square
[2]: https://crates.io/crates/hyperdb
[3]: https://img.shields.io/travis/datrs/hyperdb.svg?style=flat-square
[4]: https://travis-ci.org/datrs/hyperdb
[5]: https://img.shields.io/crates/d/hyperdb.svg?style=flat-square
[6]: https://crates.io/crates/hyperdb
[7]: https://docs.rs/hyperdb/badge.svg
[8]: https://docs.rs/hyperdb
