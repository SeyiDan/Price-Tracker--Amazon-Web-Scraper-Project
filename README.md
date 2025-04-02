# Amazon Web Scraper Project

A Python-based web scraping application that automatically tracks Amazon product prices over time, saves the data to a CSV file, and optionally sends email notifications when prices drop below a specified threshold.

## Features

- Scrapes product information from Amazon product pages
- Extracts product title, price, and date
- Saves data to a CSV file for historical price tracking
- Supports automatic periodic checks (configurable interval)
- Email notification system for price drops
- Data visualization capabilities with pandas

## Requirements

- Python 3.6+
- BeautifulSoup4
- Requests
- pandas
- smtplib (built-in)
- csv (built-in)
- datetime (built-in)
- time (built-in)

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/SeyiDan/Price-Tracker--Amazon-Web-Scraper.git
   cd Price-Tracker--Amazon-Web-Scraper
   ```

2. Install required packages:
   ```
   pip install beautifulsoup4 requests pandas
   ```

## Usage

The project is structured as a Jupyter Notebook for easy experimentation and visualization. To use:

1. Open the Jupyter Notebook:
   ```
   jupyter notebook "Amazon Web Scraper Project.ipynb"
   ```

2. Configure the URL in the notebook to the Amazon product you want to track

3. Run the cells to:
   - Test initial scraping
   - Create a CSV file for data storage
   - Configure the automated checking function
   - Set up email notifications (optional)

4. For continuous monitoring, run the timer cell which will check the price at your specified interval (default is daily)

## How It Works

1. **Web Scraping**: Uses BeautifulSoup to parse HTML content from Amazon product pages
2. **Data Extraction**: Identifies and pulls product title, price, and adds current date
3. **Data Storage**: Writes and appends data to a CSV file for tracking over time
4. **Automation**: Can be configured to run checks at specified intervals
5. **Notifications**: Optional email alerts when price drops below threshold

## Customization

- **Product URL**: Change the URL variable to track different products
- **Check Frequency**: Modify the `time.sleep()` value (in seconds) in the timer cell
- **Price Threshold**: Adjust the price threshold in the `check_price()` function
- **Email Settings**: Update email configuration in the `send_mail()` function

## Important Notes

- Amazon frequently updates their website structure, so selectors may need updating
- Using proper headers in requests helps prevent being blocked
- For production use, consider adding error handling and logging
- Email notification requires setting up an app password if using Gmail

## Sample Output

The script generates a CSV file with the following structure:

| Title | Price | Date |
|-------|-------|------|
| Got Data Funny Business Data Analyst T-Shirt | 15.99 | 2025-02-24 |
| ... | ... | ... |

## Privacy and Legal Considerations

- Ensure compliance with Amazon's Terms of Service
- Do not make excessive requests in short periods
- Use responsibly and for personal use only
