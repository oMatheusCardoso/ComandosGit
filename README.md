# Aqui está um guia rápido de comandos Git!

## Inicializar e configurar

```
git init                     # inicia um repositório local
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
git remote add origin URL    # conecta repositório local ao remoto (GitHub)
```

## Status e histórico

```
git status        # mostra arquivos modificados e prontos para commit
git log           # histórico de commits
git log --oneline # histórico resumido
```

## Adicionar e salvar mudanças

```
git add .                     # adiciona todos os arquivos modificados
git add nome_arquivo.py       # adiciona um arquivo específico
git commit -m "mensagem"      # cria commit com mensagem
```

## Subir para o GitHub

```
git push origin main          # envia para o branch main no GitHub
git push -u origin main       # primeira vez, define upstream
```

## Atualizar com o que está no GitHub

```
git pull origin main          # baixa mudanças do GitHub
git pull --rebase origin main # baixa e reorganiza sua linha do tempo
```

## Branches

```
git branch                    # lista branches
git branch nova-feature       # cria novo branch
git checkout nova-feature     # troca para o branch
git checkout -b nova-feature  # cria e já troca
git merge nova-feature        # junta branch no atual
```

## Desfazer coisas

```
git restore nome_arquivo.py       # desfaz mudanças não adicionadas
git reset HEAD nome_arquivo.py    # remove do "git add"
git reset --hard HEAD             # volta tudo para o último commit
```

## Outros úteis

```
git clone URL                    # clona repositório do GitHub
git diff                         # mostra mudanças no código
git rm nome_arquivo.py           # remove arquivo do repositório
```

---

**Dica:** use sempre `git status` e `git log --oneline` para entender o estado do seu repositório.

---

