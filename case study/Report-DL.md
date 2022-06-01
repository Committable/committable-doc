# Case Study: Dapp-Learning

1. COMMITs

   The following table introduces 6 COMMITs (native NFT in Committable) from the dapp-learning project ([https://github.com/Dapp-Learning-DAO/Dapp-Learning.git)](https://github.com/Dapp-Learning-DAO/Dapp-Learning.git).

   | Num  | COMMITs                                  | Description                                            |
   | :--: | ---------------------------------------- | ------------------------------------------------------ |
   |  1   | 24d2a418580ca7e8dad292cc0d7dedf0f384e04a | create file increment.sol, implemente basic logic      |
   |  2   | c380169dd489e4bb1986f8690f995fb506086430 | modify increment.sol, add function getNumber           |
   |  3   | fd6974bb8eb86110a85d0cf17be3db6adec20b58 | rename directory of increment.sol                      |
   |  4   | b204d3636fa4afb6af0a4cffb6a0e0492b116555 | modify increment.sol，define two events，and emit them |
   |  5   | 4f6b73844dea1b07a6ddb509a21eab9635fad032 | modify increment.sol，add require statment             |
   |  6   | 507e68b6bebdb19569928a1e453e4138f1a7df4f | modify increment.sol，add a comment                    |

   The evolvement of this project is shown as below.

   | <font size=1>Example02-web3js-sendtransaction/Incrementer.sol</font> | <font size=1>Example02-web3js-sendtransaction/Incrementer.sol</font> | <font size=1>Example02-web3js-transaction/Incrementer.sol</font> |
   | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
   | pragma solidity ^0.8.0;contract Incrementer {<br/>    uint256 public number;<br/>    constructor(uint256 _initialNumber) {<br/>        number = _initialNumber;<br/>    }<br/>    function increment(uint256 _value) public {<br/>        number = number + _value;<br/>    }<br/>    function reset() public {<br/>        number = 0;<br/>    }<br/>}` |                                                              |                                                              |
   | <font size=1>Example02-web3js-transaction/Incrementer.sol</font> | <font size=1>Example02-web3js-transaction/Incrementer.sol</font> | <font size=1>Example02-web3js-transaction/Incrementer.sol</font> |
   |                                                              |                                                              |                                                              |

   

2. 

