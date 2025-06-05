# Varangian Guard Template

## Setup

### Secrets

For the actions to work multiple secrets need to be set in the settings. For this go to `Settings` > `Secrets and variables` > `New repository secret` and set the following secrets:

- `COSIGNER_MATERIAL` - random string that is used to derive the Co-Signer private key
- `SAFE_ADDRESS` - address of the Safe that should be monitored
  - Example: `0x779720809250AF7931935a192FCD007479C41299`
- `SERVICE_URL` - base url of the service that is used to submit transactions
  - Example: `https://safe-transaction-gnosis-chain.safe.global/`


### Activating Actions

For the GitHub actions to work the initial run has to be manually activated. This will also output the address of the Co-Signer.

For this go to `Actions` > `Varangian Co-Signer` (in the left sidebar) and click `Run workflow` (on the right side)