# stackup-nft-art-engine
🖼️ Generate 50 PolyAliens NFT art and metadata with your StackUp usernames for the Quest 1

## Steps

### 1. Install packages

```sh
npm install
```

> If you deal with any errors installing packages, please check and update your `npm` version.

### 2. Generate 50 Polyaliens images and metadata

First, open `config.js` file located in `./src` directory.

Now, insert your StackUp username inside description.

```javascript
const description = "<your-stackup-username>'s PolyAliens NFT collection.";
```

Finally, to generate images and the metadata, type the following command:

```sh
node index.js
```

> This will generate `images` and `metadata` folders inside `./build` directory.

### 3. Upload images folder to IPFS using [Pinata](https://www.pinata.cloud/)

* Upload `images` directory to Pinata.

* Copy the CID of `images` folder.

### 4. Update the IPFS CID in metadata

First, open `config.js` file located in `./src` directory.

Now, paste the IPFS CID of `images` you just copied from Pinata in baseUri `UPDATE`

```javascript
const baseUri = "ipfs://UPDATE";
```

To replace the `UPDATE` with your IPFS CID of `images`, run the following command:

```sh
node utils/updateBaseUri.js
```

### 5. Upload json folder to IPFS using [Pinata](https://www.pinata.cloud/)

* Upload `json` directory to Pinata.


Happy hacking!
