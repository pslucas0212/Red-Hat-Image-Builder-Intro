# Install and Configure Red Hat Image Builder to Create Red Hat Edge Devices

In this tutoria we will walk through the steps to install and configure Red Hat Image Builder using the Red Hat Enterprise Linux 9.2 (RHEL) web console.


Create a virtual machine with RHEL 8.2, 4 virtual cores 8GIB RAM and 80GB Disk.


Register system
```
$ sudo subscription-manager register --org=xxxxxxxxx --activationkey=your-activation-key
```

Update system to latest code  
```
$ sudo dnf update -y  && sudo dnf upgrade -y
```


Install the following packages on the virtual machine.
- osbuild-composer
- composer-cli
- cockpit-composer
- bash-completion
- firewalld

  ```
  $ sudo dnf install osbuild-composer composer-cli cockpit-composer bash-completion firewalld
  ```

Reboot the virtual machine
```
$ sudo reboot now
```
  
Enable the firewall
```
$ sudo firewall-cmd --add-service=cockpit && firewall-cmd --add-service=cockpit --permanent
```
