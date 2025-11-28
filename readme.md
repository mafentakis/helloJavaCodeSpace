# Hello Java Codespace

This repository demonstrates a bare minimum Java project configured for use with a Dev Container. There is no custom Dockerfile or direct Docker setup involved—everything is driven by the `devcontainer.json` file that points to the Microsoft-provided Java image.

## What is a Dev Container?
A Dev Container defines a reproducible development environment that editors like VS Code can automatically create for you. By sharing the Dev Container configuration, collaborators get the same toolchain (Java 21 and Gradle in this case) without manual setup.

### How is this different from containers or Docker?
- **Dev Container**: A set of configuration files (such as `.devcontainer/devcontainer.json`) that describe the tools, SDKs, and editor settings your IDE should provision for development.
- **Container**: The runtime unit created from an image that actually runs your tools and code. Dev Containers instruct your editor to build or pull an image and start a container for you.
- **Docker**: A popular container engine/CLI used to build images and run containers. Dev Containers can run on Docker, but they can also run on other compatible runtimes supported by the Dev Container specification.

### Learn more
- Dev Containers overview: https://code.visualstudio.com/docs/devcontainers/containers
- Dev Container specification: https://containers.dev/
- VS Code Dev Containers FAQ: https://code.visualstudio.com/docs/devcontainers/faq

## Project contents
- `src/main/java/HelloWorld.java`: Simple "Hello, world!" application.
- `build.gradle` and `settings.gradle`: Minimal Gradle configuration using Java 21 and the application plugin.
- `.devcontainer/devcontainer.json`: Points to the Java 21 image and recommends VS Code extensions.

## Running locally
With Gradle available, you can run the sample app using:

```bash
gradle run
```

The Dev Container configuration installs Gradle for you inside the container so the command works without additional setup.
