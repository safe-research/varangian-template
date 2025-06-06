# Varangian Guard Template

## Setup

### Create copy of repo

The first step is to create a copy of this repo for yourself. For this click `Use this template` (in the top right) and select `Create a new repository`.

If you want to keep your information private it is possible to mark your own repository as "private".

### Secrets

For the actions to work multiple secrets need to be set in the settings. For this go to `Settings` > `Secrets and variables` > `New repository secret` and set the following secrets:

- `COSIGNER_MATERIAL` - random string that is used to derive the Co-Signer private key
  - This should be a as long as possible, random string, so just hit your keyboard as if there is no tomorrow
- `SAFE_ADDRESS` - address of the Safe that should be monitored
  - Example: `0x779720809250AF7931935a192FCD007479C41299`
- `SERVICE_URL` - base url of the service that is used to submit transactions
  - Example: `https://safe-transaction-gnosis-chain.safe.global/`

### Activating Actions

For the GitHub actions to work the initial run has to be manually activated. This will also output the address of the Co-Signer.

For this go to `Actions` > `Varangian Guard` (in the left sidebar) and click `Run workflow` (on the right side)

After this the Varangian Guard will check every 5 to 10 minutes if a new transaction is ready. If this is the case it will sign the transaction and relay it.

### Setting up the Guard on the Safe

The Varangian Guard is based on the Safenet Guard. There are three steps necessary to complete the setup:
- Deploy the Safenet Guard contract for your Safe
- Enable the Safenet Guard contract on your Safe
- Set the Varangiuan Guard Co-Signer in the Safenet Guard contract

This actions can be performed in a single transaction. For this a Safe app is provided. Follow the steps on the [Varangian Guard Safe app repo](https://github.com/safe-research/varangian/tree/main/app) to add it to the Safe wallet app and follow the instructions.