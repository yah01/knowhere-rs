# knowhere-rs
Rust port of Knowhere

## Generate
Compile Knowhere with Release mode first:
```shell
mkdir build && cd build
conan install .. --build=missing -o with_ut=True -s compiler.libcxx=libstdc++11 -s build_type=Release
conan build ..
``` 

This generates the Knowhere shared library to `knowhere/build/Release`, so the bindgen could find it.

Then run `cargo build` to generate the bindings at `src/knowhere.rs`