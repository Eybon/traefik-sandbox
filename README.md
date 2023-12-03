# traefik-sandbox

Projet sandbox pour tests de l'outil Traefik

## :speech_balloon: Infos

Lancement via `docker-compose`
```sh
sudo docker compose up -d
```

### Traefik

La console est exposé sur le port `8081` :
- En local via http://localhost:8081
- En local en passant par un fake dns via http://test.domaine.localhost:8081
- Sur un réseau local par exemple via http://192.168.1.70:8081/

### Reverse-proxy 

Le conteneur Traefik fait reverse-proxy vers plusieurs autres conteneurs utilisés pour tester le reverse-proxy

| App  | Port | Commentaire                                  | Repo                                             |
|:----:|------|----------------------------------------------|--------------------------------------------------|
| app1 | 8091 | App qui affiche juste un "hello-world"       | https://github.com/Eybon/docker-sandbox          |
| app2 | 8092 | App qui fournit des infos OS et HTTP Request | https://github.com/traefik/whoami                |
| app3 | 8093 | App "hello-world" pour du test               | https://github.com/opsxcq/docker-helloworld-http |



## :book: Documentations

|            Doc             | Lien                                                                                     |
|:--------------------------:|------------------------------------------------------------------------------------------|
| Doc Traefik docker-compose | https://doc.traefik.io/traefik/user-guides/docker-compose/basic-example/                 |
|  Reverse-proxy pas à pas   | https://anceret-matthieu.fr/2022/05/traefik-a-modern-reverse-proxy/                      |
|    Reverse-proxy docker    | https://blog.alterway.fr/traefik-un-reverse-proxy-pour-vos-conteneurs.html               |
|   Reverse-proxy détaillé   | https://blog.eleven-labs.com/fr/utiliser-traefik-comme-reverse-proxy/                    |
|      Traefik redirect      | https://www.benjaminrancourt.ca/how-to-redirect-a-domain-to-another-domain-with-traefik/ |
|      Traefik redirect      | https://jensknipper.de/blog/traefik-redirect-to-external-domain/                         |

