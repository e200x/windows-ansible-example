Enable WinRM:
powershell New-NetFirewallRule -DisplayName 'winrm' -Profile 'Any' -Direction Inbound -Action Allow -Protocol TCP -LocalPort 5985
powershell set-executionpolicy remotesigned -Force
powershell Enable-WSManCredSSP -Role Server -Force

Usage:
ansible-playbook playbook.yaml --extra-vars "ansible_password=Pa$$w0rd"