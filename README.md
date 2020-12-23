# contrail-gen-introspect-cert
Ansible playbook to get a X.509 key/cert signed by Contrail Introspect CA (easyrsa)
to use:  
1) input IP of easrsa CA Container / VM  
2) run ansible-playbook  -i inventory.ini sign_cert.yml  
3) An environment variables file linking to the newly generated certs will be produced that can be used with https://github.com/dannyvernals/contrail-introspect-cli  
