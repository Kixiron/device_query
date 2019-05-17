# device_query

[![Build Status](https://travis-ci.org/ostrosco/device_query.svg?branch=master)](https://travis-ci.org/ostrosco/device_query)

A simple library to query mouse and keyboard inputs on demand without a window. Will work in Windows and Linux.

```Rust
use device_query::{DeviceQuery, DeviceState, MouseState, KeyCode};

let device_state = DeviceState::new();

let mouse: MouseState = device_state.get_mouse();
println!("Current Mouse Coordinates: {:?}", mouse.coords);

let keys: Vec<KeyCode> = device_state.get_keys();
println!("Is A pressed? {}", keys.contains(KeyCode::A));
```
