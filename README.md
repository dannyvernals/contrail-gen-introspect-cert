# contrail-gen-introspect-cert
Ansible playbook to get a X.509 key/cert signed by local Contrail CA (easyrsa)  
This is useful when you are interacting with Contrail remotely e.g. with Introspect APIs and need to authenticate with client-side certs.  

to use:  
1) input IP of easrsa CA Container / VM  into inventory.ini
2) input name of the Contrail cluster you wish to generate a certificate to interact with in the inventory (entity_name)  
3) run ansible-playbook  -i inventory.ini sign_cert.yml  
4) An environment variables file linking to the newly generated certs will be produced that can be used with https://github.com/dannyvernals/contrail-introspect-cli  
