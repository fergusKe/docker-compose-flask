[參考]
文章
https://pythonise.com/series/learning-flask/building-a-flask-app-with-docker-compose
影片
https://www.youtube.com/watch?v=dVEjSmKFUVI&list=PLF2JzgCW6-YY_TZCmBrbOpgx5pSNBD0_L

[安裝_docker]
curl -fsSL get.docker.com -o get-docker.sh
sh get-docker.sh
sudo docker version
sudo systemctl start docker
sudo docker version

[安裝_portainer]
https://www.portainer.io/

```
docker volume create portainer_data
docker run --name=portainer -d -p 9000:9000 -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer
```

之後查看 http://localhost:9000/

[設定不需要輸入_sudo]
https://docs.docker.com/engine/install/linux-postinstall/

[docker-compose]
docker-compose build
docker-compose up -d
docker-compose down -v

docker-compose up --build

[設置變數]
export FLASK_APP=run.py
export FLASK_ENV=development

[啟動服務]
flask run
