# toml-query

Work with [toml-rs]() `Value` objects in an easy way:

```rust
value.read("foo.bar.a.b.c")                       // -> Result<Option<&Value>, Error>
value.set("foo.bar.a.b.c", Value::Integer(1))     // -> Result<Option<Value>, Error>
value.insert("foo.bar.a.b.c", Value::Integer(1))  // -> Result<Option<Value>, Error>
value.delete("foo.bar.a.b.c")                     // -> Result<Option<Value>, Error>
```

# Vacation notice

**Notice:** I, the author of toml-query, will be on vacation from mid-May 2018
until early 2019. I hope I can continue develop toml-query during that time, but I
cannot guarantee that. I hope I can continue development of toml-query after that
and I certainly plan to do so.

@TheNeikos as commit rights to this repository and will respond to issues and
PRs.

# Development

This library was developed using a Test-Driven-Development approach from the
ground up.

Goals:

* Nice, clean and human-readable error messages in the `Error` types
* Easy to use library

Non-Goals:

* High performance. TOML objects shouldn't be enormous. The library _may_ get
  faster at some point in time, but it is not a primary goal of the development.

# License

MPL 2.0
