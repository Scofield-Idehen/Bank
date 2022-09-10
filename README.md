#  SOLIDITY Bank CONTRACT 
A dynamic contract that allows User Deposit and withdraw ETH!!
THE PROCESS 

In creating a simple Dynamic Secure bank we must take note of the following, which are

DEPOSIT
WITHDRAW
BALANCE

We will start by understanding how to DEPOSIT inot our smart contract, the key thing here is we must first map our address to the sender, 
after mapping we must create a fucntion. 

Notice we signed the addressto a Uint(unsigned integer) 

We create a function and make a payable because we are sending ETH to the contract, we open the function and make it public since we want anyone to call it {
name[msg.sender]+=msg.value;

we said name of sender, whatever value of ETH should br added to Value of sender. 

You can compile and test a this point and see what we have done. 

WITHDRAW FUNCTION 

To create the withdraw function we create a new function called withdraw and make it public since we want anybody to call the function 

we call an arg and assign it an UINT opening the fucntion we require that whoever deposited can only collect their balance only by saying require(name[msg.sender]>=_arg,"ERR");

we call tthen minus the amount withdraw from Bal like so, name[msg.sender]-=_arg;

We create an statement (bool sent,) = msg.sender.call{value: _arg}("sent"); to optimise our contract and allow the contract to be true:

we require(sent, "ERR");

BALANCE 

Although we have a balance funtion created for us when we mapped the address to the Balances at the top we need to insert the address to see the balance but les create 
custmized bal call

create a new function and then call return(address(this).balance)

Cheers
