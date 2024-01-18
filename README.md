Step 2: Install Homebrew for a Non-Root User
Follow these steps to install Homebrew for a non-root user:

2.1. Choose Installation Directory
Select a directory where you have write permissions to install Homebrew. For example, you can choose your home directory:

bash
Copy code
export HOMEBREW_PREFIX=$HOME/homebrew
2.2. Download Homebrew Installation Script
Run the following command to download the Homebrew installation script:

bash
Copy code
curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh > install_homebrew.sh
2.3. Modify Installation Script
Open the install_homebrew.sh script in a text editor and find the line that sets the installation directory. Replace it with the directory you chose in step 2.1:

bash
Copy code
# Replace the line below with your chosen installation directory
HOMEBREW_PREFIX="/your/chosen/directory"
2.4. Run Installation Script
Execute the modified installation script:

bash
Copy code
bash install_homebrew.sh
Follow the on-screen instructions. The script will prompt you to install Homebrew in the directory you specified.

2.5. Update Shell Profile
Add the Homebrew binary location to your shell profile (e.g., ~/.bashrc or ~/.zshrc). Replace your/chosen/directory with the actual directory you selected:

bash
Copy code
export PATH=/your/chosen/directory/bin:$PATH
2.6. Source the Updated Profile
Source the updated profile to apply the changes:

bash
Copy code
source ~/.bashrc   # or source ~/.zshrc for Zsh users
Step 3: Verify Homebrew Installation
Check if Homebrew is successfully installed by running:

bash
Copy code
brew --version
You should see the Homebrew version information.

Conclusion
You've successfully installed Homebrew for a non-root user on your macOS machine. You can now use Homebrew to install and manage packages without administrative privileges.

Happy brewing!

sql
