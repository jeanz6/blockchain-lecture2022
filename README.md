# blockchain-lecture2022-
My repository for the blockchain lecture 2022 at dhbw mannheim


## Erste Vorlesung
Benutzter Technologie Stack:
remix.ethereum.org - als Online IDE für Smart Contracts

metamask.io - als Web3 Wallet integriert in Chrome/Brave

Solidity - objektorientiere anwendungsspezifische höhere Programmiersprache für die Entwicklung von Smart Contracts auf Blockchain-Plattformen

### Erstellen eines eigenen Smart Contract mit Solidity
1. Gehe auf remix.ethereum.org 
2. Erstelle eine weitere .sol-Datei unter dem Ordner contracts
3. Die Datei soll folgenden Code enthalten mit der wir den ersten TINF-Coin kreieren

```sol

// SPDX-License-Identifier: GNU GPL
pragma solidity >=0.8.0 < 0.9.0;

import "https://github.com/OpenZeppelin/openzeppelin-contracts/blob/release-v4.4/contracts/token/ERC20/ERC20.sol";

contract TINFCoin is ERC20 { 
    
    constructor () ERC20("TINFCoin", "TINF") { 
        _mint(msg.sender, 42 * 10 ** 18 );
    }
    
}

```
Der Coin ist auf 42 Coins limitiert und basiert auf dem ERC20-Token Standard --> Fungible Token



