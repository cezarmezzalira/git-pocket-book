# Manual de bolso - GIT

## O que é o git?

O Git é um sistema de controle de versão distribuído de código-fonte desenvolvido por Linus Torvalds. Ele permite que você rastreie e controle alterações em arquivos e projetos de software de forma eficiente.

O Git é uma ferramenta poderosa que permite que você faça o versionamento do código-fonte de forma independente e colaborativa. Ele permite que você crie branches separados para trabalhar em diferentes funcionalidades ou correções de bugs, facilitando o desenvolvimento de software em equipe.

O Git é conhecido por sua arquitetura distribuída, o que significa que cada desenvolvedor tem uma cópia local do repositório do projeto, permitindo o trabalho offline e a sincronização de alterações com outros desenvolvedores. Ele também possui um sistema de commit, branching e merging que permite o controle de versão e a colaboração em equipe.

## Porque usar o git para versionamento de código?

O Git é amplamente utilizado para o versionamento de código por várias razões:

- Controle de Versão Eficiente: O Git permite rastrear todas as alterações feitas em um projeto, facilitando a visualização do histórico de desenvolvimento e a identificação de quem fez cada alteração.

- Trabalho Colaborativo: Com o Git, vários desenvolvedores podem trabalhar em um mesmo projeto simultaneamente, cada um em sua própria branch, e depois mesclar suas alterações de forma organizada.

- Branching e Merging Flexíveis: O Git oferece suporte a criação de branches independentes para desenvolver novas funcionalidades ou correções de bugs sem interferir no código principal. Depois, é possível mesclar essas alterações de forma controlada.
- Segurança dos Dados: Como o Git é um sistema distribuído, cada desenvolvedor tem uma cópia local do repositório, o que garante a segurança dos dados em caso de problemas no repositório remoto.

Em resumo, o Git é uma ferramenta essencial para o versionamento de código devido à sua eficiência, capacidade de trabalho colaborativo, flexibilidade de branching e merging, e segurança dos dados.

## Principais conceitos

A seguir, exploraremos os principais conceitos sobre a utilização do git.

### Repositórios

Um repositório Git é um diretório ou pasta onde o Git armazena metadados e objetos de um projeto, permitindo o controle de versão e o rastreamento de alterações.

Ele contém todo o histórico de alterações do projeto, incluindo commits, branches, tags e configurações.

Dentro de um repositório Git, você pode armazenar arquivos de código-fonte, documentos, imagens e outros tipos de arquivos relevantes para o projeto.

O repositório Git mantém o controle das alterações feitas em cada arquivo, permitindo que você reverta para versões anteriores, compare alterações e trabalhe de forma colaborativa com outros desenvolvedores.

Em resumo, um repositório Git é essencial para o desenvolvimento de software, pois fornece um histórico completo de todas as alterações feitas em um projeto e facilita o trabalho em equipe de forma eficiente.

Comando: `git init`

### Commit

Um commit no Git é uma operação que registra as alterações feitas em um repositório. Ele cria uma nova versão do repositório, capturando todas as alterações feitas desde o último commit.

Quando você faz um commit, você está registrando as alterações que fez no código-fonte, adicionando novos arquivos, corrigindo erros, melhorando a documentação ou realizando outras alterações relevantes para o projeto.

O commit inclui uma mensagem descritiva que explica as alterações feitas, ajudando outros desenvolvedores a entenderem o propósito e a importância das alterações.

Cada commit no Git é identificado por um hash único, que é gerado a partir dos metadados do commit, como a mensagem, o autor, a data e as alterações feitas nos arquivos.

Esses hashes permitem rastrear todas as alterações feitas no repositório ao longo do tempo, criando um histórico de commits que pode ser visualizado e analisado.

Comando: `git commit -m "Mensagem"`

### Branch

As branches no Git são ramificações do código-fonte principal em um repositório, permitindo que você trabalhe em paralelo em novas funcionalidades ou correções sem interferir no código principal. Cada branch representa uma linha independente de desenvolvimento com seu próprio conjunto de commits.

