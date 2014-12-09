ChefGem
=======

This is test project for an issue that I'm having post the chef 12 release.

    vagrant up
    
```
Mixlib::ShellOut::ShellCommandFailed
------------------------------------
chef_gem[jvmargs] (jvmargs::default line 10) had an error: Mixlib::ShellOut::ShellCommandFailed: Expected process to exit with [0], but received '1'
---- Begin output of /opt/chef/embedded/bin/gem install jvmargs -q --no-rdoc --no-ri -v "0.0.8" ----
STDOUT: Building native extensions.  This could take a while...
Building native extensions.  This could take a while...
STDERR: ERROR:  Error installing jvmargs:
	ohai requires Ruby version >= 2.0.0.
---- End output of /opt/chef/embedded/bin/gem install jvmargs -q --no-rdoc --no-ri -v "0.0.8" ----
Ran /opt/chef/embedded/bin/gem install jvmargs -q --no-rdoc --no-ri -v "0.0.8" returned 1

Cookbook Trace:
---------------
  /tmp/vagrant-chef-2/chef-solo-1/cookbooks/jvmargs/recipes/default.rb:10:in `from_file'

Relevant File Content:
----------------------
/tmp/vagrant-chef-2/chef-solo-1/cookbooks/jvmargs/recipes/default.rb:

  3:  # Recipe:: default
  4:  #
  5:  # Copyright 2014, YOUR_COMPANY_NAME
  6:  #
  7:  # All rights reserved - Do Not Redistribute
  8:  #
  9:
 10>> chef_gem 'jvmargs'
 11:

[2014-12-09T20:26:43+00:00] ERROR: Running exception handlers
[2014-12-09T20:26:43+00:00] ERROR: Exception handlers complete
[2014-12-09T20:26:43+00:00] FATAL: Stacktrace dumped to /var/chef/cache/chef-stacktrace.out
[2014-12-09T20:26:43+00:00] ERROR: chef_gem[jvmargs] (jvmargs::default line 10) had an error: Mixlib::ShellOut::ShellCommandFailed: Expected process to exit with [0], but received '1'
---- Begin output of /opt/chef/embedded/bin/gem install jvmargs -q --no-rdoc --no-ri -v "0.0.8" ----
STDOUT: Building native extensions.  This could take a while...
Building native extensions.  This could take a while...
STDERR: ERROR:  Error installing jvmargs:
	ohai requires Ruby version >= 2.0.0.
---- End output of /opt/chef/embedded/bin/gem install jvmargs -q --no-rdoc --no-ri -v "0.0.8" ----
Ran /opt/chef/embedded/bin/gem install jvmargs -q --no-rdoc --no-ri -v "0.0.8" returned 1
[2014-12-09T20:26:43+00:00] FATAL: Chef::Exceptions::ChildConvergeError: Chef run process exited unsuccessfully (exit code 1)
Chef never successfully completed! Any errors should be visible in the
output above. Please fix your recipes so that they properly complete.
```

