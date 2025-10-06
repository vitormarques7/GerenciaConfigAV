# RELATÓRIO DE PROJETO – Estratégias de Branching em Git

## Identificação
- **Integrantes da equipe**:
- João Vitor dos Santos Marques
- Alana
- Letícia

- **Repositório GitHub**: https://github.com/vitormarques7/GerenciaConfigAV.git
## 1. Estrutura Inicial
- Branch principal (`main`) criada e configurada?
- Branch `develop` criada a partir de `main`?
- Descreva como foi feita a configuração inicial (comandos usados e prints).
    - A configuração inicial foi realizada por todos os integrantes da equipe em suas máquinas locais. 
      Após clonar o repositório (git clone), cada membro configurou sua identidade no Git utilizando os 
      comandos git config --global user.name "Seu Nome" e git config --global user.email "seu.email@exemplo.com".
      A verificação foi feita com o comando git config --global --list para garantir que as credenciais estavam corretas.
  
    - ### Comando utilizado: git config --global --list

      [imagem git config.png](images/imagem%20git%20config.png)
    - ### Comando utilizado: git remote -v

      [imagem git remote.png](images/imagem%20git%20remote.png)

    - ### Comando utilizado: git branch -a

      [imagem git branch.png](images/imagem%20git%20branch.png)
  
## 2. Fase 1 – Git Flow
### 2.1 Features
- Quais features foram criadas?
  - feature/leticia-add-footer
  - feature/leticia-update-readme
- Liste as branches de features e descreva as alterações.
  - ### Leticia
    - feature/leticia-add-footer: Esta branch foi criada para adicionar um rodapé (footer) ao arquivo index.html. 
      O trabalho foi feito em dois commits: o primeiro adicionou o rodapé e o segundo ajustou o texto de copyright. 
      Posteriormente, esses commits foram unificados com rebase.

    - feature/leticia-update-readme: O objetivo desta branch foi atualizar o arquivo README.md, preenchendo a seção 
        de integrantes da equipe com os nomes de todos os membros. 
  
- Prints dos commits:

  [imagem commits1.png](images/imagem%20commits1.png)

### 2.2 Conflitos
- Onde ocorreram conflitos (arquivos/linhas)?
- Como os conflitos foram resolvidos?
- Inclua prints mostrando os marcadores (`<<<<<<<`, `=======`, `>>>>>>>`) e o
  arquivo final após resolução.

### 2.3 Release
- Criada branch `release/2.0`?
- Alterações preparatórias (ex.: versão, documentação).
- Integração com `main` e geração da tag `v2.0`.

### 2.4 Hotfix
- Qual foi o problema corrigido?
- Como foi feito o merge do hotfix em `main` e `develop`?
- Inclua prints e comandos usados.

### 2.5 Uso de Rebase
- Em qual feature aplicaram `git rebase`?
- Explique o que mudou no histórico.

## 3. Fase 2 – Trunk-Based Development
### 3.1 Branches Curtos
- Quais branches foram criados a partir de `main`?
- Quantos commits cada um teve?

### 3.2 Squash
- Qual merge foi feito usando **squash**?
- Explique por que foi escolhido squash em vez de merge normal.

### 3.3 Tag Final
- Tag criada: `v3.0`.
- - Prints do histórico.

## 4. Histórico de Commits
Inclua saída do comando [com "git log --oneline --graph --all"]:
* 0d9e9f4 (HEAD -> main, origin/main, origin/HEAD) docs: Adiciona estrutura ao RELATORIO.md
* 3920877 docs: Adiciona imagens para o relatório
* c3fbd71 (tag: v3.0) feat: Implementa página de contato com estilos
*   094db36 Merge branch 'leticia-task-3'
    |\  
    | * 23dfbea (origin/leticia-task-3, leticia-task-3) feat: Adiciona página de serviços
* |   50f36a9 Merge branch 'vitor-task-1'
  |\ \  
  | * | 3c5e886 (origin/vitor-task-1, vitor-task-1) feat: Adiciona página sobre
  |/ /  
  | | * 42b78c6 (origin/alana-task-2, alana-task-2) refactor: Move contact.html para o diretório src
  | | * e3d8010 style: Ajusta espaçamento na página de contato
  | | * 794e458 feat: Adiciona página de contato
  | |/  
  |/|
* |   4836cb3 (tag: v2.0.1) Merge remote-tracking branch 'origin/hotfix/2.0.1'
  |\ \  
  | | | *   e7d5bf9 (origin/develop) Merge remote-tracking branch 'origin/hotfix/2.0.1' into develop
  | | | |\  
  | | |_|/  
  | |/| |   
  | * | | a86ff81 (origin/hotfix/2.0.1) fix(docs): Ajusta relatório ao modelo da atividade e adiciona integrantes
  |/ / /
