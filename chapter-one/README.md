# The Window

In this Chapter, we went over how to use `winit` to create a window
in both native and web-assembly.

## Dependencies

```toml
[dependencies]
anyhow = "1.0"
winit = { version = "0.30", features = ["android-native-activity"] }
env_logger = "0.10"
log = "0.4"
wgpu = "28.0"
pollster = "0.3"
```

### Env Logger

We enabled logging via the `env_logger` crate. This is because when wgpu
encounters an error, it panics with a generic error, while logging the
real error via the `log` crate. So failute to initialise loggin using
`env_logger::init()` means wgpu will fail silently, leaving one confused.