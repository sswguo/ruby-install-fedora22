# ruby-install-fedora22

## Ref:
http://guides.ruby-china.org/getting_started.html

## Issue #1:
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

## Solution:
1:  gem install json -v 1.8.3 

## Issue #2:  
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

## Solution:
sudo dnf install libvirt-devel
