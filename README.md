# Foundry
## forge

## 创建新项目:XXX
```forge init XXX```

## 编译合约
```forge build```
 
## 运行测试
```forge test```

## 部署合约
```forge create SimpleStorage --interactive --rpc-url http://127.0.0.1:8545```

## 用脚本部署合约
```forge script script/DeploySimpleStorage.s.sol```

forge script script/DeploySimpleStorage.s.sol --rpc-url http://127.0.0.1:8545

forge script script/DeploySimpleStorage.s.sol --rpc-url http://127.0.0.1:8545 --broadcast --private-key 0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80

forge script ./script/DeploySimpleStorage.s.sol --rpc-url $RPC_URL --broadcast --private-key $PRIVATE_KEY

forge script script/DeploySimpleStorage.s.sol:DeploySimpleStorage --rpc-url http://localhost:8545 --account defaultKey --sender 0xf39fd6e51aad88f6f4ce6ab8827279cfffb92266 --broadcast -vvv

Contract Address: 0x5FbDB2315678afecb367f032d93F642f64180aa3

## 把环境变量导入
```source .env```

## 格式化
```forge fmt```

# cast
```cast --to-base .... dec```

## 调用send 函数store
cast send 0x5FbDB2315678afecb367f032d93F642f64180aa3 "store(uint256)" 123 --rpc-url $RPC_URL --private-key $PRIVATE_KEY

## 调用call 函数retrieve
cast call 0x5FbDB2315678afecb367f032d93F642f64180aa3 "retrieve()"

## foundryup
运行此命令```foundryup```将自动安装最新stable版本的预编译二进制文件：forge,cast,anvil,chisel

## Documentation

https://book.getfoundry.sh/