# AutoTx - a Metamask Snap

## Summary

A Metamask Snap allows specific transaction profiles to be automatically signed and submitted to the blockchain, bypassing the Metamask pop-up window and allowing a smooth in-game experience

## Problem
Every time a web3 game wants to do an in-game transaction, a Metamask window pops up to sign the transaction, which offers bad UX by breaking the flow of the game

## Solution
Metamask Snaps can be used to generate and sign transactions on the user's behalf

To ensure user safety, this snap will clearly define which smart contract, which function call, and the range of acceptable parameters

## Getting Started
The prototype will consist of the following functionality:
* Input of:
  * Smart contract address
  * Function being called
  * Some fixed inputs for the function
  * Allowed ranges for numeric inputs, such as specifying 0 to 20 USDC to be spent, or a limit on game token to be spent
* Some simple use cases:
  * Pay for in-game item with tokens (parameter in the snap acts as an ERC-20 allowance, limiting how many tokens can be spent automatically)
  * Consume NFT as in-game item (acts as an ERC-721 setApprovalForAll)
  * Press an in-game button (Claim! Withdraw! Pet Aavegotchi!) (no parameters, can happen repeatedly)

## FAQ
**Who will use this?**
* Game developers who want users to be able to use an existing Metamask wallet to pay for in-game items

**What problem does this really solve?**
* Annoying Metamask pop-up windows that break the game UX

**Is this just another walled garden designed to monetize something that's freely available?**
* **No.** The entire platform is open sourced.

**Ok.. then how do you make money?**
* For token send transactions, take a tiny cut (e.g. 0.1%) and send to team Gnosis Safe

**How do I know the contracts are secure?**
* Metamask Snaps must be published as `npm` modules. Code is open-source, and can be inspected by anyone.
* TBC we assume that if the `npm` module gets upgraded then the Metamask Snap will still use the previously specified version by the game developer?

### AutoTx Roadmap

- [x] AutoTx PRFAQ Live
- [ ] AutoTx MVP released at end of Sozu Haus hacker house
- [ ] Good stuff will then happen
- [ ] Metamask Snaps currently only available in development environment (Metamask Flask), but will later hopefully be available in the main Metamask environment
- [ ] Game devs use AutoTx to smooth the UX
