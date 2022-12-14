# Preview
Until November 28th, 2022 you can preview this app hosted on heroku [here](https://forcoderhouse.herokuapp.com/)
# Usage

## Important!

For the server to correctly work, you must set the following environment variables:

- `MONGO_URL` to connect to Mongodb
- `TWILIO_AUTH_TOKEN` and `TWILIO_ACCOUNT_SID` to send sms via Twilio
- `ADMIN_PHONE` and `ADMIN_EMAIL` to receive notifications
- `GOOGLE_MAIL` and `GOOGLE_MAIL_PASSWORD` to send emails via Gmail

### Development mode
You can run it with ts-node running the `npm run dev` command and setting the environment variables in a .env file
### Production mode

Build the project:

    npm run build

You can run it in fork mode (default):

    npm start

Or in cluster mode:

    npm start -- --mode=cluster

# Config

### Arguments

You can specify the following arguments:

- `--port` selects the port for the server to listen.
- `--mode` to run it in cluster of fork mode, fork is the default mode.
- `--i` selects how many instances will run. One instance will run in the specified port and the others in the following skipping the first one. For example if 3000 is the default port, the second server will listen in 3002, the minimum is 2 and the default is 5.

### Example

    npm start -- --mode=cluster --port=3000 --i=3

- The program will run in cluster mode, with one instance listening in port 3000 while the other two in 3002 and 3003 respectively
