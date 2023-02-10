# Fair Funding

Fair Funding is a concept that allows crypto projects to be funded while limiting the downside exposure of investors.
The Fair Funding platform performs an auction every day (similar to NounsDAO) that promises benefits in the funded project.
Investors bid in the auction and the highest bidder after 24h wins.
The funds deposited in the auction by the investor are then put into an Alchemix vault and a non-liquidatable, self-repaying loan is taken out against this position.
The loan is sent to the raising project while the investor retains complete control over his funds at Alchemix with the help of an ERC721 that represents his position. Over time the self-repaying feature of Alchemix will release the funds and the token owners can claim their share until fully repaid.

## Contracts
- `AuctionHouse.vy` handles the daily auction
- `Vault.vy` handles the Alchemix integration
- `MintableERC721.sol` is an OpenZeppelin based ERC721 implementation used to represent the financial positions in the vault


## Tests

The Fair Funding platform has been developed almost exclusively test driven with the help of Titanoboa & Vyper.
A total of 133 tests cover all aspects of the auction, vault and user interactions.

We use Poetry (https://python-poetry.org/) for the python env management.

To run the tests run:
```
poetry shell
poetry install
pytest
```

## Contact
https://unstoppable.ooo


## Security Contact
team@unstoppable.ooo