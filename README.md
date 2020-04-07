# akvcam, Virtual camera driver for Linux  #

akvcam is a fully compliant V4L2 virtual camera driver for Linux.

## Modifications

This is a modified fork I've written of akvcam. One of the few but detrimental issues I've come across with akvcam is fluid streaming to the virtual device, as when akvcam isn't receiving frames at a perfect consistent rate, it shows an RGB static background which at my best efforts will show intermittently and indefinitely when writing to the device. This modified fork solves that by caching frames, meaning whenever akvcam isn't receiving a frame, it will use the last frame it did receive. This solves the issue and allows fluid and consistent streaming.
