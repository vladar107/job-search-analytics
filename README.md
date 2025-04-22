# Job Search Analytics

A data analysis tool for tracking and visualizing job application progress using data stored in Notion.

## Description

This project connects to a Notion database containing job application data and provides comprehensive analytics to help you understand your job search process. It analyzes application patterns, success rates, and timelines, providing visualizations for different aspects of the job search process.

## Features

- **Data Retrieval**: Connect to Notion database and extract job application data
- **Job Category Analysis**: Visualize applications by job category and rejection reasons
- **Response Time Analysis**: Analyze the distribution of response times between application and decision
- **Application Rate Tracking**: Track application rates over time by job category
- **Application Funnel Analysis**: Visualize your application funnel from initial application to offer
- **Conversion Rate Analysis**: Calculate conversion rates between different stages of the application process
- **Job Type Specific Analysis**: 
  - **Engineering Roles**: Analyze conversion rates for Technical Lead, Senior Engineer, and Staff Engineer positions
  - **Architecture Roles**: Analyze conversion rates for Post Sale Engineer, Sales Engineer, and Software/Solution Architect positions

## Prerequisites

- Python 3.6+
- A Notion account with a database for tracking job applications
- Notion API token

## Installation

1. Clone the repository:
   ```
   git clone <repository-url>
   cd job-search-analytics
   ```

2. Create a virtual environment:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install the required packages:
   ```
   pip install -r required.txt
   ```

4. Create a `.env` file in the project root with your Notion credentials:
   ```
   NOTION_TOKEN="your_notion_api_token"
   NOTION_DB_ID="your_notion_database_id"
   ```

## Notion Database Setup

Your Notion database should have the following properties:
- **Name**: Title of the job application
- **Job Category**: Multi-select field for job categories
- **Status**: Select field for application status (Applied, Screening Invited, Interview In Progress, Offer, Rejected)
- **Applied**: Date field for when you applied
- **End Date**: Date field for when the application process ended
- **Reject Reason**: Multi-select field for rejection reasons

## Usage

1. Ensure your Notion database is properly set up and your `.env` file contains the correct credentials.

2. Run the Jupyter notebook:
   ```
   jupyter notebook analytics-1.ipynb
   ```

3. Execute the cells in the notebook to generate analytics and visualizations for your job search data.

## Dependencies

- pandas: Data manipulation and analysis
- numpy: Numerical operations
- requests: HTTP requests
- notion_client: Notion API client
- matplotlib: Data visualization
- dotenv: Loading environment variables from .env files

## License

[MIT License](LICENSE)
