### Olá, eu sou a Stefanie Cristinie, Estagiário de TI | Estagiário de Desenvolvimento de Software! 👋

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=stefaniecristinie&layout=compact&theme=radical)](https://github.com/stefaniecristinie)
 
<div>
<a href="https://github.com/stefaniecristinie"><img height="50cm" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original-wordmark.svg"><img height="50cm" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-plain-wordmark.svg"><img height="50cm" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-plain-wordmark.svg"><img height="50cm" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-plain.svg"></a>
<img height="150cm" align="right" src="https://github.com/stefaniecristinie/stefaniecristinie/blob/main/6m7kug.gif">
</div>


##

<div>
<a href="https://www.linkedin.com/in/stefaniecristinieti"><img height="30cm" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"></a>
</div>

![Snake animation] (https://github.com/stefaniecristinie)

name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
