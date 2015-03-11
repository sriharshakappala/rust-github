# Rust Github

Rust based library for interacting with the Github API. This is just a practice library while I learn how to write Rust libraries / applications.

## Examples

### Get a user

This request will return a single `gitHub::users::User` struct.

```rust
extern crate github;

use github::Github;


fn main() {
    let github = Github::new();
    let user = github.users.get("octocat");
    println!("Name: {:?}", user.name);
    println!("Email: {:?}", user.email);
    println!("Location: {:?}", user.location);
}
```
