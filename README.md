Here’s a **GitHub README.md** for your project that explains everything clearly:

***

# **User Account Management Script**

A Bash script for managing user accounts on Linux systems. This script provides options to create, delete, reset passwords, and list user accounts, along with a help menu.

***

## **Features**

*   ✅ **Create User** (`-c` / `--create`)
    *   Prompts for username and password.
    *   Checks if the username already exists.
    *   Creates the user and sets the password.
    *   Displays a success message.

*   ✅ **Delete User** (`-d` / `--delete`)
    *   Prompts for username.
    *   Checks if the user exists.
    *   Deletes the user and their home directory.
    *   Displays a confirmation message.

*   ✅ **Reset Password** (`-r` / `--reset`)
    *   Prompts for username and new password (with confirmation).
    *   Checks if the user exists.
    *   Updates the password securely.
    *   Displays a success message.

*   ✅ **List Users** (`-l` / `--list`)
    *   Displays all system users with their **username** and **UID**.

*   ✅ **Help** (`-h` / `--help`)
    *   Shows usage instructions and available options.

***

## **Usage**

```bash
./user_mgmt.sh [OPTIONS]
```

### **Available Options**

      -c, --create       Create a new user account
      -r, --reset        Reset password for an existing user
      -d, --delete       Delete an existing user account
      -l, --list         List all user accounts with details
      -h, --help         Display this help message

***

## **Examples**

```bash
./user_mgmt.sh --create        # Create a new user
./user_mgmt.sh --reset         # Reset password for a user
./user_mgmt.sh --delete        # Delete a user
./user_mgmt.sh --list          # Show all users with UID
./user_mgmt.sh --help          # Display help
```

***

## **Prerequisites**

*   Linux system with Bash shell.
*   `sudo` privileges for user management commands.
*   Ensure the script has **execute permission**:

```bash
chmod +x user_mgmt.sh
```

***

## **Implementation Details**

*   Uses `/etc/passwd` for user existence checks.
*   Passwords are set using `chpasswd` for non-interactive updates.
*   Deletes user home directory with `userdel -r`.
*   Displays detailed error messages for invalid inputs.

***

## **Security Notes**

*   Password input is hidden using `read -s`.
*   Script must be run by a user with `sudo` privileges.
*   Does **not** display passwords after creation/reset for security reasons.

***


Would you like me to **add a section with screenshots of sample runs** and a **GitHub badge for Bash scripts**? Or should I also include **installation instructions and a troubleshooting section**?
