<h2 align="left">Olá👋! Meu nome é Miguel e sou estudante de programação🖥️</h2>

###

<img align="right" height="150" src="https://images.steamusercontent.com/ugc/938307470432973677/E7E61ECA5C6F8C8A2E42915CDC52CFB8ED14BCCE/?imw=5000&imh=5000&ima=fit&impolicy=Letterbox&imcolor=%23000000&letterbox=false"  />

###

<div align="left">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="30" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="30" alt="html5 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="30" alt="css3 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="30" alt="python logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" height="30" alt="github logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" height="30" alt="vscode logo"  />
</div>

###

<div align="left">
  <img src="https://img.shields.io/static/v1?message=Instagram&logo=instagram&label=&color=E4405F&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="instagram logo"  />
  <img src="https://img.shields.io/static/v1?message=Discord&logo=discord&label=&color=7289DA&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="discord logo"  />
  <img src="https://img.shields.io/static/v1?message=Stackoverflow&logo=stackoverflow&label=&color=FE7A16&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="stackoverflow logo"  />
  <img src="https://img.shields.io/static/v1?message=HackerRank&logo=hackerrank&label=&color=2EC866&logoColor=white&labelColor=&style=for-the-badge" height="35" alt="hackerrank logo"  />
</div>

###

name: Generate snake animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - master

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: generate snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: dist/snake.svg?palette=github-dark


      - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

###

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Miguel-Deniss&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=blue-green&locale=pt-br&hide_border=true&order=1" height="130" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=Miguel-Deniss&locale=pt-br&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=blue-green&hide_border=true&order=2" height="130" alt="languages graph"  />
  <img src="https://streak-stats.demolab.com?user=Miguel-Deniss&locale=pt-br&mode=daily&theme=blue-green&hide_border=true&border_radius=5&order=3" height="150" alt="streak graph"  />
</div>

###
