Important - Required Ngrok Setup Steps
In the next lecture, we will be introducing Ngrok to tunnel traffic between our backend and Expo client.

Ngrok has made some substantial changes that require you to signup for an account and install an authtoken.

Sign up for a free account here:

https://dashboard.ngrok.com/signup

Then, download the official Ngrok library for your specific OS rather than the Node port shown in the lectures:

https://ngrok.com/download


After registering for an account and installing the full library, you will need to copy your authtoken from your Ngrok account dashboard.


Then, using your terminal, run the following command:

ngrok authtoken YOUR_AUTHTOKEN

This command only needs to be done once. Going forward, you can open a tunnel by using your terminal to run the following command (replacing PORT_NUMBER with the port of the backend server):

ngrok http PORT_NUMBER

You must run the Ngrok server directly using the above command. Do not attempt to run Ngrok from the package.json file with "npm run tunnel" as it will not use the authenticated version.

Note - If you are reading this note after attempting to use Ngrok as shown in the course, you will need to follow all of the steps above. Then, afterward, you will need to restart any running tunnels and applications and generate a new tunnel address.