Ao criar uma branch, você pode trabalhar em novas funcionalidades (features), correções de bugs ou fazer experimentos sem modificar o código na branch principal (normalmente chamada de "master" ou "main").

Isso possibilita o isolamento do trabalho em progresso e a posterior integração das alterações de volta à branch principal por meio de um processo conhecido como "merge".

Branches são essenciais para o desenvolvimento colaborativo, pois permitem que vários desenvolvedores trabalhem em diferentes partes do código simultaneamente, mantendo a estabilidade do projeto.

Além disso, as branches facilitam a organização do trabalho, o teste de novas funcionalidades e a manutenção de versões estáveis do software.

Comando: `git branch -M <branch>`

### Working folder

O working folder (ou pasta de trabalho) é uma parte do sistema de controle de versão Git onde você trabalha com seus arquivos. É a pasta onde você faz as alterações nos seus arquivos, adiciona novos arquivos, renomeia arquivos, move arquivos, etc.

O working folder é uma cópia local dos arquivos do repositório Git. Quando você faz alterações nos arquivos do working folder, essas alterações não são automaticamente enviadas para o repositório remoto. Em vez disso, você precisa fazer um commit para registrar essas alterações no histórico do repositório.

O working folder é onde você realiza as operações diárias de desenvolvimento, como escrever código, corrigir erros e testar alterações.

É importante entender que as alterações feitas no working folder não são permanentes até que você faça um commit e as envie para o repositório.

Comando: Basta criar, alterar ou excluir algum arquivo do repositório.

### Staging area

A staging area (ou área de preparação) é um conceito central no Git. É uma área temporária onde você prepara os arquivos que deseja incluir em um commit.

Antes de fazer um commit, você pode adicionar arquivos ao staging area usando o comando git add. Quando você adiciona um arquivo ao staging area, ele é marcado para ser incluído no próximo commit.

A staging area é diferente do working folder (pasta de trabalho) onde você faz as alterações nos arquivos. No working folder, você faz as alterações diretamente nos arquivos.

*Importante: ao adicionar um arquivo ao staging area, você está preparando essas alterações para serem incluídas no próximo commit.*

Outro ponto de atenção é entender que o staging area é uma área temporária e as alterações feitas no staging area não são permanentes até que você faça um commit.

Se você não adicionar um arquivo ao staging area antes de fazer um commit, essas alterações não serão incluídas no histórico do repositório.

Comando: `git add <caminho completo arquivo>`

### Remote

Um remote no Git é uma referência a um repositório hospedado em um servidor remoto, como o GitHub. Ele permite que você envie e receba alterações entre o repositório local e o remoto.

Durante a clonagem de um repositório, o remote é configurado para facilitar a sincronização de alterações.

Comandos como `git push` são usados para enviar alterações do repositório local para o remote, enquanto o comando `git pull` é utilizado para buscar e mesclar as alterações do remote no repositório local.

O remote é essencial para colaboração em equipe, permitindo que vários desenvolvedores compartilhem e trabalhem em um projeto centralizado.

Comando: `git remote <opções>`

### Push

Um `push` no Git é uma operação que envia as alterações do seu repositório local para um repositório remoto, como o GitHub ou o GitLab. Ele permite que você compartilhe suas alterações com outros desenvolvedores ou colaboradores.

Quando você faz um push, as alterações do seu repositório local são enviadas para o repositório remoto.

Isso significa que as alterações são mescladas com as alterações existentes no repositório remoto, permitindo que você tenha as últimas atualizações do projeto.

O push é uma operação essencial para sincronizar o seu repositório local com o repositório remoto, especialmente quando você está trabalhando em um projeto com vários desenvolvedores.

Ele ajuda a manter o código atualizado e evita conflitos de mesclagem ao trabalhar em equipe.

Comando: `git push origin <branch>`

### Pull

