## home page 

## profile

## meal paln
# Nepali Diet Planner — Full Stack

```
nepali-diet-planner/
├── backend/    Django + DRF API (see backend/README.md)
└── frontend/   React + Vite client (see frontend/README.md)
```

## Run both together

**Terminal 1 — backend:**
```bash
cd backend
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py seed_data
python manage.py train_decision_tree
python manage.py runserver
```
Runs at http://localhost:8000, API under `/api/`.

**Terminal 2 — frontend:**
```bash
cd frontend
npm install
cp .env.example .env
npm run dev
```
Runs at http://localhost:5173 and talks to the backend via `VITE_API_URL`.

Open http://localhost:5173, sign up, complete the health assessment, then
generate a meal plan.


