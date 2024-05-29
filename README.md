**SOLIDITY ASSESSMENT**

In this repository, this contains the required code for the Solidity: ETH PROOF BEGINNER EVM Course challenge. 

**DESCRIPTION**

This activity let's us explore the Remix Etherium IDE. A function called contract is created in here wherein I've created an NFT called Doge Coin.
I've also included an input to mint the amount of coins you would be handling that would later on reflect in your account as your balance.
You can also burn your coins in a specific amount of your desire yet not higher than your balance.
Explore the code to know how it works.

**Getting Started**

**Executing program**

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

pragma solidity 0.8.26;

contract NFToken{
    
    // public variables here
        string public tokenName = "DOGE Coin";
        string public tokenAbbrv = "DOGE";
        uint public totalSupply =0;

    // mapping variable here
        mapping(address => uint) public bal;

    // mint function
        function mint(address add, uint val) public{
            totalSupply += val;
            bal[add] += val;
        }
    // burn function
        function burn(address add, uint val) public{
            require(bal[add] >= val, "The number you've inputted does not compute with the balance.");
                totalSupply -= val;
                bal[add] -= val;
        }
     }

You have to compile the code in order for it to work, you can do that by clicking on compile in the online IDE then you can now run the code. You can also check on the auto-compile button in the compile section so you won't have to click it again.
![image](https://github.com/alpha-doge/NTC-LAZO-Solidity_Assessment/assets/125114021/b02a1abc-aaaa-4878-b4b0-bbb221245b97)

Once you're done compiling, you have to go to the deploy section in the Remix IDE then deploy the code to run the NFT Doge Coin transaction.
Copy paste your Account number in the deploy section then paste it in any transaction tab you want whether it is check your balance, minting, and burning coins.

![image](https://github.com/alpha-doge/NTC-LAZO-Solidity_Assessment/assets/125114021/3febdf57-594c-4f5b-ae78-8cf6aee1892a)

**Author**

Kobe Michael A. Lazo

**License**

This project is licensed under the DOGE License
