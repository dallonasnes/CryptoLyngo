# CryptoLyngo

## Netlify Demo
https://objective-goldwasser-512947.netlify.app/

## Video Demo
https://docs.google.com/document/d/1jLR6D1fWedE9N_SnZO3XlUDI0poC8_Qdefwg4h3zMHo/edit?usp=sharing

## How to run
#### Locally
1. Run `yarn install` in the root dir
2. Run `yarn chain` in one terminal
3. Once the first terminal is dumping ETH network logs, run `yarn deploy && yarn start` in the second terminal
#### Docker
1. See readme in `docker` dir

Thanks to [scaffold-eth](https://github.com/scaffold-eth/scaffold-eth)

## Deployments
### Celo Testnet (Alfajores)
LingoRewards
0x20D9c9287a077684B346E60cc489D05ac8687040

CryptoLingo
0x1B7fC3e85419A69DD4E3C7091E584107daD3E3cB

### Harmony Testnet
"LingoRewards"
0xbF090B1288F721FDC36d5D815B34Da4a79a28dCc

"CryptoLingo"
0x5eE36eb8dfB2b7edD5353b27E819723F9f640C6B


## Current Risks & Future Mitigations
### All Content is Public
Risk: All content uploaded by users is currently viewable by anyone reading the smart contract. The only gating we are doing is by the frontend. This is just for demo purposes.
Potential Mitigations: Look into using Pinata’s submarining feature, or implement our own.

### An Author can post duplicates
Risk: Anyone can call createStory on the smart contract and receive LingoRewards tokens for it, no matter if the ipfs content exists or not.
Potential Mitigations: Use an oracle to verify contents exist on ipfs; make a user stake something and have a periodic offchain script verify if contents exist or not, slash the stake if not; put a backend service for the user to call, and make the backend service call createStory on the user’s behalf.
