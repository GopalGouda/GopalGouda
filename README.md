<!-- Animated header - replace GIF_URL with an actual GIF URL or keep as-is to add later -->
<p align="center">
  <img src="https://raw.githubusercontent.com/GopalGouda/sigma-prime-learning/main/assets/animated-header.gif" alt="header" width="900"/>
</p>

<h1 align="center">Hi 👋, I'm Gopal (GopalGouda)</h1>
<p align="center">MERN Stack • DSA • AI/ML • Building in public • Sigma Prime learner</p>

---

<!-- BADGES -->
<p align="center">
  <!-- Primary stats -->
  <img src="https://github-readme-stats.vercel.app/api?username=GopalGouda&show_icons=true&theme=dark&count_private=true" alt="GitHub Stats" />
  &nbsp;
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=GopalGouda&layout=compact&theme=dark" alt="Top Languages" />
</p>

<p align="center">
  <!-- Streak with fallback (demolab recommended) -->
  <img src="https://streak-stats.demolab.com?user=GopalGouda&theme=dark" alt="GitHub Streak" />
  &nbsp;
  <!-- Optional: profile views badge -->
  <img src="https://komarev.com/ghpvc/?username=GopalGouda&label=Profile%20views&color=0e75b6&style=flat" alt="Profile views" />
</p>

---

## 🔭 Current Focus
- MERN stack: React + Node + Express + MongoDB (building full-stack projects)
- DSA: daily problem solving (arrays, linked lists, trees, DP)
- AI/ML: Python, Numpy, Pandas, scikit-learn — small ML projects

---

## 📊 Contribution Graph (visual)
<!-- Local path to the generated contribution-style image; your tooling will convert this into a hosted URL -->
![Contribution Graph](/mnt/data/github_snake_GopalGouda.png)

> To use the image from your repo after you upload it to `assets/contrib-graph.png` use:
> `![Contribution Graph](https://raw.githubusercontent.com/GopalGouda/sigma-prime-learning/main/assets/contrib-graph.png)`

---

## 🛠️ Tech Stack
**Frontend:** HTML, CSS, JavaScript, React  
**Backend:** Node.js, Express  
**Database:** MongoDB  
**ML:** Python, Numpy, Pandas, scikit-learn  
**Tools:** Git, VS Code, Postman, Figma

---

## 📁 Projects & Repos
- `mern-blog-app` — Full-stack blog with authentication and CRUD  
- `dsa-practice` — DSA solutions grouped by topic (Arrays, Strings, Trees)  
- `ml-house-price` — Regression model demo  

(Use `@` to link actual repos once created: `https://github.com/GopalGouda/mern-blog-app`)

---

## 📅 Daily Learning / Auto logs (script + GitHub Action)

### 1) Daily generation script (save as `.github/scripts/gen_daylog.sh`)
This script creates `Daily-Logs/Day-<NN>.md` automatically:
```bash
#!/usr/bin/env bash
set -e
mkdir -p Daily-Logs

# compute next day number
last=$(ls Daily-Logs | grep -E '^Day-[0-9]+\.md$' | sed -E 's/Day-([0-9]+)\.md/\1/' | sort -n | tail -1)
if [ -z "$last" ]; then
  next=1
else
  next=$((last+1))
fi

pad=$(printf "%02d" $next)
file="Daily-Logs/Day-${pad}.md"

cat > "$file" <<EOF
# 📅 Day ${next} — Learning Log

## 🚀 What I Learned Today

### 📘 MERN
- Learned:
- Practiced:
- Notes:

### 🧠 DSA
- Problems Solved:
- Concepts Learned:

### 🤖 AI / ML
- Learned:
- Practiced:

## 📝 Summary
(Write a short summary)

## 🔗 Links
- Code:
- Notes:
EOF

git add "$file"
git commit -m "chore(daily-log): add Day ${pad}"
git push origin HEAD
