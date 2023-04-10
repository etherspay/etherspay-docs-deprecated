---
description: https://etherspay.com
---

# Etherspay Token ($EPT)

etherspay has its own ERC20 based token. The purpose of $EPT is to reward users that actively use etherspay. The conditions for earning rewards are listed on [etherspay-faq.md](../faq/etherspay-faq.md "mention")

### Source code

The source code of the $EPT token is available on Github and is written down below and the contract ABI is available [<mark style="color:green;">**here**</mark>](https://github.com/rayorole/etherspay-token/blob/dev/build/contracts/ERC20.json)

{% embed url="https://github.com/rayorole/etherspay-token" %}

{% tabs %}
{% tab title="Token.sol" %}
```solidity
// SPDX-License-Identifier: MIT
pragma solidity >=0.4.22 <0.9.0;

import "./SafeMath.sol";
import "./IERC20.sol";

contract ERC20 is IERC20 {
    string public name = "etherspay";
    string public symbol = "EPT";
    uint8 public decimals = 18;
    uint256 public _totalSupply = 201020210 ether; // 201 million tokens

    using SafeMath for uint256;

    mapping(address => uint256) balances;
    mapping(address => mapping (address => uint256)) allowed;

    constructor() {
        balances[msg.sender] = _totalSupply;
    }

    function totalSupply() public override view returns (uint256) {
        return _totalSupply;
    }

    function balanceOf(address tokenOwner) public override view returns (uint256) {
        return balances[tokenOwner];
    }

    function transfer(address receiver, uint256 amount) public override returns (bool) {
        require(amount <= balances[msg.sender]);
        
        balances[msg.sender] = balances[msg.sender].sub(amount);
        balances[receiver] = balances[receiver].add(amount);
        
        emit Transfer(msg.sender, receiver, amount);
        return true;
    }

    function approve(address spender, uint256 amount) public override returns (bool) {
        allowed[msg.sender][spender] = amount;
        emit Approval(msg.sender, spender, amount);
        return true;
    }

    function allowance(address owner, address spender) public override view returns (uint) {
        return allowed[owner][spender];
    }

    function transferFrom(address owner, address buyer, uint256 amount) public override returns (bool) {
        require(amount <= balances[owner]);
        require(amount <= allowed[owner][msg.sender]);

        balances[owner] = balances[owner].sub(amount);
        allowed[owner][msg.sender] = allowed[owner][msg.sender].sub(amount);
        
        balances[buyer] = balances[buyer].add(amount);
        emit Transfer(owner, buyer, amount);
        return true;
    }

}
```
{% endtab %}

{% tab title="IERC20.sol" %}
```solidity
// SPDX-License-Identifier: MIT
pragma solidity >=0.4.22 <0.9.0;

interface IERC20 {

    function totalSupply() external view returns (uint256);
    function balanceOf(address account) external view returns (uint256);
    function transfer(address recipient, uint256 amount) external returns (bool);
    function allowance(address owner, address spender) external view returns (uint256);
    function approve(address spender, uint256 amount) external returns (bool);
    function transferFrom(address sender, address recipient, uint256 amount) external returns (bool);

    event Transfer(address indexed from, address indexed to, uint256 value);
    event Approval(address indexed owner, address indexed spender, uint256 value);
}
```
{% endtab %}

{% tab title="Safemath.sol" %}
```solidity
// SPDX-License-Identifier: MIT
pragma solidity >=0.4.22 <0.9.0;

library SafeMath {

    function add(uint256 a, uint256 b) internal pure returns (uint256) {
        return a + b;
    }

    function sub(uint256 a, uint256 b) internal pure returns (uint256) {
        return a - b;
    }
}
```
{% endtab %}
{% endtabs %}