Um pull é uma operação do Git que busca as alterações do repositório remoto e as mescla com o seu repositório local. Ele permite que você tenha as últimas atualizações do projeto e trabalhe em equipe de forma eficiente.

Quando você faz um pull, o Git busca as alterações do repositório remoto e as mescla com as alterações existentes no seu repositório local.

Isso significa que você recebe as últimas alterações feitas por outros desenvolvedores e pode atualizar seu código para refletir essas alterações.

O pull é outra operação essencial para sincronizar o seu repositório local com o repositório remoto, especialmente quando você está trabalhando em um projeto com vários desenvolvedores. Ele ajuda a manter o código atualizado e evita conflitos de mesclagem ao trabalhar em equipe.

Comando: `git pull <branch>`

### Clone

Um clone no Git é uma operação que cria uma cópia local de um repositório remoto existente.

Ele permite que você obtenha uma cópia completa do repositório, incluindo todos os arquivos e o histórico de commits.

Quando você faz um clone de um repositório remoto, o Git cria uma nova pasta local com todos os arquivos e diretórios do repositório remoto.

Isso permite que você trabalhe com o código localmente e faça alterações sem afetar o repositório remoto original.

O clone é uma operação útil para começar a trabalhar em um projeto existente ou para fazer uma cópia de um repositório para trabalhar localmente.

Comando: `git clone <url>`

### Merge

O merge no Git é uma operação que combina as alterações de um branch com o branch principal (normalmente chamado de "master" ou "main").

Ele une as alterações feitas em um branch específico com o branch principal, permitindo que você integre as alterações de um branch em outro.

Quando você faz um merge, o Git compara as alterações feitas em cada branch e identifica as diferenças.

Em seguida, ele cria um novo commit que combina as alterações dos dois branches, criando uma nova versão do código.

Existem diferentes estratégias de merge, mas o merge mais comum é o merge de fast-forward.

Nesse caso, o Git simplesmente move a referência do branch principal para o último commit do branch que está sendo mesclado.

Isso ocorre quando o branch que está sendo mesclado não possui commits que não estejam presentes no branch principal.

Sequencia de passos para realizar um merge localmente:

1. Ainda na branch de origem, finalizar o desenvolvimento e criar os commits dos arquivos que estão na staging area

2. Após efetuar os commits, navegue até a branch de destino com o comando `git checkout <branch destino>`

3. Certifique-se que a branch de destino está atualizada com o remote, executando o comando `git pull <branch atual>`

4. Agora, execute o comando `git merge <branch origem>`

5. Se não houverem conflitos, o procedimento será feito automaticamente.

Comando: `git merge <branch de origem>`

### Rebase

O rebase no Git é uma operação que permite combinar as alterações de um branch com o branch principal, mas em vez de criar um novo commit de merge, ele reescreve o histórico de commits do branch que está sendo "rebaseado".

Quando você faz um rebase, o Git aplica os commits do branch que está sendo "rebaseado" em cima do branch principal, mantendo uma sequência linear de commits.

Isso permite que você reorganize ou reescreva o histórico de commits do branch, evitando a criação de commits de merge desnecessários.

O rebase é útil quando você deseja manter um histórico de commits limpo e linear, especialmente em branches de longa duração ou quando você deseja integrar as alterações de um branch em outro de forma mais eficiente.

No entanto, é importante ter cuidado ao rebase, pois ele pode reescrever o histórico de commits do branch, o que pode causar conflitos ou problemas de compatibilidade com outras branches que já usam os commits reescritos.

Sequencia de passos para realizar um rebase localmente:

1. Ainda na branch de origem, finalizar o desenvolvimento e criar os commits dos arquivos que estão na staging area

2. Após efetuar os commits, navegue até a branch de destino com o comando `git checkout <branch destino>`

3. Certifique-se que a branch de destino está atualizada com o remote, executando o comando `git pull <branch atual>`

4. Agora, execute o comando `git rebase <branch origem>`

5. Se não houverem conflitos, o procedimento será feito automaticamente.

Comando: `git rebase <branch de origem>`
