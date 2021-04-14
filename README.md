# Keypair lib

Component to generate and regenerate a keypair, in a deterministic and private way.
The cryptographic part consists of two [Zenroom](zenroom.org) smart contracts, the first executed server-side to generate a seed (based on public data such as user name), the second generate client side, based on the output of the first smart contract and on private information, namely "The challenges". 


To configure backend environment variables please put an .env file at the top of your project like this or rename .env.sample to .env: 

```json
#BACKEND CREDENTIALS
BACKEND_PRIVATE_KEY=Aku7vkJ7K01gQehKELav3qaQfTeTMZKgK+5VhaR3Ui0=
BACKEND_PUBLIC_KEY=BBCQg21VcjsmfTmNsg+I+8m1Cm0neaYONTqRnXUjsJLPa8075IYH+a9w2wRO7rFM1cKmv19Igd7ntDZcUvLq3xI=
BACKEND_PASSWORD=myVerySecretPassword

#CHANGE HERE TO OVERRIDE THE CONTRACTS
SERVER_SIDE_CONTRACT=zencode/Keypair-Creation-Server-Side.zen
CLIENT_SIDE_CONTRACT=zencode/Keypair-Creation-Client-Side.zen

#CHANGE HERE TO OVERRIDE FOLDER OR FILENAME default: prop/questions-en_GB.json
QUESTION_FOLDER=props/
QUESTION_FILE_PREPEND=questions-
``` 
 
 