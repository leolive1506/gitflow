# Git hub flow
    - Branch master
        - Desevelver -> cria um feature
            - Após terminar, merge com master
        - Algum problema na master criar um bugfix e corrigir
            - Após terminar, merge com master
# Git flow
    - Ditar regras de relacionamenos, padrão de nomenclatura

## Estrutura em 
- master
    - Protegida, não é qualquer um que mexe nela
    - Quanndo testado ja no **release branch**, é enviado para cá
    - Ambiente de produção
- develop
    - Aqui que desenvolve o fluxo, cada feature nova é develvovida na **feature branches**, quando terminada a nova feature, enviada pra develop
    - Recebe todas novas features
- release branches
    - Conforme, acumulado de feature no **develop**, quando considerado entregável é enviada para esse branch
    - Ambiente de homologação, ambiete de teste
    - Não é criado funcinolidade nesse branch
- hotfixes
    - branch de bugs encontrado no relaese ou outro branch
- feature branches
    - Novas funcionalidades

- Branchs de suporte são automática excluidas do repositório quando dizer que terminou
    - Duas que sempre permanecem são: develop e master

# Diferença entre bugfix e hotfix
## Bugfix
    - problemas encontrados e resolvidos durante as fases de produção ou teste ou mesmo após a implantação como parte do ciclo normal de lançamento de um produto
## Hotfixes
    -  são aplicados somente depois que o produto é lançado e está ativo.


## Comandos
- Iniciar gitflow
```sh
git flow init
```

### Feature
- Criar uma nova
```sh
# start -> começar uma nova
git flow feature start name_branch
```

- Subir p git
- Se tiver certo finaliza com ```sh git flow feature finish name_branch```
```sh
git flow feature publish name_branch
```

- Finalizar uma
    - Ao finalizar, ja faz merge na develop e exclui o branch finalizado
```sh
# start -> começar uma nova
git flow feature finish name_branch
```

- Obter uma feature
```sh
git flow feature pull name_branch
```

### Release
- Crirar um nova
```sh
# usado versão no nome, ex: 0.1.0
git flow release start name_branch
```

- Finalizar
    - Após finalizado, atualiza o **master** e o **develop**
    - Força criar tag, normalmetne com o nome (usado versão)
```sh
git flow release start name_branch
```

- Ver as tags
```sh
git tag
```

## Hot fix
- Para criar e terminar uma é o mesmo processo acima
- Branch é criada a partir da master
    - A ideia é "dectou um problema em prod e precisa resolver"
    - Apos finalizaod, atualiza a **master** e **develop**