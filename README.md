# Homework-20-solidity

For this activity we made contracts with solidity. The first part, the associate profit splitter, the solidity code is used to help divide the amount made into portions so that each employee gets a share of the amount. The idea behind this code is to make a simple bute safe way to get these employees their share of the profits without being tampered with and to be recieved in a timely manner. 

The code starts off with setting up the pragma environment to 0.5 and then creating a contract that holds each employee designation. for this assignment we have three employees. The address are set to payable so they are allowed to accept Ether. Then we build a constructor function that can initialize variables of the employees(the addresses). 
![image](https://user-images.githubusercontent.com/71734654/115133119-6d8bfb80-9fcb-11eb-8b0e-855947464810.png)

Then I created a function that returns the balance of which should always equal 0, this is because if it isnt, that means the employees didnt recieve all of what they were supposed to be payed. Then we create a deposit function, this function is used so we can split up the amount being sent from the sender into equal amounts for each employee.
We can take care of any remainders with the msg.sender.transfer() function which transfers the remainder back to HR.

One the function is done push the compile button and then go to the deploy section on solidity. You should make sure metamask is running and is in put on your local host. Also make sure your environment is on injected web3. Scroll to the deploy button and click on the drop down arrow, this is where you enter the addresses of three employees. This part is where ganashe comes in. Ganashe is a app that lets you use prepaid test Ether and keeps track of your metamask/solidity trasnactions. You want to make sure the RPC server is set HTTP://127.0.0.1:8545 so the transaction will work.
![image](https://user-images.githubusercontent.com/71734654/115133374-4afae200-9fcd-11eb-9d74-68c20baabad3.png)

once you complete that step with ganashe and everythin is ready to go click transact! The transaction should show up on your ganashe app and you should see the Ether in some of the address get lower or higher as you transfer Ether.
You have now completed the your transaction!!

For the other two assignments, the second assignment is kind of like the first one but instead of equal amounts the goal is to send amounts to different teirs of a workforce. We know at different levels there are different salaries. The assignment calls for dividing an amount and distributing that  amount based on a percentage. One employee for example will recieve 60% of the amount, another will recieve 25%, and the remaining 15% will go to the last employee.

The third asignment has the coder making a solidity code that helps an employee recieve their 1000 shares over a 4 year period. This conract is made so it takes in when the employee reaches a year in the 4-yeear span they recieve their share and if they leave the company before the 4 years is up that the remaining shares will be returned to the company. 
