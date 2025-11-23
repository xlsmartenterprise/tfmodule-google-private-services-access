# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [v1.0.0] - 2025-11-23

### Added
- Initial release of the Private Service Access module
- Global IP address reservation for VPC peering with Google-managed services
- Service Networking Connection for private access to managed services
- Support for custom IP address range allocation
- Configurable prefix length for reserved IP ranges
- Support for both IPv4 and IPv6 address versions
- Configurable deletion policy (ABANDON option for safe resource cleanup)
- Dependency management using null_resource for ordered resource creation

### Outputs
- `address` - First IP of the reserved range
- `google_compute_global_address_name` - Name of the reserved range
- `peering_completed` - Dependency output for enforcing resource creation order

### Requirements
- Terraform >= 1.5.0
- Google Provider >= 7.0.0, < 8.0.0
- Google-Beta Provider >= 7.0.0, < 8.0.0