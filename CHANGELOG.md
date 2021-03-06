## 0.8.0 (unreleased)

### Bug fixes

* Pull request [#22](https://github.com/fnichol/chef-rvm/pull/22): Expand list of sane rubies to include `"ree"` and `"kiji"`. ([@juzzin][])
* Pull request [#26](https://github.com/fnichol/chef-rvm/pull/26): RVM is installed in compilation phase when gem_package recipe is included. ([@temujin9][], [@fnichol][])
* Update rvm/vagrant/system_chef_solo default attribute value to match newest Vagrant lucid32 basebox. ([@fnichol][])
* Pull request [#27](https://github.com/fnichol/chef-rvm/pull/27): Explicitly handle the unmanaged 'system' ruby. ([@temujin9][]).
* Pull request [#28](https://github.com/fnichol/chef-rvm/pull/28): Fix bug when no RVM rubies had yet been installed. ([@relistan][]).
* Pull request [#30](https://github.com/fnichol/chef-rvm/pull/30): Implement 'group_users' support. ([@phlipper][]).
* Update ruby compilation dependencies for debian/ubuntu. ([@fnichol][])

### New features

* Issue [#4](https://github.com/fnichol/chef-rvm/issues/4): Per-user RVM installs with support in all LWRPs. ([@fnichol][])
* Refactor system and user installs into: system_install, system, user_install, user ([reference](https://github.com/fnichol/chef-rvm/commit/69027cafbe8e25251a797f1dcf11e5bc4c96275b)). ([@fnichol][])
* Support Mac OS X platform for system-wide and per-user installs. ([@fnichol][])
* Issue [#23](https://github.com/fnichol/chef-rvm/issues/24): Let gem_package resource target multiple RVM rubies. ([@fnichol][])
* Pull request [#26](https://github.com/fnichol/chef-rvm/pull/26): Add new attribute `group_id`. ([@temujin9][])
* General refactoring and re-modularizing. ([@fnichol][])

### Improvments

* Pull request [#26](https://github.com/fnichol/chef-rvm/pull/26): RVM unix group is created in compilation phase if GID is provided. ([@temujin9][])
* Revamp CHANGELOG in the style of [guard](https://github.com/guard/guard). ([@fnichol][])
* Pull request [#27](https://github.com/fnichol/chef-rvm/pull/27): Improve gem_package logging message to include full list of selected rubies. ([@temujin9][])
* RVM gem installed using opscode cookbook conventions (via gem_package). ([@fnichol][])
* Add RVM::Shell::ChefWrapper based on chef's popen4 impl. ([@fnichol][])
* Create RVM::ChefUserEnvironment which can be injected with a user. ([@fnichol][])
* Normalize 'missing gem' logging notices. ([@fnichol][])
* Add Chef::RVM::StringCache to get and cache canonical RVM strings. ([@fnichol][])
* Modularize `libraries/helpers.rb` in modules. ([@fnichol][])


## 0.7.1 (May 15, 2011)

### Bug fixes

* Issue [#20](https://github.com/fnichol/chef-rvm/issues/20): Update metadata.rb to not include README.md (too long). ([@fnichol][])

### New features

* Add Rakefile for opscode platform deploy builds. ([@fnichol][])

### Improvments

* Update metadata.rb properties. ([@fnichol][])


## 0.7.0 (May 14, 2011)

### Bug fixes

* Issue [#20](https://github.com/fnichol/chef-rvm/issues/20): Update rvm/install_rubies attr to "true"/"false". ([@fnichol][])
* Issue [#14](https://github.com/fnichol/chef-rvm/issues/14): Allow no default RVM ruby (i.e. use system ruby). ([@fnichol][])
* Issue [#12](https://github.com/fnichol/chef-rvm/issues/12): Update RVM install to use SSL URL. ([@fnichol][])
* Now /etc/rvmrc has export for rvm/rvmrc key/value pairs. ([@fnichol][])

### New features

* Issue [#13](https://github.com/fnichol/chef-rvm/issues/13): Speed up install by disabling RDOC generation. ([@fnichol][])
* New experimental recipe gem_package which patches gem_package resource. ([@fnichol][])
* Add rvm_global_gem resource. ([@fnichol][])

### Improvments

* Issue [#3](https://github.com/fnichol/chef-rvm/issues/3): Revamp and update README.md. ([@fnichol][])
* Issue [#3](https://github.com/fnichol/chef-rvm/issues/5): Add CHANGELOG.md. ([@fnichol][])
* Issue [#19](https://github.com/fnichol/chef-rvm/issues/19): Attr rvm/upgrade accepts "none", false and nil as same value. ([@fnichol][])
* Update rvm/skip_docs_on_install attr to rvm/rvm_gem_options. ([@fnichol][])
* Refactor of rvm_gem provider to leverage Chef::Provider::Package::Rubygems. ([@fnichol][])


## Previous releases

The changelog began with version 0.6.0 so any changes prior to that can be
seen by checking the tagged releases and reading git commit messages.

[@fnichol]: https://github.com/fnichol
[@juzzin]: https://github.com/juzzin
[@phlipper]: https://github.com/phlipper
[@relistan]: https://github.com/relistan
[@temujin9]: https://github.com/temujin9
