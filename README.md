# ForecastinQ — Team B

An intelligent sales forecasting and inventory management web application built with Flask and SQLite.

**Repository:** [ForecastIQ-TeamB](https://github.com/vivek-kumar-kandu/ForecastIQ-TeamB)

## Features

- Dashboard with sales and business summaries
- Sales recording and reporting
- Product catalog and inventory tracking
- Low-stock notifications and restocking
- Customer and supplier management
- Sales forecasting
- User registration, login, and role-based user management
- Application settings

## Technology

- Python
- Flask
- SQLite
- HTML, CSS, and JavaScript

## Getting started

Use Python 3.8 or newer.

1. Clone the repository and open the project directory:

   ```bash
   git clone https://github.com/vivek-kumar-kandu/ForecastIQ-TeamB.git
   cd ForecastIQ-TeamB
   ```

2. Create and activate a virtual environment:

   **Windows (PowerShell):**

   ```powershell
   py -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

   **macOS/Linux:**

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Install dependencies and initialize the sample database:

   ```bash
   pip install -r requirements.txt
   python init_db.py
   ```

   **Warning:** `python init_db.py` recreates the SQLite database at `database/forecastinq.db`. Running it again will overwrite that local database.

4. Start the application:

   ```bash
   python app.py
   ```

5. Open [http://localhost:5000](http://localhost:5000) in your browser.

## Demo accounts

The initialized sample database includes these accounts. All use the password `Admin@123`.

| Username | Role |
| --- | --- |
| `admin` | Admin |
| `manager` | Manager |
| `staff` | Staff |

Use demo credentials only for local development. Change the default credentials and configure a strong `SECRET_KEY` before deploying the application.

## Project structure

```text
.
├── app.py                # Flask application and route registration
├── blueprints/           # Authentication and application feature routes
├── config.py             # Application and database configuration
├── database/
│   └── schema.sql        # SQLite schema and sample records
├── db.py                 # Database connection helpers
├── init_db.py            # Database initialization and sample sales
├── requirements.txt      # Python dependencies
├── static/               # CSS and JavaScript
├── templates/            # Jinja templates
└── utils.py              # Shared application utilities
```

## Configuration

The app reads its Flask session signing key from the `SECRET_KEY` environment variable. Set a unique, strong value for any deployment; the built-in fallback is for local development only.

## License

The [MIT License](LICENSE) applies to this project's code. It allows anyone to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the software, including for commercial purposes, as long as the copyright and license notices are included with substantial copies of the software.

The software is provided "as is", without warranty. See the [license text](LICENSE) for the full terms.
