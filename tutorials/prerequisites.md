## Open your Cloud Shell environment

Clone the **azurehpc** repo

```
git clone git@github.com:Azure/azurehpc.git
```

If you don't have a Key Vault, create one

```
az keyvault create --name azhpc-vault --resource-group my-rg
``` 

If not done, create a password and store it in Key Vault

```
secret='yoursecret'
az keyvault secret set --vault-name azhpc-vault --name "winadmin-secret" --value $secret
```
You can access your keyvault secret from a config.json file using the following format (secret.KeyVaultName.key)

Initialize your working directory, fill up the missing parameters

```
. azurehpc/install.sh
```

`azhpc_dir` is now in your environment. This is how you will reference the files/directories.  You should create a new directory for you projects.

