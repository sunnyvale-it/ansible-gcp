# Using Ansible with Google Cloud Platform inventory source 

Check if Ansible **google.cloud** plugin collection is already installed

```console
$ ansible-galaxy collection list | grep google.cloud
google.cloud                  1.0.2
```


If not install the Ansible **google.cloud** plugin collection

```console
$ ansible-galaxy collection install google.cloud
```

Before proceeding, open the [misc/inventory.gcp.yml](misc/inventory.gcp.yml) file and change the following params, according to your environment:

```yaml
projects:
  - myproj
service_account_file: credentials.json
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