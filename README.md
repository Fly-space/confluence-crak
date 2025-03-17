# Настройка Confluence с PostgreSQL

## Зависимости:

### Установить файл задачи
* [taskfile](https://taskfile.dev/installation/)

### установить docker
* [docker installation](https://docs.docker.com/get-docker/)

### установить git
* [git installation](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

### скачать attlassian-agent-use-in-JAVA_OPTS.jar и atlassian-agent-license-generator.jar
* [Licence Generator](https://drive.google.com/drive/folders/1z1ImzAvd3FngSJq6AiD6be_kDwYDD1RA?usp=drive_link)

### репозиторий для клонирования
    git clone https://github.com/Fly-space/confluence-crack

### В вашем каталоге должны быть следующие файлы
--> Dockerfile
<br/>
--> docker-compose.yml
<br/>
--> Taskfile.yml
<br/>
--> atlassian-agent-use-in-JAVA_OPTS.jar
<br/>
--> atlassian-agent-license-generator.jar
<br/><br/>

# Используйте следующие команды для запуска и взлома Confluence:

## Запустить Dockerfile
    task build (в image: example.com/confluence:8.0.3 ставим нужную версию confluence)

## создать файл в docker compose 
    task up

## Создание лицензии для вашего сервера Confluence. пожалуйста, скопируйте сгенерированный код и вставьте его на стартовую страницу
    task gen -- "input serverID"

## Если вы установили плагин на confluence, вы можете использовать следующую команду для создания лицензии
    task plugin -- "input plugin app key"

# При необходимости вы также можете использовать следующие команды

## отправьте свое изображение в реестр изображений (необязательно)
    task push

## создать файл в docker compose (необязательно)
    task down
