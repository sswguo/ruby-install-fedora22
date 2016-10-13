# ruby-install-fedora22

## Install ruby via ansible (Recommended)
[Ruby Installer Playbook](https://github.com/WellsG/centos7-ansible/blob/master/ansible-sample/playbooks/rvm.yml)


## Install RVM (Ruby Version Manager)
```
[~] $ gpg2 --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
[~] curl -sSL https://get.rvm.io | bash -s stableE3
```
```
In case of problems: https://rvm.io/help and https://twitter.com/rvm_io

  * WARNING: You have '~/.profile' file, you might want to load it,
    to do that add the following line to '/home/wguo/.bash_profile':

      source ~/.profile

[~] $ source ~/.profile
[~] $ source /etc/profile.d/rvm.sh
[~] $ rvm requirements
Checking requirements for fedora.
Installing requirements for fedora.
Installing required packages: libyaml-devel, autoconf, gcc-c++, readline-devel, libffi-devel, automake, libtool, bison...........
Requirements installation successful.
[~] $ rvm list known
# MRI Rubies
[ruby-]1.8.6[-p420]
[ruby-]1.8.7[-head] # security released on head
[ruby-]1.9.1[-p431]
[ruby-]1.9.2[-p330]
[ruby-]1.9.3[-p551]
[ruby-]2.0.0[-p648]
[ruby-]2.1[.8]
[ruby-]2.2[.4]
[ruby-]2.3[.0]
[ruby-]2.2-head
ruby-head
```

## Install Ruby via RVM
```
[~] $ rvm install 2.2.4
Searching for binary rubies, this might take some time.
No binary rubies available for: fedora/22/x86_64/ruby-2.2.4.
Continuing with compilation. Please read 'rvm help mount' to get more information on binary rubies.
Checking requirements for fedora.
Requirements installation successful.
Installing Ruby from source to: /home/wguo/.rvm/rubies/ruby-2.2.4, this may take a while depending on your cpu(s)...
ruby-2.2.4 - #downloading ruby-2.2.4, this may take a while depending on your connection...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 12.7M  100 12.7M    0     0   639k      0  0:00:20  0:00:20 --:--:-- 1591k
ruby-2.2.4 - #extracting ruby-2.2.4 to /home/wguo/.rvm/src/ruby-2.2.4....
ruby-2.2.4 - #applying patch /home/wguo/.rvm/patches/ruby/2.2.4/fix_installing_bundled_gems.patch.
ruby-2.2.4 - #configuring.........................................................
ruby-2.2.4 - #post-configuration..
ruby-2.2.4 - #compiling................................................................................
ruby-2.2.4 - #installing..................
ruby-2.2.4 - #making binaries executable..
ruby-2.2.4 - #downloading rubygems-2.4.8
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   154  100   154    0     0    167      0 --:--:-- --:--:-- --:--:--   167
100  437k  100  437k    0     0   288k      0  0:00:01  0:00:01 --:--:-- 5908k
ruby-2.2.4 - #extracting rubygems-2.4.8....
ruby-2.2.4 - #removing old rubygems.........
ruby-2.2.4 - #installing rubygems-2.4.8......................
ruby-2.2.4 - #gemset created /home/wguo/.rvm/gems/ruby-2.2.4@global
ruby-2.2.4 - #importing gemset /home/wguo/.rvm/gemsets/global.gems...............................................
ruby-2.2.4 - #generating global wrappers........
ruby-2.2.4 - #gemset created /home/wguo/.rvm/gems/ruby-2.2.4
ruby-2.2.4 - #importing gemsetfile /home/wguo/.rvm/gemsets/default.gems evaluated to empty gem list
ruby-2.2.4 - #generating default wrappers........
ruby-2.2.4 - #adjusting #shebangs for (gem irb erb ri rdoc testrb rake).
Install of ruby-2.2.4 - #complete 
Please be aware that you just installed a ruby that requires 1 patches just to be compiled on an up to date linux system.
This may have known and unaccounted for security vulnerabilities.
Please consider upgrading to ruby-2.3.0 which will have all of the latest security patches.
Ruby was built without documentation, to build it run: rvm docs generate-ri
```

## Install Rails via gem
```
[~] $ gem install rails
```

## Gem env
```
[~] $ gem env
RubyGems Environment:
  - RUBYGEMS VERSION: 2.4.8
  - RUBY VERSION: 2.2.4 (2015-12-16 patchlevel 230) [x86_64-linux]
  - INSTALLATION DIRECTORY: /home/wguo/.rvm/gems/ruby-2.2.4
  - RUBY EXECUTABLE: /home/wguo/.rvm/rubies/ruby-2.2.4/bin/ruby
  - EXECUTABLE DIRECTORY: /home/wguo/.rvm/gems/ruby-2.2.4/bin
  - SPEC CACHE DIRECTORY: /home/wguo/.gem/specs
  - SYSTEM CONFIGURATION DIRECTORY: /home/wguo/.rvm/rubies/ruby-2.2.4/etc
  - RUBYGEMS PLATFORMS:
    - ruby
    - x86_64-linux
  - GEM PATHS:
     - /home/wguo/.rvm/gems/ruby-2.2.4
     - /home/wguo/.rvm/gems/ruby-2.2.4@global
  - GEM CONFIGURATION:
     - :update_sources => true
     - :verbose => true
     - :backtrace => false
     - :bulk_threshold => 1000
  - REMOTE SOURCES:
     - https://rubygems.org/
  - SHELL PATH:
     - /home/wguo/.rvm/gems/ruby-2.2.4/bin
     - /home/wguo/.rvm/gems/ruby-2.2.4@global/bin
     - /home/wguo/.rvm/rubies/ruby-2.2.4/bin
     - /home/wguo/.rvm/bin
     - /home/wguo/perl5/bin
     - /home/wguo/perl5/bin
     - /usr/lib64/qt-3.3/bin
     - /usr/kerberos/sbin
     - /usr/kerberos/bin
     - /usr/local/go/bin
     - /usr/lib/jvm/java-1.7.0-openjdk/bin
     - /usr/local/bin
     - /usr/local/sbin
     - /usr/bin
     - /usr/sbin
     - /bin
     - /sbin
     - /home/wguo/.local/bin
     - /home/wguo/bin
     - /home/wguo/gowork/bin
```

## Test Rails

- Create new app blog
```
[~/rbworkspace] $  rails new blog
```
- Start rails server
```
[~/rbworkspace/blog] $ rails server
Could not find rake-11.2.2 in any of the sources
Run `bundle install` to install missing gems.
```
It will show the missing gems error, and then run "bundle install":
```
[~/rbworkspace/blog] $ bundle install
```
Then start rails server again. It should works!


### Ref:
http://www.itzgeek.com/how-tos/linux/centos-how-tos/install-ruby-on-rails-on-ubuntu-centos-fedora-using-rvm.html
http://guides.ruby-china.org/getting_started.html

### Issue #1:
When exec the following cmd:
gem pristine --all

```
Fetching: fog-brightbox-0.0.2.gem (100%)
ERROR:  While executing gem ... (Gem::FilePermissionError)
    You don't have write permissions for the /usr/share/gems directory.
```

```
Cached gem for json-1.8.3 not found, attempting to fetch...
Fetching: json-1.8.3.gem (100%)
Building native extensions.  This could take a while...
ERROR:  While executing gem ... (Errno::EACCES)
    Permission denied @ rb_sysopen - /usr/lib64/gems/ruby/json-1.8.3/gem_make.out
```

### Solution:
1:  gem install json -v 1.8.3 

### Issue #2:  
```
[~/rbworkspace/blog] $ gem install ruby-libvirt -v 0.4.0
Fetching: ruby-libvirt-0.4.0.gem (100%)
Building native extensions.  This could take a while...
ERROR:  Error installing ruby-libvirt:
	ERROR: Failed to build gem native extension.

    /usr/bin/ruby -r ./siteconf20160830-2595-1p070tc.rb extconf.rb
*** extconf.rb failed ***
Could not create Makefile due to some reason, probably lack of necessary
libraries and/or headers.  Check the mkmf.log file for more details.  You may
need configuration options.

Provided configuration options:
	--with-opt-dir
	--without-opt-dir
	--with-opt-include
	--without-opt-include=${opt-dir}/include
	--with-opt-lib
	--without-opt-lib=${opt-dir}/lib64
	--with-make-prog
	--without-make-prog
	--srcdir=.
	--curdir
	--ruby=/usr/bin/$(RUBY_BASE_NAME)
	--with-libvirt-include
	--without-libvirt-include
	--with-libvirt-lib
	--without-libvirt-lib
	--with-libvirt-config
	--without-libvirt-config
	--with-pkg-config
	--without-pkg-config
extconf.rb:83:in `<main>': libvirt library not found in default locations (RuntimeError)

extconf failed, exit code 1

Gem files will remain installed in /home/wguo/.gem/ruby/gems/ruby-libvirt-0.4.0 for inspection.
Results logged to /home/wguo/.gem/ruby/extensions/x86_64-linux/ruby-libvirt-0.4.0/gem_make.out
```

### Solution:
sudo dnf install libvirt-devel
