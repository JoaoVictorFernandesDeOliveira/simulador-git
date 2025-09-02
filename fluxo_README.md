# Fluxo de Trabalho do Projeto Git (Passo a Passo)

Este arquivo serve como um guia para os principais comandos Git, desde a configuração inicial até o envio de novas alterações para o GitHub.

### Configuração Inicial (Feito!)

1.  **Criação das pastas:** Você começou criando uma pasta principal (`Projetos`) no seu computador e, dentro dela, a pasta específica do seu projeto (`simulador-git`).

2.  **`git init`**
    * **O que é:** Inicializa um **repositório Git local** na sua pasta. Ele cria uma pasta oculta chamada `.git` para monitorar todas as suas alterações.

3.  **Criação do repositório no GitHub:**
    * **O que é:** Cria um repositório vazio no seu perfil do GitHub (no navegador), servindo como um backup do seu projeto na nuvem.

4.  **`git remote add origin <URL>`**
    * **O que é:** Conecta o seu repositório local ao repositório remoto no GitHub. O apelido `origin` é usado para se referir ao endereço online.

5.  **Criação do primeiro arquivo:**
    * **O que é:** Você criou o arquivo `simulador_README.md` com o conteúdo planejado, que serve como a "página de entrada" do seu projeto.

6.  **`git add simulador_README.md`**
    * **O que é:** Move o arquivo para uma "área de preparação". Você usa este comando para selecionar quais alterações quer incluir no próximo salvamento.

7.  **`git commit -m "Mensagem"`**
    * **O que é:** Salva as alterações da área de preparação em seu histórico local. A mensagem (`-m`) serve para descrever o que foi feito.

8.  **`git push origin master`**
    * **O que é:** Envia todos os seus commits locais para o repositório remoto no GitHub.

---

### Fluxo de Trabalho em Projetos Colaborativos (Entrando em um projeto)

Quando você se junta a um projeto que já existe, como em uma empresa ou na faculdade, você não precisa criar um repositório do zero. O primeiro passo é clonar o projeto para o seu computador.

1.  **`git clone <URL do Repositório>`**
    * **O que é:** Copia todo o projeto de um repositório online (no GitHub, por exemplo) para uma pasta no seu computador. Este comando já cria a pasta do projeto e configura a conexão com o repositório remoto. Você precisa estar na pasta onde quer que o projeto seja baixado.

Depois de clonar o projeto, o seu fluxo de trabalho diário (descrito abaixo) será o mesmo, mas com um passo extra para manter o projeto organizado.

2.  **Trabalhando com Branches**
    * **O que é:** Uma branch é uma ramificação ou "cópia" do projeto principal.
    * **Como saber em qual branch você está?** Use o comando `git branch`. A branch que tiver um asterisco (`*`) ao lado é a sua branch de trabalho atual.
    * **Como criamos uma nova branch?** Usando o comando `git checkout -b <nome_da_sua_branch>`.
    * **Observação:** O nome da branch geralmente segue a convenção **`tipo/nome-da-tarefa`** para que todos na equipe entendam o objetivo da branch. Por exemplo: `feature/adiciona-login` ou `bugfix/corrige-erro-de-pagamento`.

### Fluxo de Trabalho Diário (Atualizando o Projeto)

Depois de configurar tudo, o fluxo para fazer uma nova alteração e enviá-la para o GitHub é o seguinte:

1.  **Faça suas alterações:** Adicione, edite ou exclua arquivos na sua pasta de trabalho.

2.  **`git add <nome_do_arquivo>` ou `git add .`**
    * **O que é:** Adiciona as novas alterações à área de preparação. Use o nome do arquivo para selecionar um específico, ou use `.` para adicionar todos os arquivos novos ou alterados de uma vez.

3.  **`git commit -m "Mensagem que descreve a alteração"`**
    * **O que é:** Salva as novas alterações em um commit. Lembre-se de que ele só salva o que está na área de preparação.

4.  **`git push origin <nome_da_sua_branch>`**
    * **O que é:** Envia o novo commit (ou os novos commits) do seu computador para o GitHub. É crucial especificar o nome da branch, pois o `git push` envia o que está na sua branch atual para a branch correspondente no GitHub.
    * **Como adicionar esta nova branch ao nosso GitHub?** Ao rodar o comando `git push origin <nome_da_sua_branch>` pela primeira vez, o Git automaticamente cria uma nova branch com esse nome no repositório remoto do GitHub.