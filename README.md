Wine Proton tkg wiki
Etienne Juvigny edited this page on Jan 19, 2023 · 2 revisions
Wine-tkg-git is a PKGBUILD for custom wine builds creation. It can also build clean plain wine or wine-staging.

CONFIGURATION
The customization takes place in config files.

The default config file is next to the PKGBUILD and called "customization.cfg". You can edit it directly or create your own modified copy in a custom path (~/config/frogminer/wine-tkg.cfg by default). You only need to add the options you want to customize. The missing ones will use the default settings found in customization.cfg.

If you want to use patches that aren't already provided by wine-tkg-git, you can add them to the wine-tkg-userpatches directory and follow the rules detailed HERE.

DEPENDENCIES
On Arch and other pacman distros, the wine-tkg-git PKGBUILD will resolve the required dependencies for you if you call makepkg with the -s argument. In case you're building proton-tkg and/or are missing dependencies (or do not want to use the PKGBUILD), in your customization.cfg (proton-tkg.cfg for proton-tkg) or external config file, set the following:

# Set to the distro of your choice to attempt dependency resolution. Valid options are "debuntu" (for debian, ubuntu and similar), "fedora" or "archlinux".
_nomakepkg_dep_resolution_distro="archlinux"
For Debian, Ubuntu and derivatives:

Debian based OSes have extremely poor multilib support, requiring a quirky workaround (which is handled in our build system)

!! note: Pop!_OS is the worst at this, and can't build lib32-wine in a multilib env currently. !!

!! Building on Ubuntu isn't recommended currently (unless in a VM/container) due to some broken cross dependencies !!

In your customization.cfg (proton-tkg.cfg for proton-tkg) or external config file, set the following:

# Set to the distro of your choice to attempt dependency resolution. Valid options are "debuntu" (for debian, ubuntu and similar), "fedora" or "archlinux".
_nomakepkg_dep_resolution_distro="debuntu"
For Fedora and derivatives:

In your customization.cfg (proton-tkg.cfg for proton-tkg) or external config file, set the following:

# Set to the distro of your choice to attempt dependency resolution. Valid options are "debuntu" (for debian, ubuntu and similar), "fedora" or "archlinux".
_nomakepkg_dep_resolution_distro="fedora"
Pages 1
Find a page…
Wine Proton tkg wiki
CONFIGURATION
DEPENDENCIES
Clone this wiki locally
https://github.com/Frogging-Family/wine-tkg-git.wiki.git
Footer
© 2025 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact
Manage cookies
