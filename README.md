# Rust 🦀

## Usage

Build the image
```
docker build --tag rust/latest .
```

Create the container and mount the `$PWD` to the `tmp/` directory inside.
```
docker run --name rust -v `pwd`:/tmp -it rust/latest bash
```

Create the a new project inside the container
```
cargo new my_new_project
```

The `my_new_project` directory should be available on your host at `$PWD/my_new_project`.
