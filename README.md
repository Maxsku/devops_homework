docker build . -t max/node - побудова і таггінг докерімеджу 
docker images - перевірив імедж
docker run -p 9000:80 -d --cpu-period=50000 --cpu-quota=25000 --memory=512m max/node - заранив контейнер з обмеженням по меморі (обмеження по кількості мб, які контейнер може використати) і cpu (обмеження по довжині циклу  і кількості циклів за період)
docker ps - подивився всі раннінг/стопед контейнери
docker stats - перевірив стати контейнера, чи дійсно обмеження працюють
docker login - залогінився в докер хаб
docker tag max/node:latest maxskurativskyi/devops_homework - створив таг
docker push maxskurativskyi/devops_homework - запушив імедж на докер хаб