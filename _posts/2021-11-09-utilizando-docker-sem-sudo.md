---
layout: post
title: 'Utilizando Docker sem Sudo'
image: /assets/images/example4.jpg
tags:
  - tag
status: publish
date: 2021-11-09
---
# Utilizando Docker sem Sudo

É um pouco chato ter que utilizar o  **sudo**  toda hora que você quer executar um container ou um compando do docker, mas é bem simples de resolver esse problema.

Abaixo seguem os comandos que devem ser executados para resolução desse problema:

```
$ sudo groupadd docker
$ sudo usermod -aG docker $USER
$ newgrp docker
$ docker run hello-world
```

Depois disso, talvez seja necessário reiniciar o seu computador, mas assim que ele reiniciar, você já poderá executar os comandos sem o  **sudo**.