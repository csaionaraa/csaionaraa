### Hii! I'm Carla Saionara, welcome :)
- 🌱 Estou estudando JavaScript

![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=csaionaraa&show_icons=true)
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=csaionaraa&layout=compact)](https://github.com/anuraghazra/github-readme-stats)


![Snake animation](https://github.com/csaionaraa/csaionaraa/blob/output/github-contribution-grid-snake.svg)
  
<div><br>
 <img align="center" alt="Vue" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original-wordmark.svg" />
 <img align="center" alt="HTML" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" />
 <img align="center" alt="CSS" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg"/>
 <img align="center" alt="JS" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg"/>
 <img align="center" alt="Python" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg"/>
 <img align="center" alt="PHP" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" />
 <img align="center" alt="Java" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original-wordmark.svg" />
 <img align="center" alt="MySQL" height="30" width="40" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original-wordmark.svg" />
</div>
 
<div> 
  <a href = "mailto:csaionaraa@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="//www.linkedin.com/in/carla-saionara-araujo-47b14a226" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
</div>

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
          github_user_name: jxhnlcs
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
