# RefChain Bounty dApp

[![Build Status](https://travis-ci.org/ifeLight/refchain.svg?branch=master)](https://travis-ci.org/ifeLight/refchain)

Refchain Bounty dApp is an decentralized application that aims to solve the problem of trust in centralized bounties.

* Creating a bounty is simple, user sets the name, description and amount of Ether that is prepared to pay for the successfuly completion of the given task. 
* Users can list the bounties and submit the solutions/service.
* Bounty issuer can reject or approve a submission. 
* Approving a submission pays the Ether, rejects all other submissions and closes the bounty.
* Ether is stored on the smart contract and cannot be withdrawn from it.

## Running the dApp

For running this app localy you need to have installed Node, Truffle and Ganache CLI.


## Installation & Usage

### Prerequisites 
The following software prerequisites must be met to run Thames Boats. The instruction linked are for Ubuntu Linux. 


* <a href="https://www.liquidweb.com/kb/install-git-ubuntu-16-04-lts/" target="_blank">Git</a> 

* <a href="https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/" target="_blank">NodeJS, v10</a> (or later)

* <a href="https://linuxize.com/post/how-to-install-node-js-on-ubuntu-18.04/" target="_blank">npm v6</a>  (or later)

* <a href="https://truffleframework.com/docs/truffle/getting-started/installation" target="_blank">Truffle</a> (latest version)

* <a href="https://truffleframework.com/ganache" target="_blank">Ganache</a> (latest version)

* Either Chrome or FireFox with the MetaMask extension installed.

1. Clone the repo, move into the directory, install external contract node modules for frontend.
Note: It can take a couple of minutes.

	```sh
	 git clone https://github.com/ifeLight/refchain.git
	 cd refchain
	 npm install
    ```

2. Install Truffle and Ganache globally.

	```sh
	 npm install -g truffle@5
	 npm install -g ganache-cli
    ```

3. Run Ganache with predefined seed words.

	```sh
	ganache-cli -m "recipe program twist race bind host dutch fog item rigid decline media"
    ```
4. Open metamask with the above seed words and set it to a private network (localhost 8545).
	An account will be created with 100 ETH.

5. In a second terminal tab compile and migrate the smart contracts.

	```sh
	truffle compile
	truffle migrate --reset --network development
    ```

6. Test the contract by running tests in truffle.

	```sh
	truffle test
    ```

7. Run the frontend (App will be available at http://localhost:3000).

	```sh
	npm start
    ```


