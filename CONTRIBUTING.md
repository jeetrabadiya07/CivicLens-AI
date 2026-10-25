# Contributing to CivicLens AI

Thank you for your interest in contributing to **CivicLens AI**! This project was created as an open-source civic technology platform for **Hacktoberfest 2026 × GDG Cloud Rajkot**.

## Getting Started

1. **Fork the Repository** on GitHub.
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/your-username/civiclens-ai.git
   cd civiclens-ai
   ```
3. Set up the Python backend:
   ```bash
   cd backend
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate

   pip install -r requirements.txt
   python scripts/seed_demo.py
   python scripts/evaluate.py
   ```
4. Set up the React frontend:
   ```bash
   cd ../frontend
   npm install
   npm run dev
   ```

## Development Guidelines

### 1. Code Standards
* **Backend**: Python 3.11+, typed FastAPI endpoints, Pydantic v2 schemas, SQLAlchemy models.
* **Frontend**: React 18, TypeScript, Tailwind CSS, reusable components. Avoid using `any` wherever possible.
* **AI & Algorithms**: Use the open-weight embedding model `sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2`. Never replace local open-source AI with proprietary paid APIs.

### 2. Running Automated Tests
Before submitting a Pull Request, run the backend test suite:
```bash
cd backend
python -m unittest discover tests
```
And verify that the frontend builds without TypeScript errors:
```bash
cd frontend
npm run build
```

### 3. Submitting Pull Requests
1. Create a descriptive branch:
   ```bash
   git checkout -b feature/improved-category-clustering
   ```
2. Commit your changes with conventional commit messages:
   ```bash
   git commit -m "feat(scoring): add adaptive decay sigma for sanitation issues"
   ```
3. Push to your branch and open a Pull Request against `main`.
4. Document any configuration changes or performance benchmarks in your PR description.
