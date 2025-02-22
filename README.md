# Carbon Intensity Data Visualization

This project fetches carbon intensity data from an external API, stores it in a MongoDB database, and visualizes it using Dash.

## Prerequisites

Ensure you have the following installed:

- Python 3.7 or later
- MongoDB Atlas (or a local MongoDB instance)
- Internet access to fetch data from the Carbon Intensity API

## Installation

<b>1. Clone the repository (if applicable):</b>
   ```sh
   git clone <repository-url>
   cd <repository-folder>
   ```
<b>2. Create and activate a virtual environment (optional but recommended):</b>
```python
python -m venv venv
source venv/bin/activate  # On macOS/Linux
venv\Scripts\activate     # On Windows
```

**3. Install the required dependencies:**
```sh
pip install -r requirements.txt
```

## <b>Configuration:</b>
The MongoDB connection string is already included in the code. Ensure your MongoDB Atlas cluster is accessible.
The dataset is pulled from https://api.carbonintensity.org.uk/ and stored in MongoDB collections.

## <b>Running the application</b>

<b>1. Start the Dash app:</b>
```sh
python app.py
```

<b>2.Access the dashboard in your browser:</b>
```html
http://127.0.0.1:8050/
```

## Features

Fetches Carbon Intensity Data: Retrieves and stores data from the API.
Database Storage: Saves data in MongoDB for further analysis.
Visualization:
- Line graph for average, min, and max carbon intensity over time.
- Bar chart for forecast intensity by region.
- Pie chart for generation mix based on the selected region.

## Notes
The MongoDB collection has a `TTL` index that automatically deletes documents after 1 hour.
The debug=True flag is enabled for development. Disable it for production.
