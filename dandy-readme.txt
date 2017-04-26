Available Accounts
==================
(0) 0x72e64d1c304a6daf2438fea17024cb8e851603ed
(1) 0xbabce737cb7d1fb12324de34617bed25f0c1488a
(2) 0x791ac51e4460107190437ba816328f2dae4c5104
(3) 0x8f61dd32b6e155be40ae227186d47140b27bd12a
(4) 0x8a964a1c7665f17d959bb5fea5fecac3c8362f43
(5) 0xe0f257182fe0f2ab2de4aeb3bdc8a829ef0493a8
(6) 0xd364feaea358b23a9d117febd4d02ed4881ca5a0
(7) 0x360b66172e31b8b69508f3ca81c083c7d5173409
(8) 0x8009685981ad2e940be15372a7ba07b449a1ca68
(9) 0x0451da326726890284a078e4dd6e3f658933228d


testrpc
truffle compile (Complie and create artifacts json file)
truffle migrate
truffle migrate --reset(Compile and execute migrations js, which is deploying contract)
truffle compile && truffle migrage --reset
truffle console (Run truffle console)


// get accounts
web3.eth.accounts

// get reference to deployed contract
var metaCoin;
MetaCoin.deployed().then(function(deployed) {metaCoin = deployed;});

// get balance of account 0
metaCoin.getBalance.call(web3.eth.accounts[0])

// send coins
var account0 = web3.eth.accounts[0];
var account1 = web3.eth.accounts[1];
metaCoin.sendCoin(account1, 1000, {from: account0});
metaCoin.getBalance.call(account0);
//test