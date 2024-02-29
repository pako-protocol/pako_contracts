

## ⚙ Development

# create env file 

###  example  value

ETHERSCAN_API_KEY=ABC123ABC123ABC123ABC123ABC123ABC1
PRIVATE_KEY= fe454ae7b8c01b307e3b65143805978cf009434f5f02ca571a299ff74c425946
BTTC_RPC_URL=https://pre-rpc.bt.io/
DEPLOYMENT_CONTEXT=bttc



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

