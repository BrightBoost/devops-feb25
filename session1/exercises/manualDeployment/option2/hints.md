## Hint: Install the Dependencies
To make sure everything runs smoothly, install all the necessary dependencies for the application. Run the following command in your terminal:
```bash
npm install
```
This will fetch all the required packages listed in the `package.json` file.


## Hint: Fix the Missing `.env` File
If you see an error message like this:
```
node: .env: not found
```
Don't panic! This just means that the application is expecting a `.env` file with some configuration settings. Create the file manually by following these steps:

1. In your project folder, create a new file named `.env`.
2. Add the following line inside the `.env` file:
   ```
   PORT=xxxx
   ```
Replace the xxxx by the port of choice.


## Hint: Get Your IP Address
To access the application in a browser, you'll need your VM's IP address. On windows, run the following command to find it:
```
ipconfig
```

On Linux, run:
```
ifconfig
```

If you still need to install ifconfig it will give you the command. After that, run:
```
curl ifconfig.me 
```
