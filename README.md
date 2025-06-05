# Varangian Guard Template

## Setup

### Secrets

For the actions to work multiple secrets need to be set in the [settings](/settings/secrets/actions).

- `COSIGNER_MATERIAL` - random string that is used to derive the Co-Signer private key
- `SAFE_ADDRESS` - address of the Safe that should be monitored
- `SERVICE_URL` - base url of the service that is used to submit transactions


### Activating Actions

For the GitHub actions to work the initial run has to be manually activated. This will also output the address of the Co-Signer.

For this trigger [`Run workflow` in the actions section](/actions/workflows/cosigner.yml) of the repository AFTER setting the corresponding secrets.