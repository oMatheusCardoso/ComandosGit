# Aqui está um guia rápido de comandos Git!

# Passo a passo para instalar e começar a usar no seu projeto!

## 1. Instalar e configurar Git

* Baixe: [https://git-scm.com/download/win](https://git-scm.com/download/win)
* Marque **Add Git to PATH** durante a instalação.
* Teste:

```powershell
git --version
```

* Configure usuário:

```powershell
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

## 2. Iniciar repositório Git

```powershell
git init
git add .
git commit -m "primeiro commit"
```

## 3. Criar repositório no GitHub

1. Acesse [https://github.com/new](https://github.com/new)
2. Dê um nome (ex: DownTube)
3. Crie vazio (sem README)

## 4. Conectar repositório local ao GitHub

```powershell
git branch -M main
git remote add origin https://github.com/user/nomedoseuprojeto.git
```

## 5. Subir projeto para GitHub

```powershell
git push -u origin main  # envia projeto ao GitHub
```

> Se der erro de non-fast-forward, use:

```powershell
git push origin main --force  # sobrescreve remoto
```

## 6. Próximas alterações

Sempre que alterar código:

```powershell
git add .
git commit -m "mensagem do commit"
git push
```

---

# Somente Comandos:

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


# Guia Passo a Passo - Configuração de Projeto Python com GitHub no Windows

Este guia mostra como criar um ambiente Python separado, instalar bibliotecas, configurar Git e subir seu projeto no GitHub.

---

## 1. Criar pasta do projeto

No PowerShell ou CMD:

```powershell
cd "A:\Matheus Cardoso\Python"
mkdir DownTube
cd DownTube
```

## 2. Criar ambiente virtual

```powershell
python -m venv venv  # cria ambiente virtual
```

Ativar o ambiente:

* PowerShell:

```powershell
.\venv\Scripts\Activate
```

* CMD:

```cmd
venv\Scripts\activate.bat
```

> Dica: Se der erro de execução no PowerShell, rode `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass` antes de ativar.

## 3. Instalar bibliotecas necessárias

```powershell
pip install pytubefix
```

Salvar dependências:

```powershell
pip freeze > requirements.txt
```

## 4. Instalar e configurar Git

* Baixe: [https://git-scm.com/download/win](https://git-scm.com/download/win)
* Marque **Add Git to PATH** durante a instalação.
* Teste:

```powershell
git --version
```

* Configure usuário:

```powershell
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

## 5. Iniciar repositório Git

```powershell
git init
git add .
git commit -m "primeiro commit - projeto pytubefix"
```

## 6. Criar repositório no GitHub

1. Acesse [https://github.com/new](https://github.com/new)
2. Dê um nome (ex: DownTube)
3. Crie vazio (sem README)

## 7. Conectar repositório local ao GitHub

```powershell
git branch -M main
git remote add origin https://github.com/oMatheusCardoso/DownTube.git
```

## 8. Subir projeto para GitHub

```powershell
git push -u origin main  # envia projeto ao GitHub
```

> Se der erro de non-fast-forward, use:

```powershell
git push origin main --force  # sobrescreve remoto
```

## 9. Próximas alterações

Sempre que alterar código:

```powershell
git add .
git commit -m "mensagem do commit"
git push
```

---

**Dica final:** Crie um arquivo `.gitignore` para não subir arquivos desnecessários como `venv/` ou `__pycache__/`.


