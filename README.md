# PUNF_Case_Study

# LinkedIn Unread Messages and Notifications Scraper

This repository contains a Python script that scrapes the number of unread messages and notifications from LinkedIn and sends an email with the current counts. It also compares the current counts with the previous counts and updates an Excel file with the data.

## Prerequisites

Before running the script, make sure you have the following:

- Python 3.x installed
- Required Python packages: `selenium`, `openpyxl`, `smtplib`
- Chrome browser installed
- ChromeDriver executable compatible with your Chrome browser version

## Installation

1. Clone this repository to your local machine using the following command:
`git clone https://github.com/ishu116/linkedin-scraper.git`

2. Install the required Python packages using `pip`:
`pip install selenium openpyxl smtplib`

3. Download the ChromeDriver executable for your Chrome browser version and place it in the repository's directory.

## Usage

1. Open the `config.py` file and set the following variables:
- `chromedriver_path`: Path to the ChromeDriver executable
- `username`: Your LinkedIn username or email
- `sender_email`: Your email address (used as the sender of the notification email)
- `sender_password`: Your email password (for authentication)
- `recipient_email`: Email address to receive the notification email
- `SMTP_SERVER`: SMTP server address (e.g., `smtp.gmail.com` for Gmail)
- `SMTP_PORT`: SMTP server port number (e.g., `587` for Gmail)

2. Run the script using the following command:
`python main.py`

3. The script will prompt you to enter your LinkedIn password securely. Enter the password and press Enter.

4. The script will scrape the number of unread messages and notifications from LinkedIn, compare it with the previous data, update the Excel file, and send an email with the current counts.

5. The script will run in an infinite loop, sleeping for 3 hours between each run. You can modify the sleep duration as needed in the code (`time.sleep(3 * 60 * 60)`).

## Excel Data

The script saves the scraped data in an Excel file named `linkedin_data.xlsx`. Each row in the file represents a snapshot of the counts at a specific time. The columns include:

1. Username: LinkedIn username
2. Timestamp: Date and time of the snapshot
3. Unread Messages: Number of unread messages
4. Unread Notifications: Number of unread notifications
5. Unread Messages Comparison: Difference between the current and previous unread messages counts
6. Unread Notifications Comparison: Difference between the current and previous unread notifications counts

## Contributing

Contributions to improve this LinkedIn scraper script are welcome! If you have any ideas, suggestions, or bug fixes, please open an issue or submit a pull request.

## Disclaimer

This script is intended for educational and personal use only. Use it responsibly and respect the LinkedIn terms of service. The author is not responsible for any misuse or violation of LinkedIn's policies.

## Contact

If you have any questions or need further assistance, please feel free to contact [yashpratapr@gmail.com].
