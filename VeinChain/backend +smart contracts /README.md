
# VeinChain

This project leverages both blockchain and fingervein hardware integration using Truffle smart contracts and Flask-based Biometric authentication applications. Follow these steps to get the project up and running.
(Note:-We do have a front-end for the same please check the repo VeinChain-Fe)
---

## 1. Ethereum Network Setup

- **Set Up Ganache or Any Ethereum Network**:  
  Ensure you have Ganache installed (or connect to another Ethereum network) as this project uses Truffle for smart contract development.  
  - [Ganache Download](https://trufflesuite.com/ganache/)  
  - Alternatively, configure your preferred Ethereum network in `truffle-config.js`.

- **Update `truffle-config.js`**:  
  Modify `truffle-config.js` with the correct provider URL and network settings according to your Ganache (or other Ethereum system) connection.

---

## 2. Smart Contract Setup with Truffle

- **Install Required NPM Packages**:  
  Navigate to the project directory and install dependencies:
  ```bash
  npm install
  ```

- **Compile Contracts**:
  ```bash
  truffle compile
  ```

- **Deploy Contracts**:  
  Run one of the following commands depending on your deployment needs:
  ```bash
  truffle migrate --reset
  ```
  or  
  ```bash
  truffle migrate --f 3
  ```
  Make sure to note the deployed contract address; this will be used in the web applications.

---

## 3. Python Environment Setup

- **Install Python Dependencies**:  
  Ensure you have Python installed, then install required packages:
  ```bash
  pip install -r requirements.txt
  ```

---

## 4. Running the Flask Applications

This project contains **two separate Flask applications** also note that to change the corresponding values for the keys and the contract addresses accordingly before the following steps:

- **web2flas.py**:  
  This is the main application that interacts with our hardware.

- **web3flas.py**:  
  This application handles dataset images for preprocessing and blockchain interaction.

> **Note**: The applications are Flask-based and come with Swagger documentation.

### Starting the Applications

1. **Run the Main App** (for hardware):
   ```bash
   python web2flas.py
   ```
2. **Run the Dataset/Blockchain App**:
   ```bash
   python web3flas.py
   ```

- **Access Swagger Documentation**:  
  Once the Flask server is running, open your browser and navigate to:
  ```
  http://<your-host>:<your-port>/apidocs
  ```
  This endpoint provides the Swagger UI for interacting with the API endpoints.

- **Update Contract Address**:  
  Use the contract address (obtained from the Truffle deployment) in the relevant sections of the web applications to ensure proper integration with the smart contracts.

---

By following these steps, you will set up your Ethereum network, compile and deploy smart contracts, install necessary dependencies, and run the Flask applications. Enjoy exploring VeinChain!

---