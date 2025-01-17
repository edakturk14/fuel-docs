# Contract and Call Model

Fuel uses a similar model to Ethereum for contracts and cross-contract calls. Contracts may call other contracts with a [`CALL`](https://github.com/FuelLabs/fuel-specs/blob/master/specs/vm/instruction_set.md#call-call-contract) (similar to an Ethereum [message call](https://github.com/ethereum/yellowpaper/blob/8fea825c80e27fa9df5d89fb3365d1067788724e/Paper.tex#L1451)). Unlike the EVM, which can only forward its base asset with a call (i.e. ETH), the FuelVM can forward a single [native fungible asset](./native_assets.md) with a call.

Transactions may initiate contract calls. Ethereum transactions may call [a single contract directly](https://github.com/ethereum/yellowpaper/blob/8fea825c80e27fa9df5d89fb3365d1067788724e/Paper.tex#L322). Fuel transactions instead execute a [script](https://github.com/FuelLabs/fuel-specs/blob/master/specs/vm/main.md#script-execution) (arbitrary bytecode attached to the transaction), which may call any number of contracts.
