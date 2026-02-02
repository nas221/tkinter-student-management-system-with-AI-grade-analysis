# Study Companion

A Tkinter-based study productivity app with login/registration, Pomodoro timer, to-do list, flashcards, and grade tracking with simple analytics.

## Features
- Login/Register with SQLite storage
- Pomodoro timer with study session tracking
- To-do list with due dates and priority cues
- Flashcards (create/import/ratings/stats)
- Grade tracker with charts and basic trend analysis

## Requirements
- Python 3.11+
- Packages listed in `requirements.txt`

## Run locally
```bash
python main
```

## Run with Docker (macOS + XQuartz)
1) Install XQuartz and enable: Preferences -> Security -> Allow connections from network clients.
2) Open XQuartz, then in a host terminal run:
```bash
xhost +localhost
```
3) Build and run:
```bash
docker build -t studycomp .

docker run --rm \
  -e DISPLAY=host.docker.internal:0 \
  -v /tmp/.X11-unix:/tmp/.X11-unix \
  -v "$PWD":/app \
  -w /app \
  studycomp
```

## Data
All data is stored in a local SQLite database file: `todo.db`.

## Notes
- The app will create required database tables on first run.
- If you want a full scikit-learn based analysis, add `scikit-learn` to `requirements.txt`.
# tkinter-student-management-system-with-AI-grade-analysis
