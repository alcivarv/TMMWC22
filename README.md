## About 🛠️
This repo is a modification of Hashlips NFT Dapp. It is your responsibility to review the code before using it. 

## Usage ℹ️

In order to make use of this dapp, all you need to do is change the configurations to point to your smart contract as well as update the images and theme file.

For the most part all the changes will be in the `public` folder.

To link up your existing smart contract, go to the `public/config/config.json` file and update the following fields to fit your smart contract, network and marketplace details. The cost field should be in wei.

Note: this dapp is designed to work with the intended NFT smart contract, that only takes one parameter in the mint function "mintAmount". But you can change that in the App.js file if you need to use a smart contract that takes 2 params.

```json
{
  "CONTRACT_ADDRESS": "0x4be32742F9a0d7d51A96fD0Da8A0D51f63c0F860",
  "SCAN_LINK": "https://etherscan.io/address/0x4be32742f9a0d7d51a96fd0da8a0d51f63c0f860",
  "NETWORK": {
    "NAME": "Ethereum",
    "SYMBOL": "Eth",
    "ID": 1
  },
  "NFT_NAME": "Meta World Cup 2022",
  "SYMBOL": "MWC",
  "MAX_SUPPLY": 10240,
  "WEI_COST": 800000000000000000,
  "DISPLAY_COST": 0.08,
  "GAS_LIMIT": 285000,
  "MARKETPLACE": "Opeansea",
  "MARKETPLACE_LINK": "https://opensea.io/collection/meta-world-cup",
  "SHOW_BACKGROUND": true
}
```

Make sure you copy the contract ABI from remix and paste it in the `public/config/abi.json` file.
(follow the youtube video if you struggle with this part).

Now you will need to create and change 2 images and a gif in the `public/config/images` folder, `bg.png`, `example.gif` and `logo.png`.

Next change the theme colors to your liking in the `public/config/theme.css` file.

```css
:root {
  --primary: #ebc908;
  --primary-text: #1a1a1a;
  --secondary: #ff1dec;
  --secondary-text: #ffffff;
  --accent: #ffffff;
  --accent-text: #000000;
}
```

Now you will need to create and change the `public/favicon.ico`, `public/logo192.png`, and
`public/logo512.png` to your brand images.

Remember to update the title and description the `public/index.html` file

```html
<title>Meta World Cup 2022</title>
<meta name="description" content="Mint your MWC NFT" />
```

Also remember to update the short_name and name fields in the `public/manifest.json` file

```json
{
  "short_name": "MWC",
  "name": "Meta World Cup"
}
```

After all the changes you can run.

```sh
npm run start
```

Or create the build if you are ready to deploy.

```sh
npm run build
```

Now you can host the contents of the build folder on a server.

That's it! you're done.
