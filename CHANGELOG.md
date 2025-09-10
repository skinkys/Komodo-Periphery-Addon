# Changelog

All notable changes to this Home Assistant Add-on will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.18.5] - 2025-09-10

### Fixed
- Ensure architecture-specific s6-overlay binaries are used so the add-on runs on ARM64 systems.

## [1.18.4] - 2025-08-09

### Added
- Initial release of Komodo Periphery Home Assistant Add-on
- Support for Komodo Periphery v1.18.4
- Docker container management capabilities
- Core connection mode for connecting to remote Komodo Core servers
- Standalone mode with passkey authentication
- Container statistics monitoring
- Stack, repository, and build directory management
- SSL/TLS support
- Native Docker integration with docker.io package
- s6-overlay service management
- Comprehensive configuration options
- Health checks and monitoring
- Support for multiple architectures (amd64, aarch64)

### Features
- **Docker Integration**: Full Docker container lifecycle management
- **Core Connectivity**: Seamless WebSocket connection to Komodo Core servers
- **Authentication**: Passkey-based security for standalone operation
- **Monitoring**: Configurable intervals for system and container monitoring
- **Repository Management**: Git repository integration for builds
- **Stack Deployment**: Docker Compose stack management
- **Terminal Access**: Container exec and terminal functionality
- **SSL Support**: Optional encryption for secure communications

### Technical
- Debian bookworm-slim base image for native glibc compatibility
- Multi-stage Docker build for optimal image size
- bashio integration for Home Assistant Add-on standards
- Comprehensive logging and error handling
- Configurable time intervals with proper validation
- Empty passkey array support for core connection mode

### Configuration
- `core_url`: WebSocket URL for Core server connection
- `passkey`: Authentication key for standalone mode
- `monitoring_interval`: System monitoring frequency
- `container_stats_interval`: Container statistics collection frequency
- `ssl_enabled`: SSL/TLS encryption toggle
- `stack_directory`: Docker Compose stack storage location
- `repo_directory`: Git repository storage location  
- `build_directory`: Docker build context location
- `disable_terminals`: Terminal access control
- `disable_container_exec`: Container exec control
