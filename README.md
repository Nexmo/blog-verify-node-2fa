# Add Two-Factor Authentication with Node.js, Express, and Vonage

Implement two-factor authentication in Node.js using Express and the Vonage Verify API.

## Requirements

* Node.js 18+
* A Vonage API account

## Getting Started

### 1. Clone or Fork the Repository

```bash
git clone https://github.com/Vonage-Community/blog-verify-node-2fa.git
cd blog-verify-node-2fa
````

Or run in GitHub Codespaces by appending `/codespaces` to the URL in your browser:

```
https://github.com/Vonage-Community/blog-verify-node-2fa/codespaces
```

### 2. Install Dependencies

```bash
npm install
```
### 3. Create a Vonage Apllication

In your [Vonage dashboard](https://dashboard.vonage.com/applications/new) create a new Application, generate a private key, and make note of your Application ID--you'll need these in the next step.

### 3. Add Environment Variables

Copy the example file and edit it:

```bash
cp .env.example .env
```

Fill in your values for:

```env
VONAGE_APPLICATION_ID=your-app-id
VONAGE_APPLICATION_PRIVATE_KEY_PATH=./private.key

VERIFY_BRAND_NAME=sender-id-to-be-shown-on-handset

```

> Don’t forget to add your `private.key` file to the root of the project.

### 4. Send Verification

```bash
node index.js
```
Navigate to [http://localhost:3000/](http://localhost:3000/), enter your test number, and click "Get Code".

### 5. Check Code

Enter the pin code received on your phone number, then click "Verify". The outcome of the verification will be displayed next.

## Next Steps

* Try different communication channels for sending the code
* Build multi-step [verification workflows](https://developer.vonage.com/en/verify/concepts/workflow) to allow for failback
* Check number validity using the [Number Insight API](https://developer.vonage.com/en/number-insight/overview)

## Contact

Got questions?
Join our [Developer Slack](https://developer.vonage.com/community/slack), follow us on [X (formerly Twitter)](https://x.com/VonageDev), or check out our [Developer Blog](https://developer.vonage.com/blog).
