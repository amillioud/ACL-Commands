# ACL-Commands
Commands for standard numbered and standard named ACLs

## Configuration commands
### Standard Numbered ACLs

  **The basic command to configure a standard numbered ACL:**
+  R1(config)#access-list 'number' {deny|permit} 'ip' 'wild-card mask' / any
  **Configure a remark:**
+  R1(config)#access-list '#' remark 'remark'
  
### Standard Named ACLs

  **Standard named ACLs are configured by entering 'standard named ACL config mode' and then configuring each entry within that config mode:**
+  R1(config)#ip access-lists standard 'acl-name'
+  R1(config-std-nacl)#[entry-number] {deny|permit} 'ip' 'wild-card mask' / any

### Apply to an interface:
+  R1(config-if)#ip access-group 'number' {in|out}

## Troubleshooting commands

  **view all ACLs on the router**
+  R1(config)#show access-lists
  **view all ip ACLs on the router**
+  R1(config)#show ip access-lists
+  R1(config)#show running-config | include access-list
