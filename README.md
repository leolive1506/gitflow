# Pesquisar
- Diferença entre bugfix e hotfix

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
- relaease branches
    - Conforme, acumulado de feature no **develop**, quando considerado entregável é enviada para esse branch
    - Ambiente de homologação, ambiete de teste
    - Não é criado funcinolidade nesse branch
- hotfixes
    - branch de bugs encontrado no relaese ou outro branch
- feature branches
    - Novas funcionalidades

- Branchs de suporte são automática excluidas do repositório quando dizer que terminou
    - Duas que sempre permanecem são: develop e master

## Comandos
- Iniciar gitflow
```sh
git flow init
```

- Criar uma nova feature
```sh
# start -> começar uma nova
git flow feature start name_branch
```

- Finalizar uma branch
```sh
# start -> começar uma nova
git flow feature finish name_branch
```