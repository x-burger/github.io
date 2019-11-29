---
title: Já existem chaves SSH?
layout: post
tags: [SSH, github]
---
Antes de gerar nova chave iremos conferir as existentes.

  * Nota: as chaves DSA foram descontinuadas no OpenSSH 7.0. Se o seu sistema operacional usar o OpenSSH, você precisará usar um tipo alternativo de chave ao configurar o SSH, como uma chave RSA. Por exemplo, se o seu sistema operacional for o MacOS Sierra, você poderá configurar o SSH usando uma chave RSA.

No terminal digite:

```bash
ls -al ~/.ssh
# Lists the files in your .ssh directory, if they exist
```

Por padrão deve existir algum desses arquivos/chaves:

```
id_dsa.pub
id_ecdsa.pub
id_ed25519.pub
id_rsa.pub

```

Se tiver algum par de chaves pública/privada ( por exemplo, id_rsa.pub e id_rsa ) e quiser usar para conectar com o Github, você pode adicioná-la ao ssh-agent.

  * Dica: Se você receber um erro que ~ / .ssh não existe, não se preocupe! Vamos criá-lo quando gerarmos uma nova chave SSH.

[Fonte](https://help.github.com/articles/checking-for-existing-ssh-keys)

***
mail me: marcio at sieburger dot link