## DbRadar:
🚀 Implemented of a Web 3.0 platform, introducing custom cryptocurrency "Dragonballs," achieving seamless user acquisition.
- Utilized React for frontend and Motoko for backend, enabling deployment on Internet Computer, decentralized web development.

### Tech Stack:
🛠️ 
- Internet Computer
- Motoko
- JavaScript
- Canister
- React
- Material-UI

### Process:

1. Check your Balance:
dfx identity get-principal

bash
Copy code

2. Save the principal id somewhere:
OWNER_PUBLIC_KEY="principal "$( dfx identity get-principal )""

markdown
Copy code

3. Check the owner's balance:
dfx canister call token balanceOf "( $OWNER_PUBLIC_KEY )"

markdown
Copy code

4. Charge the Canister:
- Check canister ID:
  ```
  dfx canister id token
  ```
- Save canister ID into a command line variable:
  ```
  CANISTER_PUBLIC_KEY="principal \"$( dfx canister id token )\""
  ```
- Transfer half a billion tokens to the canister Principal ID:
  ```
  dfx canister call token transfer "($CANISTER_PUBLIC_KEY, 500_000_000)"
  ```

5. Deploy the Project to the Live IC Network:
- Create and deploy canisters:
  ```
  dfx deploy --network ic
  ```
- Check the live canister ID:
  ```
  dfx canister --network ic id token
  ```
- Save the live canister ID to a command line variable:
  ```
  LIVE_CANISTER_KEY="principal \"$( dfx canister --network ic id token )\""
  ```
- Transfer some tokens to the live canister:
  ```
  dfx canister --network ic call token transfer "($LIVE_CANISTER_KEY, 50_000_000)"
  ```

### Dependencies:
📦 
- @dfinity/auth-client: ^0.10.3
- @dfinity/authentication: ^0.10.3
- @dfinity/identity: ^0.10.3
- lit-html: ^1.4.1
- react: ^16.8.2
- react-dom: ^16.8.2
- react-scripts: ^3.0.1
- ts-loader: ^9.2.3
- typescript: ^4.3.5

### Learnings:
📚 
- Utilizing React for frontend development
- Implementing Motoko for backend operations
- Deployment on the Internet Computer for decentralized web development

### Improvement:
🔧 
- Enhancing user interface and user experience
- Adding additional features and functionalities
- Optimizing performance and scalability

### Running the Project:
🏃‍♂️ 
- Ensure `dfx` is running.
- Deploy the project to the live IC network.
- Transfer tokens to the live canister.
- Access the project using the live canister front-end URL.

- ## Video or Image 📹🖼️
Images:
<img src = "https://github.com/Fardeeeeen/DbRadar/blob/main/db1.png" alt = "pages" />
<img src = "https://github.com/Fardeeeeen/DbRadar/blob/main/db2.png" alt = "pages" />

### 📧 Contact Information
For any inquiries or support, please contact [Fardeen Zubair](mailto:fardeenzubair@gmail.com).

