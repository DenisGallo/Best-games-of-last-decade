# 🎮 Game Recommender from Metacritic

This Python script scrapes **Metacritic** for video games released in the last 10 years and generates a recommendation list filtered by games you’ve already played and titles on a blacklist.

## 📋 Features
- Automatically fetches Metacritic pages listing games released between **9 years ago** and the current year.
- Filters out:
  - Games you’ve already played (`already_played.txt`)
  - Blacklisted games (`blacklist.txt`)
- Uses **randomized user-agents** to reduce the risk of being blocked.
- Applies a **5-second delay** between requests to avoid rate limiting.
- Calculates the number of recommendations proportionally to the games already played (it starts with 5 games and adds 5 games for every game already played, up to a maximum of 100).

## 🛠 Requirements
- Python 3.8+
- Jupyter Notebook
- Python libraries:
  ```bash
  pip install requests beautifulsoup4 python-dateutil
  ```

## 📂 File Structure

-    already_played.txt – List of games you’ve already played (one per line).

-    blacklist.txt – List of games to exclude (one per line).

-    recommender.ipynb – The Python script (as jupyter notebook).

## 🚀 How to Use

Clone or download the project.

Make sure already_played.txt and blacklist.txt contain the desired data.

Run the notebook: recommender.ipynb

The script will return a list of recommended titles based on the filters.

## ⚠️ Notes

Metacritic’s HTML structure may change: if that happens, update the BeautifulSoup parsing accordingly.

Excessive usage may violate Metacritic’s Terms of Service – use responsibly.

If the number of games already played is high, the number of recommendations may be capped at 100.

## 📜 License

This project is licensed under the MIT License. Feel free to use and modify it, respecting the data source’s terms.

## 👨‍💻 Roadmap

Possbile future upgrades:
- Dockerized WebApp
- Multi-user features
- Terraform AWS deployment readiness
