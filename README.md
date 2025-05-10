# HashFlog 🔒

![GitHub release](https://img.shields.io/github/release/Frost58531/HashFlog.svg) [![GitHub stars](https://img.shields.io/github/stars/Frost58531/HashFlog.svg)](https://github.com/Frost58531/HashFlog/stargazers) [![GitHub forks](https://img.shields.io/github/forks/Frost58531/HashFlog.svg)](https://github.com/Frost58531/HashFlog/network)

HashFlog is a file-based credential vault designed to securely store user credentials. It uses SHA-256 for email IDs and bcrypt for password hashing. Each record is Fernet-encrypted, ensuring that sensitive data remains protected. The design includes an append-only log and a small index for O(1) look-ups, making it lightweight and efficient. This solution requires no database and operates with just two files, making it ideal for secure prototypes, IoT applications, and web apps.

## Table of Contents

1. [Features](#features)
2. [Installation](#installation)
3. [Usage](#usage)
4. [How It Works](#how-it-works)
5. [Topics](#topics)
6. [Contributing](#contributing)
7. [License](#license)
8. [Support](#support)

## Features

- **Secure Storage**: Store email IDs using SHA-256 and passwords with bcrypt.
- **Fernet Encryption**: Each record is encrypted for added security.
- **Efficient Access**: An append-only log allows for quick retrieval.
- **No Database Required**: Works with just two files.
- **Scalable**: Designed to handle millions of users.
- **Ideal for Prototypes**: Perfect for IoT and web applications.

## Installation

To get started with HashFlog, download the latest release from our [Releases page](https://github.com/Frost58531/HashFlog/releases). After downloading, follow these steps:

1. Extract the files.
2. Navigate to the directory in your terminal.
3. Run the installation script:

   ```bash
   python setup.py install
   ```

## Usage

Using HashFlog is straightforward. Here’s how you can store and retrieve credentials.

### Storing Credentials

To store credentials, use the following command:

```bash
python hashflog.py store --email your_email@example.com --password your_password
```

### Retrieving Credentials

To retrieve stored credentials, use:

```bash
python hashflog.py retrieve --email your_email@example.com
```

### Command-Line Options

- `--email`: Specify the email ID.
- `--password`: Provide the password for storage.

## How It Works

HashFlog employs a simple yet effective architecture. Here’s a breakdown:

1. **Credential Storage**: 
   - Email IDs are hashed using SHA-256.
   - Passwords are hashed with bcrypt, which adds a salt for security.

2. **Encryption**: 
   - Each record is encrypted using Fernet, ensuring that even if files are accessed, the data remains unreadable.

3. **Log Structure**: 
   - An append-only log records each entry, allowing for easy tracking of changes.
   - A tiny index is maintained for O(1) look-ups, ensuring that retrieval is quick and efficient.

4. **File Management**: 
   - All data is stored in two files, making the system lightweight and easy to manage.

## Topics

HashFlog covers a range of topics relevant to secure credential storage:

- **append-only-log**: A method for maintaining a record of changes.
- **bcrypt**: A password hashing function designed for secure storage.
- **credential-store**: A system for securely storing user credentials.
- **encryption-decryption**: Processes for securing and accessing data.
- **fernet**: A symmetric encryption method for secure data storage.
- **file-based-database**: A lightweight alternative to traditional databases.
- **lightweight-auth**: Simple authentication mechanisms for applications.
- **password-hashing**: Techniques for securely storing passwords.
- **python**: The programming language used for implementation.
- **sha256**: A cryptographic hash function used for securing email IDs.

## Contributing

We welcome contributions to HashFlog! If you’d like to help, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or fix.
3. Make your changes.
4. Submit a pull request.

## License

HashFlog is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Support

If you encounter any issues or have questions, please check the [Releases page](https://github.com/Frost58531/HashFlog/releases) for updates and documentation. You can also open an issue in the repository for support.

---

HashFlog aims to provide a simple yet effective solution for credential management. Whether you're developing a prototype or building a secure application, HashFlog offers the tools you need to keep user data safe.