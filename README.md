# SWAN Pool Live-Rewards

SWAN Pool Live-Rewards is a Rails App API Backend that interfaces with a React Frontend.

The architecture of the backend is an improvement over the previous similar app called [delegation-explorer](https://github.com/AskBid/delegation-explorer).
Rather than query a `[cardano-graphql`](https://github.com/input-output-hk/cardano-graphql) that interfaces with [`cardano-db-sync`](https://github.com/input-output-hk/cardano-db-sync) (which maintannes a postgresql database) to populate our local database, in Live-Rewards I connect directyl to `cardano-db-sync` using a double database system with the Rails backend.

SWAN Pool Live-Rewards allows a user to connect one or more Stake Address to their account so to check on their rewards before thsoe are sent by the blockchain, this allows to know 10 days in advance what the rewards being accrued are.

SWAN Pool Pool-Compare allows User to select a particular Epoch Stake (a delegation of a certain address in a certain epoch) and compare the rewards they would have achieved by delegating instead to different Pools than the actual one the address was delegated to.


# About Cardano delegations

Every Cardano Coin (₳) holder can delegate their holdings to a Pool. Each delegation worth is represented from the StakeAddress amount.
Each Pool participate to a lottery to produce blocks, the more delegations a Pool have, the more likely it is to be assigned blocks to produce. Pool performance also contributes to how many blocks the pool will produce.
For each block produced the Pool will get ₳ rewards that will be split proportionally between all the Delegators.
Delegations and Rewards distribution is organised in Epochs, every 5 days new delegations can be assigned and old rewards are delivered.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/AskBid/delegations-explorer. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](contributor-covenant.org) code of conduct.

## License

The repository is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT)