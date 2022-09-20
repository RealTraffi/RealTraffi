#sobre mim
- 👋 Ola Meu Nome É @RealTraffi
- Meu Email De Contato é guilherme.leme@escola.pr.gov.br
- 👀 Eu estou interessado em aprender a programar
- 🌱 Eu estou aprendendo a programar recentemente

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="40" height="40"/>
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" width="40" height="40"/> <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" width="40" height="40"/>

<div>
<a href="https://www.youtube.com/seu-canal-youtube-aqui" target="_blank"><img src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white" target="_blank"></a>
<a href="https://instagram.com/seu-usuário-instagram-aqui" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
<a href="https://www.twitch.tv/seu-usuário-aqui" target="_blank"><img src="https://img.shields.io/badge/Twitch-9146FF?style=for-the-badge&logo=twitch&logoColor=white" target="_blank"></a>
<a href = "mailto:contato@seu-usuário-aqui"><img src="https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
<a href="https://www.linkedin.com/in/seu-usuário-linkedln-aqui" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>   
</div>

<div>
<a href="https://github.com/seu-usuário-aqui">
<img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=seu-usuário-aqui&layout=compact&langs_count=7&theme=dracula"/>
<img height="180em" src="https://github-readme-stats.vercel.app/api?username=seu-usuário-aqui&show_icons=true&theme=dracula&include_all_commits=true&count_private=true"/>
</div>
name: Traffi

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
          github_user_name: seu-usuário-aqui
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

