# AirLine-Analysis

Post COVID, especially in the year 2023, the airline industry faced significant financial challenges . This included flight cancellations, travel restrictions, and a decrease in passengers, leading to financial losses for airlines. To adapt to these changes, airlines had to ground planes, reduce flight schedules, and increase spending on cleaning and safety measures. While governments provided financial aid, passengers still experienced issues with fluctuating ticket prices and flight delays. Overall, this period was difficult for both airlines and travellers. The sad thing is that the situation is continuing.

Flight delays can occur for various reasons such as maintenance issues, bad weather, airport problems, late-arriving planes, and security issues. These delays not only cost airlines money but also inconvenience to passengers.

Our project aims to understand why flights are delayed and how it impacts the airline industry. By analysing historical flight data, we hope to identify patterns and solutions to make air travel smoother.

Guide to the Files :

• The Queries_Visualtions python file shows how we used SQL queries by connecting Google BigQuery to Jupyter notebook and plotted some bar charts to show the visualisation of the query output. • Data_Cleaning python file shows the steps in cleaning the dataset. • The image file refers to simple queries which shows the count of Holidays for each month and local holiday count for each month to check if holidays effect delays in particular months.

Steps to Connect Google BigQuery to Jupyter Notebook

Package Installation: Begin by ensuring that the required Python packages are installed in your Jupyter environment. The primary package needed is "google-cloud-bigquery," which facilitates interactions with BigQuery. You can install it via pip in the terminal: pip install google-cloud-bigquery

Creating a Service Account: • Navigate to the Google Cloud Console (https://console.cloud.google.com/). If you don't have a Google Cloud account, you must sign up for one. • Create a new project or select an existing one from the top navigation bar. Ensure that the selected project contains the BigQuery datasets you intend to access. • Go to IAM & Admin > Service Accounts from the left-hand navigation menu. • Click "Create Service Account" at the top of the page. Provide a name for the service account (e.g., "bigquery-notebook-access") and optionally a description. • Grant the necessary permissions to the service account in the "Service account permissions" section. At least assign the "BigQuery User" role to enable query execution on datasets. • Generate a private key for the service account, selecting JSON as the key type. Save the downloaded JSON file containing the service account credentials securely on your local machine.

Setting up Authentication in Jupyter Notebook: • Open your Jupyter Notebook and set the GOOGLE_APPLICATION_CREDENTIALS environment variable to the path of your credentials JSON file. This informs the google-cloud-bigquery library about the location of your credentials.

Code: import os os.environ["GOOGLE_APPLICATION_CREDENTIALS"] = "/path/to/your/credentials.json"

Testing the Connection: Verify the connection to BigQuery by executing sample queries within your Jupyter Notebook using the google-cloud-bigquery library.
Performing ETL : https://cloud.google.com/architecture/performing-etl-from-relational-database-into-bigquery
