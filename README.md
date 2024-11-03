# RollupFed
A Federated Learning protocol utilizing Proof of Stake to reinforce economic security within the network. The framework is built on micro-rollups to enable verifiable off-chain computations for state management, along with enforcing slashing conditions.

# Architecture
RollupFed leverages Stackr to create a micro-rollup across the client network. This rollup functions as a Model Parameters Sharing (MPS) Chain, tracking the model parameter states for each epoch. This ensures a verifiable record of the updated parameters contributed by each client.

The rollup design also enables off-chain verifiable computation, where slashing conditions are enforced. The rollup's State Transition function conducts off-chain slashing checks and maintains each client’s model parameter state, as well as a status on whether the client should be slashed for that epoch. After each epoch, the aggregator retrieves the state, and if any client is found to be malicious, it engages the SlashingManager to penalize that client by slashing their stake.
