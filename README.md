**ShadowStrike User Guide**

**Overview**

ShadowStrike is an advanced SSH mass brute force tool designed for penetration testers and security researchers. It employs multi-threading, password list generation, user enumeration, SSH protocol version detection, stealth mode, error handling and recovery, and reporting and logging capabilities to conduct comprehensive and effective SSH brute force attacks.

**Features**

* **Multi-threading:** ShadowStrike utilizes multiple threads to simultaneously attack multiple SSH servers, significantly reducing the overall attack time.
* **Password List Generation:** ShadowStrike can generate custom password lists based on specific criteria, such as username, company name, or common password patterns.
* **User Enumeration:** ShadowStrike can perform user enumeration on the target SSH server to identify valid usernames, allowing for a more focused brute force attack.
* **SSH Protocol Version Detection:** ShadowStrike detects the version of the SSH protocol that the target server is using, allowing for tailored attack strategies based on known vulnerabilities or weaknesses in different SSH versions.
* **Stealth Mode:** ShadowStrike employs various techniques to minimize its footprint and avoid detection by intrusion detection systems (IDS) or security information and event management (SIEM) systems.
* **Error Handling and Recovery:** ShadowStrike includes robust error handling and recovery mechanisms to gracefully handle a variety of errors and connection failures, ensuring uninterrupted attacks.
* **Reporting and Logging:** ShadowStrike provides comprehensive reporting and logging capabilities, generating reports that summarize the successful and unsuccessful login attempts and logging all relevant information to a file or database.
* **Multi-factor Authentication (MFA) Bypass:** ShadowStrike can bypass common MFA methods, such as TOTP, SMS, and hardware tokens, to authenticate with SSH servers that have MFA enabled.
* **SSH Protocol Version Detection:** ShadowStrike can detect the version of the SSH protocol that the target server is using, allowing for tailored attack strategies based on known vulnerabilities or weaknesses in different SSH versions.
* **Stealth Mode:** ShadowStrike employs various techniques to minimize its footprint and avoid detection by intrusion detection systems (IDS) or security information and event management (SIEM) systems.
* **Error Handling and Recovery:** ShadowStrike includes robust error handling and recovery mechanisms to gracefully handle a variety of errors and connection failures, ensuring uninterrupted attacks.
* **Reporting and Logging:** ShadowStrike provides comprehensive reporting and logging capabilities, generating reports that summarize the successful and unsuccessful login attempts and logging all relevant information to a file or database.
* **User Interface:** ShadowStrike provides a user-friendly command-line interface (CLI) that allows users to easily configure and run the tool.
* **Customization:** ShadowStrike allows users to customize the tool's settings and parameters to suit their specific needs, such as the target IP range, username list, password list, proxy list, and logging level.
* **Integration with Other Tools:** ShadowStrike can be integrated with other security tools or platforms to enhance its functionality, such as password cracking tools to generate custom wordlists or vulnerability scanners to identify SSH servers that are vulnerable to specific exploits.

**How to Use ShadowStrike**

1. **Installation:**

   * ShadowStrike is written in C++ and requires the following libraries:
     * libssh
     * cracklib
     * socks5
     * captchasolver
     * tfa
     * spdlog
   * To install these libraries on Ubuntu/Debian-based systems, you can use the following commands:
     ```
     sudo apt-get update
     sudo apt-get install libssh-dev libcrack2 socks5-dev captchasolver-dev tfa-dev spdlog-dev
     ```
   * On macOS, you can install the dependencies using Homebrew:
     ```
     brew install libssh cracklib socks5 captchasolver tfa spdlog
     ```
   * Once the dependencies are installed, you can compile and install ShadowStrike by cloning the GitHub repository and running the following commands:
     ```
     git clone https://github.com/byt3bl33d3r/ShadowStrike.git
     cd ShadowStrike
     make
     sudo make install
     ```

2. **Usage:**

   * To use ShadowStrike, open a terminal window and navigate to the ShadowStrike installation directory.
   * Run the following command to start the tool:
     ```
     shadowstrike
     ```
   * You will be prompted to enter the following information:
     * **Target IP Range:** The IP range of the SSH servers you want to attack, e.g. "192.168.1.0/24"
     * **Username List:** The list of usernames you want to try, e.g. "admin,user,root"
     * **Password List:** The path to the password list you want to use, e.g. "/usr/share/wordlists/rockyou.txt"
     * **Proxy List:** The list of proxy servers you want to use, e.g. "127.0.0.1:8080,192.168.1.100:3128" (optional)
   * Once you have entered all the required information, ShadowStrike will start the brute force attack.
   * The tool will generate a report summarizing the successful and unsuccessful login attempts and log all relevant information to a file named "shadowstrike.log".

**Additional Information**

* ShadowStrike is for educational purposes only and should not be used for malicious activities.
* Always obtain proper authorization before conducting any security assessments or penetration tests.
* For more information about ShadowStrike, please refer to the GitHub repository: https://github.com/byt3bl33d3r/ShadowStrike

**Examples**

* To attack a single SSH server with a specific username and password list, you can use the following command:
  ````
  shadowstrike -i 192.168.1.100 -u admin -p /usr/share/wordlists/rockyou.txt
  ```
* To attack multiple SSH servers with a list of usernames and passwords, you can use the following command:
  ````
  shadowstrike -i 192.168.1.0/24 -u admin,user,root -p /usr/share/wordlists/rockyou.txt
  ```
* To attack SSH servers using a list of proxy servers, you can use the following command:
  ````
  shadowstrike -i 192.168.1.0/24 -u admin,user,root -p /usr/share/wordlists/rockyou.txt -x 127.0.0.1:8080,192.168.1.100:3128
  ```

**Troubleshooting**

* If you encounter any issues with ShadowStrike, please refer to the GitHub repository for troubleshooting tips and support: https://github.com/byt3bl33d3r/ShadowStrike/issues
