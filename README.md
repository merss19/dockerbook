sudo usermod -aG docker
docker run -i -t debian зайти в контейнер
docker ps - инфа о всех контайнерах
docker inspect больше инфо о контайнере
docker logs список всех событий, произошедших внутри заданного контейнера:
docker diff список файлов, измененных в работающем контейнере;
docker commit cowsay test/cowsayimage
---------------Dockerfile------------
RUN определяют команды, выполняемые в  командной оболочке внутри данного образа.
docker build -t test/cowsay-dockerfile . -  создать образ
docker run test/cowsay-dockerfile /usr/games/cowsay "Moo" - запускать образ
ENTRYPOINT ["/usr/games/cowsay"] - команды для запуска внутри образа
