# Using Ansible with Google Cloud Platform inventory source 

Ansible script


Check if Ansible **google.cloud** plugin collection is already installed

```console
$ ansible-galaxy collection list | grep google.cloud
google.cloud                  1.0.2
```


If not install the Ansible **google.cloud** plugin collection

```console
$ ansible-galaxy collection install google.cloud
```

Test the inventory creation

```console
$ ansible --list-hosts all
```

Test the connection to computes

```console
$ ansible -m ping all 
```

Using playbook

```console
$ CLOUDSDK_PYTHON_SITEPACKAGES=1 ansible-playbook test.yml 
```