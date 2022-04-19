<<<<<<< HEAD
# Create An ENTIRE NFT Collection (10,000+) & MINT
=======
# Minting DAPP
>>>>>>> a34c8e1 (main)

## Table of Contents

- [RESOURCES](#resources)
<<<<<<< HEAD
- [COMMANDS](#commands)
- [UPDATES & FIXES](#updates--fixes)

## RESOURCES

Original Video: 

👴 [How To Create An ENTIRE NFT Collection (10,000+) & MINT In Under 1 Hour Without Coding Knowledge](https://youtu.be/AaCgydeMu64)

(WATCH THIS ONE!) Updated video for v2.0.0 release: 

🌟 [How To Create An ENTIRE NFT Collection (10,000+) & MINT with ZERO Coding Knowledge v2.0](https://youtu.be/quGdJweadFM)

How to automate listing for sale on OpenSea: 

💰 [How To List & Reveal An ENTIRE NFT Collection (10,000+) Without Coding Knowledge on OpenSea](https://youtu.be/Iy1n_LxUwZs)

Original video code: [v0.1.0-alpha](https://github.com/codeSTACKr/video-source-code-create-nft-collection/releases/tag/v0.1.0-alpha)

Base code is from [hashlips_art_engine](https://github.com/HashLips/hashlips_art_engine)

Minting uses [NFTPort](https://nftport.xyz)

Join the Discord server for more help from the community: [codeSTACKr Discord](https://discord.gg/A9CnsVzzkZ)

The macro script from the "listing for sale" video: [macro1.mmmacro](macro1.mmmacro)

UPDATE: Added rarity calculator. See this [video](https://youtu.be/Uz1y4j9gvP8) for the walkthrough.
=======
- [INSTALLATION](#installation)
- [COMMANDS](#commands)

## RESOURCES

Video: 

🌟 [EASY Minting dApp | Whitelisting | Entire Process!! Create an Entire NFT Collection (10,000+)](https://youtu.be/cLB7u0KQFIs)

Base art generator code is from [hashlips_art_engine](https://github.com/HashLips/hashlips_art_engine)

Contract uses [NFTPort](https://nftport.xyz)

Join the Discord server for more help from the community: [codeSTACKr Discord](https://discord.gg/A9CnsVzzkZ)

## INSTALLATION

### Backend

- Clone this repo or download the latest release zip file.
- Unzip, if needed, and open the folder in VS Code.
- From the terminal run: 
```
 npm install
```
- Copy your image layers into the `/backend/layers` folder.
- Use the `/backend/src/config.js` file to set up your layers and NFT information.
>>>>>>> a34c8e1 (main)

## COMMANDS

Generate: 
```
$ npm run generate
```
<<<<<<< HEAD
- Generates unique images based on the layers in the `layers` folder.
- WARNING: This command deletes the `build` folder if it exists!
=======
- Generates unique images based on the layers in the `/backend/layers` folder.
- WARNING: This command deletes the `/backend/build` folder if it exists!
>>>>>>> a34c8e1 (main)

Rarity (Hashlips): 
```
$ npm run rarity
```
- Calculates the rarity of NFT properties based on layer files.

Rarity (codeSTACKr): 
```
$ npm run rarity_md
```

- Calculates the rarity of NFT properties based on metadata.

Rarity Rank (codeSTACKr): 
```
$ npm run rarity_rank
```

- Provides ranking details through a user interface after calculating using the codeSTACKr Rarity command.

Update Info: 
```
$ npm run update_info
```

- Allows you to update `namePrefix`, `description`, and/or `baseUri` for metadata after it was already generated.

Create Generic Metadata: 
```
$ npm run create_generic
```

<<<<<<< HEAD
- Creates generic metadata using the settings from the `src/config.js` file.
=======
- Creates generic metadata using the settings from the `/backend/src/config.js` file.
>>>>>>> a34c8e1 (main)

Upload Files/Images: 
```
$ npm run upload_files
```

<<<<<<< HEAD
- Uploads all files in the `build/images` folder.
=======
- Uploads all files in the `/backend/build/images` folder.
>>>>>>> a34c8e1 (main)

Upload Metadata: 
```
$ npm run upload_metadata
```

<<<<<<< HEAD
- Uploads all `.json` files in both the `build/json` folder and, if it exists, the `build/genericJson` folder as well. 
=======
- Uploads all `.json` files in both the `/backend/build/json` folder and, if it exists, the `/backend/build/genericJson` folder as well. 
>>>>>>> a34c8e1 (main)

Deploy Contract: 
```
$ npm run deploy_contract
```

<<<<<<< HEAD
- Deploys a contract to the blockchain using the settings from the `src/config.js` file.
=======
- Deploys a contract to the blockchain using the settings from the `/backend/src/config.js` file.
>>>>>>> a34c8e1 (main)

Get Contract: 
```
$ npm run get_contract
```

- Gets the deployed contract details using the transactions hash from the Deploy Contract command. 

<<<<<<< HEAD
Mint: 
```
$ npm run mint
```

- Running this command with no flags will mint all NFTs
- `--start=1`
  - The start flag indicates the edition number to start minting from.
- `--end=100`
  - The end flag indicates the edition number to stop at.
- To start at a number and continue minting all, do not include the end flag.
- Make both flags the same number to only mint a single NFT.
- NOTE: The start and end numbers are inclusive.

Reveal: 
```
$ npm run reveal
```

- Checks the contract owners wallet to see which NFTs have sold and reveals all sold NFTs.
- Including the `--start=1` and/or `--end=100` flags will reveal only the specified edition or range of editions.
- Make both flags the same number to only reveal a single NFT.

Check Transactions: 
```
$ npm run check_txns --dir=minted
```

- Verifies the success of mint or reveal transactions.
- The `--dir` flag is required. Accepted values are `minted` or `revealed`.
=======
Update Contract:
```
$ npm run update_public_mint_start_date
$ npm run update_presale_mint_start_date
$ npm run update_presale_whitelisted_addresses
$ npm run update_presale_whitelisted_addresses_remove
$ npm run update_royalty_share
$ npm run update_royalty_address
$ npm run update_base_uri
$ npm run update_prereveal_token_uri
```

- Updates specific fields of the contract using the settings from the `/backend/src/config.js` file.
- Available fields to update:
  - `prereveal_token_uri` - This will update the pre-reveal token uri for all NFTs. (Hidden image)
  - `base_uri` - This will update the base uri for all NFTs and reveal all.
  - `public_mint_start_date` - Eg: 2022-02-08T11:30:48+00:00
  - `presale_mint_start_date` - Eg: 2022-02-08T11:30:48+00:00
  - `presale_whitelisted_addresses` - Adds address(es) to the whitelist
  - `presale_whitelisted_addresses_remove` - Removes address(es) from the whitelist
  - `royalties_share` - Updates the royalty share
  - `royalties_address` - Updates the royalty wallet address
>>>>>>> a34c8e1 (main)

Refresh OpenSea: 
```
$ npm run refresh_os --start=1 --end=100
```

- Refreshes the listing for the specified editions on OpenSea.
- Both the `--start` and `--end` flags are required.

<<<<<<< HEAD
## UPDATES & FIXES

### npm not recognized

You have not installed [node.js](https://nodejs.org) properly (* and or if you're using a M1 on macs you'll need to downgrade your current version of node.js to v14 for it to work*). Be sure to follow the installation instructions from their download page for your specific operating system. And restart your computer after installation. 

For Mac M1 users, see this issue for more details: [Hashlips Art Engine - Issue 812](https://github.com/HashLips/hashlips_art_engine/issues/812)

### Images not lining up

Be sure that every layer is the same size. If you want the resulting image to be 512x512, then each layer needs to be 512x512. This will ensure that everything lines up properly.

### Only the last image shows up

This is because you are not using `.png` images. `.jpg` or any other type will not work. `.png` has transparency which means there is no background and things behind it will show through. 

### ES Module Error \[ERR_REQUIRE_ESM\]

If you are following along with the tutorial you will run into this issue unfortunately. 

When the tutorial was created, `node-fetch` was at version 2. It was recently updated to version 3 and no longer supports the `require` syntax. 

Fortunately, it's an easy fix. Just type these commands into the terminal:

- `npm uninstall node-fetch`
- `npm install node-fetch@2`

### Any sort of "path" error

Ensure that your layer names in the `config.js` file match exactly to your layer folder names. Also, remove any `-` (hyphens) from your file names.

### "Quota Limit Reached" or "Too many requests" errors

There have been some changes made to the code from the original video resulting from some errors when uploading files, metadata, and minting using NFTPort. Depending on your plan, Free vs Community, there are rate limits.

To fix these issues, I've updated the code to include a timeout that will allow the files to be uploaded at a slower rate, instead of all at once, eliminating these errors.

If you've reached your quota limit, contact NFTPort to upgrade your plan to get more. 

**To use this code:**

- Clone this repo or download the latest release zip file.
- Unzip, if needed, and open the folder in VS Code.
- From the terminal type: 
  - `npm install`
- Copy your image layers into the `layers` folder.
- Use the `src/config.js` file to set up your layers and NFT information.

## Reference the [video](https://youtu.be/quGdJweadFM) for more details.
=======
## Reference the [video](https://youtu.be/cLB7u0KQFIs) for more details.
>>>>>>> a34c8e1 (main)
