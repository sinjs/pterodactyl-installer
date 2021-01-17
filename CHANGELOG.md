# Changelog

This project follows the [semantic versioning](https://semver.org) convention. Changelog points should be divided into fixed, changed, or added.

## next-release

### Fixed

- [#135](https://github.com/vilhelmprytz/pterodactyl-installer/issues/135) panel/wings: Fixed so that the automatic ufw firewall configuration no longer requires confirming for the enable operation (user interaction after initial configuration is not intended behavior).

### Changed

- [#88](https://github.com/vilhelmprytz/pterodactyl-installer/issues/88) panel: Changed so that certbot now uses `certbot --nginx` over `certbot certonly` which makes it easier to perform certificate renewals later on (thanks [@Linux123123](https://github.com/Linux123123)).
- [#100](https://github.com/vilhelmprytz/pterodactyl-installer/pull/100) panel: Refactor several different functions in panel script, removal of redundant variables and functions and general cleanup/restructure (thanks [@Linux123123](https://github.com/Linux123123)).
- [#137](https://github.com/vilhelmprytz/pterodactyl-installer/issues/137) panel: Removed ability to run `p:environment:mail` script since it's redundant.
- [#139](https://github.com/vilhelmprytz/pterodactyl-installer/pull/139) wings: Refactor - replaced all `"$var"` with `[ "$var" == true ]` (thanks [@Linux123123](https://github.com/Linux123123)).

### Added

- [098d01a](https://github.com/vilhelmprytz/pterodactyl-installer/commit/098d01a9729dffaf40e80077da2d7d51b42a197b) panel: Add a prompt in `verify-fqdn` that requires user consent before performing HTTPS request against [https://checkip.pterodactyl-installer.se](https://checkip.pterodactyl-installer.se).

## v0.1.1 (released on 2021-01-01)

### Fixed

- [#133](https://github.com/vilhelmprytz/pterodactyl-installer/issues/133) panel: Fixed the `verify-fqdn.sh` so that it now installs the packages quietly. Panel script will now only execute the FQDN verification if `ASSUME_SSL` or `CONFIGURE_LETSENCRYPT` is true.

## v0.1.0 (released on 2021-01-01)

- Initial release, introduces versioning to the project