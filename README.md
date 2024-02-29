

## ⚙ Development

Install foundry if you don't have one:
```shell
# install foundry
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

Compile and run tests:
```shell
yarn
yarn test
#run single test function using --match-test
forge test --match-test testXXX  -vvvvv
#run single test contract using --match-contract
forge test --match-contract xxxTest  -vvvvv
#run a group of tests using --match-path
forge test --match-path test/...  -vvvvv
```

Deploy:
```shell
forge script scripts/Deploy.s.sol:Deploy --private-key $PRIVATE_KEY --broadcast --legacy --rpc-url $RPC_URL --ffi                   
forge script scripts/Deploy.s.sol:Deploy --sig 'sync()' --private-key $PRIVATE_KEY --broadcast --legacy --rpc-url $RPC_URL --ffi
```

