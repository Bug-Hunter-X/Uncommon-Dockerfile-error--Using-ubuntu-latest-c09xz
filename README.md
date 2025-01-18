# Uncommon Dockerfile Bug: Using `ubuntu:latest`

This example demonstrates a common yet easily overlooked issue in Dockerfiles: using the `ubuntu:latest` image.

While convenient, this approach introduces instability.  Future updates to the base image can unexpectedly break your Docker image, leading to build failures or runtime issues.

**Problem:** The `ubuntu:latest` tag points to the latest version of Ubuntu available. This means that building your image today will likely use a different base image than it will in a month, introducing potential incompatibilities.

**Solution:** Specify a precise version of Ubuntu to ensure consistent builds.  This avoids unexpected changes to your base image.