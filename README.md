# StockPilot AI

StockPilot AI is a Streamlit-based inventory command center with forecasting, deadstock analysis, transfer optimization, and role-based workspace access.

## Run Locally

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
streamlit run app2.py
```

## Deploy To Streamlit Community Cloud

1. Push this repository to GitHub.
2. Go to Streamlit Community Cloud: https://share.streamlit.io/
3. Create a new app:
- Repository: your GitHub repo
- Branch: `main`
- Main file path: `app2.py`
4. In **App Settings -> Secrets**, add:

```toml
DATABASE_URL = "postgresql+psycopg2://USER:PASSWORD@HOST:5432/DBNAME"
```

5. Deploy.

## Persistence Notes

- If `DATABASE_URL` is set, app data persists in Postgres.
- If not set, the app falls back to local SQLite (`stockpilot.db`), which is not durable on Streamlit Cloud.

## Demo Users

- `admin / admin123`
- `manager / manager123`
- `ops / ops123`

Change these after first login for production use.