* | |   7e0b185 (tag: v2.0) feat: Finaliza release 2.0 e integra na main
  |\ \ \  
  | |/ /  
  |/| |
* | | 4164c53 fix: Atualiza nome da equipe no footer
* | | a646ebb feat: Adiciona footer na página
  | | *   3a0be6c Merge branch 'release/2.0' into develop
  | | |\  
  | | |/  
  | |/|   
  | * | ec9edaf (origin/release/2.0) chore: Atualiza a versão para 2.0
* 0d9e9f4 (HEAD -> main, origin/main, origin/HEAD) docs: Adiciona estrutura ao RELATORIO.md
* 3920877 docs: Adiciona imagens para o relatório
* c3fbd71 (tag: v3.0) feat: Implementa página de contato com estilos
*   094db36 Merge branch 'leticia-task-3'
    |\
    | * 23dfbea (origin/leticia-task-3, leticia-task-3) feat: Adiciona página de serviços
* |   50f36a9 Merge branch 'vitor-task-1'
  |\ \
  | * | 3c5e886 (origin/vitor-task-1, vitor-task-1) feat: Adiciona página sobre
  |/ /
  | | * 42b78c6 (origin/alana-task-2, alana-task-2) refactor: Move contact.html para o diretório src
  | | * e3d8010 style: Ajusta espaçamento na página de contato
  | | * 794e458 feat: Adiciona página de contato
  | |/
  |/|
* |   4836cb3 (tag: v2.0.1) Merge remote-tracking branch 'origin/hotfix/2.0.1'
  |\ \
  | | | *   e7d5bf9 (origin/develop) Merge remote-tracking branch 'origin/hotfix/2.0.1' into develop
  | | | |\
  | | |_|/
  | |/| |
  | * | | a86ff81 (origin/hotfix/2.0.1) fix(docs): Ajusta relatório ao modelo da atividade e adiciona integrantes
  |/ / /
* | |   7e0b185 (tag: v2.0) feat: Finaliza release 2.0 e integra na main
  |\ \ \
  | |/ /
  |/| |
* | | 4164c53 fix: Atualiza nome da equipe no footer
* | | a646ebb feat: Adiciona footer na página
  | | *   3a0be6c Merge branch 'release/2.0' into develop
  | | |\
  | | |/
  | |/|
  | * | ec9edaf (origin/release/2.0) chore: Atualiza a versão para 2.0
  | |/
  | *   350c604 feat: Integra feature de footer e resolve conflitos
  | |\
  | | * 668e173 (origin/feature/leticia-add-footer, feature/leticia-add-footer) feat: Adiciona e ajusta footer da página
  | * |   e7d90d0 (develop) fix: Resolve conflito ao integrar header da branch feature/vitor-add-header
  | |\ \
  | | * | 0c89883 (origin/feature/vitor-add-header) feat: Adiciona header na página inicial
  | * | |   42e9b8a Merge remote-tracking branch 'origin/feature/leticia-update-readme' into develop
  | |\ \ \
  | * \ \ \   9524573 Merge branch 'feature/alana-add-css' into develop
  | |\ \ \ \
  | | * | | | c0135bb (origin/feature/alana-add-css) feat: Adiciona arquivo de estilo CSS básico
  | |/ / / /  
  |/| | | |   
  | * | | |   bf1a8a5 fix: Resolve conflito de merge no titulo do index.html
  | |\ \ \ \  
  | | * | | | 2453376 (origin/feature/alana-add-title) feat: Adiciona H1 principal na página
  | |/ / / /  
  |/| | | |   
  | * | | | e7bd767 Merge branch 'feature/vitor-add-html' into develop
  |/| | | |
  | | |/ /
  | |/| |
  | * | | 2234fde (origin/feature/vitor-add-html) feat: Adiciona estrutura base do index.html
  |/ / /
  | | | * 5bdfd4a (origin/feature/leticia-update-readme, feature/leticia-update-readme) docs: Preenche nomes da equipe no RELATORIO
  | | |/
  | | | * 6362222 (backup/feature/leticia-add-footer) fix: Atualiza nome da equipe no footer
  | | | * ee91f46 feat: Adiciona footer na página
  | | |/
  | | * 810914b fix: Atualiza nome da equipe no footer
  | | * 7ea6da0 feat: Adiciona footer na página
  | |/
  | * 8e4ac0a docs: Preeche nomes da equipe em RELATORIO
  |/
* 28f90da chore: adicionar .gitignore na raiz
* 0c33e20 configurações iniciais
* 62bfb2a feat: adicionar RELATORIO inicial
