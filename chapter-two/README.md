# The Surface

This is the part of the window that we draw to. We need it to draw directly
to the screen.
The `window` needs to implement the `HasRawWindowHandle` trait from the
`raw-window-handle` crate to create a surface.

## Instance and Adapter

The `Instance` is the first thing you create when using `wgpu`.
Its main purpose is to create `Adapter`'s and `Surface`'s.

### Adapter

The `Adapter` is a handle for the actual graphics card. You can use it
to get information about the graphics card, such as its name, and what 
backend adapter it uses.
We use it to create the `Device` and `Queue`.

## Device and Queue

Created from the `Adapter`.