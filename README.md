Web Scraping 

Web Scraping deals with information retrieval, news gathering, web monitoring, competitive marketing and more. 
The use of web scraping makes accessing the vast amount of information online, easy, and simple. 

This Web Scraping application extracting news information by following below steps:
  1: Making an HTTP request to a server
  2: Extracting and parsing (or breaking down) the website’s relevant data
  3: Saving the relevant data locally

Consideration for web application:

  1. HTTP GET request: use urllib3
  2. News Portal: ekantipur (https://ekantipur.com/(category news))
  3. Python Package: beautifulsoup4 (For parsing Web site HTML content and extracting information)
  4. Extracted information will be save into a .CSV file as well as into a SQLite database table.
  5. SQLiteStudio used to validate database table entries


**Custom functions:**
1.  Scrap News: scrap_news_articles()
  *   This function will extract all the news into a dataframe, save the records into a .CSV file for data analysis

2. Create Database Connection:create_db_connection()
  *   This function will create a database connection to the SQLite database
      specified by the file (dbfile)

3. Create databse table and insert records:create_table_records()
  * This function establish a connection to the SQLite database using connection object,create a cursor object. Using cursor create the table and insert records

4. Save News:saved_scrap_news_articles()
  *   This function will use SQLite database engine to create a table and store the extracted news
  *   This function will require the daily news dataframe as input to update the table

5. Select records from table :select_all_records()
   *  This function will use the database connection, cursor object to fetch all the recods from the database table
