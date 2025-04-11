
Built by https://www.blackbox.ai

---

```markdown
# Safety Inspector

## Project Overview
Safety Inspector is a web application that facilitates file uploads directly to Google Drive via OAuth2 authentication. It provides a simple interface for users to authenticate using their Google account and upload files to their Drive, specifically designed to handle PDF files from an admin interface.

## Installation

To get started with Safety Inspector, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://your-repo-url.git
   cd safety-inspector
   ```

2. **Install dependencies**:
   You need to have [Node.js](https://nodejs.org/) installed on your machine. Run the following command to install the required packages:
   ```bash
   npm install
   ```

3. **Set up environment variables**:
   Create a `.env` file in the root of your project directory and populate it with the following variables:
   ```plaintext
   GOOGLE_CLIENT_ID=your_google_client_id
   GOOGLE_CLIENT_SECRET=your_google_client_secret
   GOOGLE_REDIRECT_URI=your_redirect_uri
   SESSION_SECRET=your_session_secret
   ```
   Ensure you replace the placeholders with your actual credentials from the Google Developer Console.

4. **Run the application**:
   Finally, you can start the application with:
   ```bash
   node server/server.js
   ```

## Usage

Once the server is running, navigate to `http://localhost:8000/auth/google` to begin the authentication process with Google. After successful authentication, you will be redirected to the admin interface (assumed to be hosted on `http://localhost:3000/admin.html`), where you can securely upload files.

## Features

- OAuth2 Authentication using Google accounts.
- Ability to upload PDF files directly to Google Drive.
- Simple and secure session management.

## Dependencies

The following dependencies are required for this project:

- **express**: Web framework for Node.js.
- **dotenv**: Module to load environment variables.
- **helmet**: Helps secure your Express apps by setting various HTTP headers.

To view the complete list of dependencies and their versions, refer to the `package.json` file.

## Project Structure

Here's a brief overview of the project's structure:

```
safety-inspector/
├── server/
│   └── server.js              # Main server file
├── package.json                # Node.js dependencies and scripts
└── .env                        # Environment variables (not included in version control)
```

### Scripts

- `prepare`: Installs husky for git hooks.
- `build`: Packages the application into an executable for Windows.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

Special thanks to the contributors and the documentation of technologies utilized in this project. For any issues or feature requests, feel free to open an issue on the repository.
```