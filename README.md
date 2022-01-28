# blockchain-lecture2022
My repository for the blockchain lecture 2022 at dhbw mannheim


## Erste Vorlesung
Benutzter Technologie Stack:

<https://remix.ethereum.org> - als Online IDE für Smart Contracts

<https://metamask.io> - als Web3 Wallet integriert in Chrome/Brave

Solidity - objektorientiere anwendungsspezifische höhere Programmiersprache für die Entwicklung von Smart Contracts auf Blockchain-Plattformen

<https://faucet.egorfine.com> - Webseite zum erhalten von Testether, einfach deine Walletadresse eintragen und man erhält 0.3 ETH 

<https://ropsten.etherscan.io> - Blockchain Explorer für Ropsten Testnetzwerk

### Erstellen eines eigenen Smart Contract mit Solidity und Deployment auf Ropsten Testnetzwerk
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

4. Compiliere innerhalb der IDE den Smart Contract
5. Da wir zunächst etwas Ether benötigen um den Smart Contract auf der Blockchain zu deployen, sollte man über <https://faucet.egorfine.com> sich zunächst etwas Testether besorgen. Grad auf der Webseite die Walletadresse des eigenen Metamask-Wallets angeben und schon erhält man 0.3 Testether.
6. Sobald die Testether in eurem Metamask-Wallet angekommen sind wechseln wir zurück in die IDE. 
7. Für den Deploy wählen wir als Environment Injected Web3 aus. Nun sollte sich das Metamask Wallet damit verbinden
8. Nun bezahlen wir die Gas Fees um den Smart Contract auf der Blockchain zu deployen.
9. Der nächste Schritt wird sein auf <https://ropsten.etherscan.io> zu gehen und dort unsere Wallet Adresse einzugeben.
10. Dort sollten wir nun die Transaction des Smart-Contracts sehen. Wir klicken auf die Transaktion und sehen nun die Adresse des Smart Contracts. Diese Adresse kopieren wir nun und fügen sie in Metamask unter "Import Tokens" ein.
11. Nun sollten wir innerhalb unseres Metamask Wallets unsere 42 TINF-Coins sehen.


### Testing to Deploy a NFT on <https://test.opensea.io>
Als erstes sollte man sich ein paar hübsche Kunstwerke anlegen - dies könnnen einfache Bilder sein.





