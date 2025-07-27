<h1 align="center">Hi 👋, I'm Gautam Singh</h1>
<h3 align="center">A passionate Full Stack Developer from India</h3>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=gautam-singh&label=Profile%20views&color=0e75b6&style=flat" alt="gautam-singh" />
</p>

---

### 🧰 Languages and Tools

<p align="center">
  <img src="https://skillicons.dev/icons?i=html,css,js,react,nodejs,java,spring,mysql,mongodb,git,github,linux" />
</p>

---

### 📈 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=gautam-singh&show_icons=true&theme=radical" alt="stats" />
</p>

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com?user=gautam-singh&theme=radical" />
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=gautam-singh&layout=compact&theme=radical" />
</p>

---

### 📊 Contribution Graph

<p align="center">
  <img src="https://github-readme-activity-graph.cyclic.app/graph?username=gautam-singh&theme=dracula" />
</p>
name: Update README with UTC Time

on:
  schedule:
    - cron: "0 * * * *"
  workflow_dispatch:

jobs:
  update-readme:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Update README
        run: |
          echo "Last updated at: $(date -u)" > README.md
          cat <<EOF >> README.md

## ⏰ This README auto-updates every hour!

EOF

      - name: Commit and Push
        run: |
          git config --global user.name 'GitHub Actions'
          git config --global user.email 'actions@github.com'
          git add README.md
          git commit -m "Update README with time"
          git push
