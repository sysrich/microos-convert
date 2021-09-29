# microos-convert

Converts existing openSUSE Tumbleweed (and maybe in the future Leap) machines to MicroOS

## Expected Features
* Evaluates existing system for viability of conversion
* Warns user this will be a disruptive change, with existing services needing configuration/reinstallation
* Proposes convertion to one of the following MicroOS system roles
  * MicroOS Container Host (Default for detected servers)
  * MicroOS
  * MicroOS Desktop GNOME (Default for detected desktops)
* Modifies btrfs filesystem configuration as necessary
* Installs transactional-update as necessary
* Modify snapper configuration
* Converts in a single transactional-update transaction
  * Removes all Tumbleweed/Leap patterns and packages
  * Installs appropriate MicroOS patterns and packages
  * Installs appropriate containers/flatpaks based on detection
* Support 'revert' of previously microos-convert'ed system
  * Rollback system to previous state
