# My Puppet Project
## Introduction

This is a very simple project showing the roles and profiles pattern with
hiera. 

See: 
  https://puppetlabs.com/presentations/designing-puppet-rolesprofiles-pattern

### Getting Started 

### Important Files

#### ENC Script (assign Roles to nodes) 

```
/etc/puppet/environments/puppet/public/$BRANCHNAME/enc/puppet_enc.sh
```

#### Default Manifest:

```
/etc/puppet/environments/puppet/public/$BRANCHNAME/manifests/site.pp
```

#### Hiera files and structure:

  - "/etc/puppet/environments/%{::environment}/hieradata/certname/%{::clientcert}"
  - "/etc/puppet/environments/%{::environment}/hieradata/cluster/%{::cluster}"
  - "/etc/puppet/environments/%{::environment}/hieradata/role/%{::role}"
  - "/etc/puppet/environments/%{::environment}/hieradata/topic/%{::topic}"
  - "/etc/puppet/environments/%{::environment}/hieradata/location/%{::location}"
  - "/etc/puppet/environments/%{::environment}/hieradata/common"

## License

Apache 2.0 License

```
   Copyright 2016 T-Systems Multimedia Solutions GmbH

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```