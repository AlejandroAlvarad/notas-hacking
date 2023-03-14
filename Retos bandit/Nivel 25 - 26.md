## Obejtivo
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.
## Datos de acceso
**bandit.labs.overthewire.org**
**bandit25**
p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
## Solución 
```
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p 2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? tes
Please type 'yes', 'no' or the fingerprint: yes
Could not create directory '/home/bandit25/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit25/.ssh/known_hosts).
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
~                                                                                                                                       ~                                                                                                                                       ~                                                                                                                                      "/etc/bandit_pass/bandit26" [readonly] 1L, 33B
```
## Notas adicionales 
tuvimos que reducir a la pantalla para abusar del **more** y poder entrar al editor y buscar la contraseña
## Referencia