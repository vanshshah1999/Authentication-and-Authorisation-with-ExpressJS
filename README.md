# Authentication-and-Authorisation-with-ExpressJS

## Difference Between Authentication and Authorization

### Authentication
Authentication is the process of verifying a user's identity. For example, during login, a user enters credentials such as a username and password. These credentials are matched against system records, and if they match, the user is authenticated and granted access to the system. Think of authentication as the key to open the door to the system.

### Authorization
Authorization determines what an authenticated user is allowed to do within the system. Once a user is authenticated, authorization controls access to resources and actions. For instance, even if a user is logged in, they may not have the permissions to delete someone else’s account unless they have admin privileges or special rights. Imagine authorization as keys to different rooms within the system. You can only enter the rooms you are authorized to access.

### In Summary
- **Authentication**: Confirms your identity, like using a key to enter the building.
- **Authorization**: Controls what you can do once inside, like having keys to specific rooms.

## Why Deleting a User After Authentication is Risky

Deleting a user account based only on authentication, without proper authorization checks, poses several risks:

### Security Risks
If user account deletion is permitted solely through authentication, anyone logged into the system could potentially delete accounts maliciously. For example, a disgruntled user might delete accounts at will, leading to data loss and eroding trust in the platform.

### Lack of Accountability
Without adequate restrictions on who can perform critical actions like deleting accounts, the system is vulnerable to misuse. Whether through accidental errors or deliberate interference, unrestricted deletion capabilities can cause significant disruption and data integrity issues.

### Violates the Principle of Least Privilege
The principle of least privilege dictates that users should have only the permissions necessary for their roles. Allowing users to delete other accounts contradicts this principle, as not all users should have the authority to perform such significant actions.

# Running the Application
1. Fork the repo.
2. Clone the App in your Local environment:
```bash
git clone https://github.com/your_github_username/authentication-and-authorisation-with-expressjs
```
3. Go to back-end directory, install the dependencies:
```bash
cd authentication-and-authorisation-with-expressjs/back-end
npm install
```
4. Add a `.env` file in the back-end folder:
```bash
echo 'TOKEN_KEY="StackUpAuthenticationProject123!"' > .env
echo 'PORT=4001' >> .env
```
5. Install "Live Server" and "Sqlite3 Viewer" VS Code extenstion
6. Go to `web-front-end\pages\index.html` file and the click "Go Live" on bottom right, the frontend Application will start running.
7. Run the server:
```bash
node app.js
```
