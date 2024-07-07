---
title: "Criar redirecionamento usando Docker"
tags: Docker
---

**Instruções:**
1. Edite o código alterando a variável de ambiente **SERVER_REDIRECT** colocando sua url.
2. **SERVER_REDIRECT_CODE** define os tipos de redirecionamentos sendo 301 permanente indicando ao Motor de busca (Search Engine) que a página antiga não está mais disponível e 302 indica que a página antiga ainda está disponível e que o redirecionamento é temporário.

## › Código

```
docker run --detach --restart=always \
 -e SERVER_REDIRECT_SCHEME=https \
 -e SERVER_REDIRECT=example.com \
 -e SERVER_REDIRECT_CODE=302 -p 80:80 \
 devbuilder/redirecionamento:v1
```

PAGUE-ME O CAFÉ: [Doar Satoshi Bitcoin](https://gravatar.com/sharebitcoin)

<div style='text-align:center;'>

###### Projeto está sob a licença MIT.

</div>