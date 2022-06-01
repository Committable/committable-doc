# Case Study: Dapp-Learning

## 1. COMMITs

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
   | -------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
   | pragma solidity ^0.8.0;<br/>contract Incrementer {<br/>&emsp;uint public number;<br/>&emsp;constructor(uint initial) {<br/>&emsp;&emsp;number = initial;<br/> &emsp;}<br/>&emsp;function incre(int value) public {<br/>&emsp;&emsp;number = number + value;<br/>&emsp;&emsp;}<br/>&emsp;function reset() public {<br/>&emsp;&emsp;number = 0;<br/>&emsp;&emsp;}<br/>}|                pragma solidity ^0.8.0;<br/>contract Incrementer {<br/>&emsp;uint public number;<br/>&emsp;constructor(uint initial) {<br/>&emsp;&emsp;number = initial;<br/> &emsp;}<br/>&emsp;function incre(int value) public {<br/>&emsp;&emsp;number = number + value;<br/>&emsp;}<br/>&emsp;function reset() public {<br/>&emsp;&emsp;number = 0;<br/>&emsp;}<br/>&emsp;function getNum() public { <br/>&emsp;&emsp;return number;<br/>&emsp;}<br/>}   |                          pragma solidity ^0.8.0;<br/>contract Incrementer {<br/>&emsp;uint public number;<br/>&emsp;constructor(uint initial) {<br/>&emsp;&emsp;number = initial;<br/> &emsp;}<br/>&emsp;function incre(uint value) public {<br/>&emsp;&emsp;number = number + value;<br/>&emsp;&emsp;}<br/>&emsp;function reset() public {<br/>&emsp;&emsp;number = 0;<br/>&emsp;&emsp;}<br/>&emsp;function getNum() public { <br/>&emsp;&emsp;return number;<br/>&emsp;}<br/>}                                    |
   | <font size=1>Example02-web3js-transaction/Incrementer.sol</font> | <font size=1>Example02-web3js-transaction/Incrementer.sol</font> | <font size=1>Example02-web3js-transaction/Incrementer.sol</font> |
   |                                 // SPDX-License-Identifier:  MIT<br/> pragma solidity ^0.8.0;<br/>contract Incrementer {<br/>&emsp;uint public number;<br/>&emsp;event Increment(uint256 value);<br/>&emsp;event Reset();<br/>&emsp;constructor(uint initial) {<br/>&emsp;&emsp;number = initial;<br/> &emsp;}<br/>&emsp;function incre(uint value) public {<br/>&emsp;&emsp;require(value > 0,  "be positive");<br/>&emsp;&emsp;number = number + value;<br/>&emsp;&emsp;emit Increment(_value);<br/>&emsp;&emsp;}<br/>&emsp;function reset() public {<br/>&emsp;&emsp;number = 0;<br/>&emsp;&emsp;emit Reset();<br/>&emsp;&emsp;}<br/>&emsp;function getNum() public { <br/>&emsp;&emsp;return number;<br/>&emsp;}<br/>}                            |            pragma solidity ^0.8.0;<br/>contract Incrementer {<br/>&emsp;uint public number;<br/>&emsp;event Increment(uint256 value);<br/>&emsp;event Reset();<br/>&emsp;constructor(uint initial) {<br/>&emsp;&emsp;number = initial;<br/> &emsp;}<br/>&emsp;function incre(uint value) public {<br/>&emsp;&emsp;require(value > 0,  "be positive");<br/>&emsp;&emsp;number = number + value;<br/>&emsp;&emsp;emit Increment(_value);<br/>&emsp;&emsp;}<br/>&emsp;function reset() public {<br/>&emsp;&emsp;number = 0;<br/>&emsp;&emsp;emit Reset();<br/>&emsp;&emsp;}<br/>&emsp;function getNum() public { <br/>&emsp;&emsp;return number;<br/>&emsp;}<br/>}                                                  |                  pragma solidity ^0.8.0;<br/>contract Incrementer {<br/>&emsp;uint public number;<br/>&emsp;event Increment(uint256 value);<br/>&emsp;event Reset();<br/>&emsp;constructor(uint initial) {<br/>&emsp;&emsp;number = initial;<br/> &emsp;}<br/>&emsp;function incre(uint value) public {<br/>&emsp;&emsp;number = number + value;<br/>&emsp;&emsp;emit Increment(_value);<br/>&emsp;&emsp;}<br/>&emsp;function reset() public {<br/>&emsp;&emsp;number = 0;<br/>&emsp;&emsp;emit Reset();<br/>&emsp;&emsp;}<br/>&emsp;function getNum() public { <br/>&emsp;&emsp;return number;<br/>&emsp;}<br/>}                                            | 

## 2. Development
### 2.1. Structure: Abstract Syntax Tree (AST)
### 2.2 Structure: Control Flow Graph (CFG)
### 2.3 Semantics: Dependency Graph (DG)

## 3. Meta-Commit Digest
<table>
    <tr>
        <td rowspan="3">1</td>
        <td colspan="6">Structure</td>
        <td colspan="2">Semantics</td>
    </tr>
    <tr>
        <td colspan="2">sequence</td>
        <td colspan="2">selection</td>
        <td colspan="2">loop</td>
        <td rowspan="2">data flow</td>
        <td rowspan="2">control flow</td>
    </tr>
    <tr>
        <td>src</td>
        <td>exe</td>
        <td>src</td>
        <td>exe</td>
        <td>src</td>
        <td>exe</td>
    </tr>
    <tr>
        <td>CMT-24d2a418</td>
        <td>+3</td>
        <td>+39</td>
        <td>+0</td>
        <td>+7</td>
        <td>+0</td>
        <td>+2</td>
        <td>+7</td>
        <td>+5</td>
    </tr>
    <tr>
        <td>CMT-c380169d</td>
        <td>+1</td>
        <td>+5</td>
        <td>+0</td>
        <td>+1</td>
        <td>+0</td>
        <td>+0</td>
        <td>+1</td>
        <td>+0</td>
    </tr>
    <tr>
        <td>CMT-fd6974bb</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
    </tr>
    <tr>
        <td>CMT-b204d363</td>
        <td>+2</td>
        <td>+2</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
        <td>+1</td>
        <td>+0</td>
        <td>+0</td>
    </tr>
    <tr>
        <td>CMT-4f6b7384</td>
        <td>+1</td>
        <td>+9</td>
        <td>+1</td>
        <td>+1</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
        <td>+2</td>
    </tr>
    <tr>
        <td>CMT-507e68b6</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
        <td>+0</td>
    </tr>
</table>

## 4. PSR Contribution
| ID   | COMMIT                                   | P |  S&emsp;  |  R  | Contribution |
| ---- | ---------------------------------------- | ---- | ---: | ---: | -----------: |
| 1    | 24d2a418580ca7e8dad292cc0d7dedf0f384e04a | High | 0.28 |  1.0 |       138.65 |
| 2    | c380169dd489e4bb1986f8690f995fb506086430 | High | 0.18 |  1.0 |        88.13 |
| 3    | fd6974bb8eb86110a85d0cf17be3db6adec20b58 | Mid  | 0.10 |  1.0 |       49.351 |
| 4    | b204d3636fa4afb6af0a4cffb6a0e0492b116555 | Mid  | 0.17 |  1.0 |        84.71 |
| 5    | 4f6b73844dea1b07a6ddb509a21eab9635fad032 | Mid  | 0.19 |  1.0 |        94.74 |
| 6    | 507e68b6bebdb19569928a1e453e4138f1a7df4f | Low  | 0.11 |  1.0 |        54.41 |


