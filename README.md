# ethereum_private_network
Private Network on Ethereum Blockchain for testing purposes

I) Steps :
1) Create Genesis Block
2) Use geth cli to :
	* create custom node name with --identity
	* instruct geth to use genesis.json as the genesis block
	* specify data directory to store all the private chain data. 
	Command:
	geth --identity "enigma" init genesis.json --datadir ~/.ethereum/enigmanet
3) start the private network and use the specified data directory to access 
	private blockchain details.
	Command:
	geth --datadir ~/.ethereum/enigmanet/ --networkid 691 
4) start interactive javascript environment by attaching another console to the 
	running geth instance
	Command:
	geth attach ~/.ethereum/enigmanet/geth.ipc
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
II) Account

1) Create Externally Owned Account
	personal.newAccount()
2) check balance of new account
	eth.getBalance("address of new account")
3) mine ether into the account
	miner.start()
4) stop the miner 
	miner.stop()
4) check balance again, should be more than 0
	eth.getBalance("address of EOA")
