# project-core (Core)

Este repositório contém o "core" do projeto Devs2Blu Hackathon: bibliotecas e módulos compartilhados usados por outros serviços e aplicações do monorepo (modelos de domínio, DTOs, validações, utilitários comuns, configuração e infra abstractions).

Índice
- Descrição
- Principais responsabilidades
- Estrutura do repositório
- Requisitos
- Como usar / instalar
- Variáveis de ambiente
- Testes
- Publicação / Build
- Contribuição
- Licença

Descrição
---------
O objetivo deste repositório é centralizar código reutilizável que representa a "camada de core" do ecossistema do hackathon. Ao invés de duplicar lógica entre serviços, colocamos aqui: regras de negócio genéricas, adaptadores, clientes HTTP compartilhados, utilitários de logging e tratamento de erros, e contratos (interfaces/DTOs).

Principais responsabilidades
---------------------------
- Modelos e DTOs compartilhados
- Validações e schemas
- Utilitários (logging, formatação, parse)
- Helpers para testes (factories, mocks)
- Adaptadores para integrações externas (interface, sem implementação acoplada)
- Configurações e helpers de ambiente

Estrutura sugerida
------------------
A estrutura abaixo é apenas uma sugestão. Ajuste conforme a stack adotada (Node, Java, .NET, etc.).

- src/
  - models/          # modelos e DTOs
  - validators/      # schemas e validações
  - utils/           # funções utilitárias
  - adapters/        # interfaces para integrações externas
  - config/          # helpers de configuração/ambiente
  - tests/           # utilitários de testes

- README.md
- package.json (se Node)
- build/ ou target/ (artefatos de build)

Requisitos
----------
Defina aqui os requisitos da stack. Exemplos comuns:
- Node.js >= 16 (se o core for em JS/TS)
- npm ou yarn
- Java 11+ (se aplicável)
- Docker (opcional)

Como usar / instalar
--------------------
Clone o repositório e instale dependências conforme a stack.

Exemplo (Node.js/TypeScript):

1. Clone
   git clone https://github.com/Devs2Blu-Hackathon/project-core.git
   cd project-core

2. Instalar dependências
   npm install
   # ou
   yarn install

3. Build (se aplicável)
   npm run build

Importar em outros projetos
---------------------------
- Se você publica o pacote em um registry (npm, Maven, NuGet), documente o nome do pacote e a versão.
- Se for usado via submódulo/monorepo, explique como consumir os módulos (paths, aliases, workspace).

Variáveis de ambiente
---------------------
Liste as variáveis que o core precisa para funcionar (se houver):

- NODE_ENV - ambiente (development|production)
- LOG_LEVEL - nível de logs (info|warn|error|debug)

Adicione exemplos em .env.example quando necessário.

Testes
------
Descreva como rodar testes e utilitários para facilitar o desenvolvimento.

Exemplo (Node):

npm test
# ou
yarn test

Inclua instruções para rodar testes unitários e de integração; explique como usar factories e mocks do core.

Publicação / Build
------------------
Explique o fluxo de build/publicação (se aplicável): CI/CD responsável por publicar artefatos, versionamento semântico e como criar uma nova tag/versão.

Contribuição
------------
- Siga as convenções de commit do time
- Abra Pull Requests contra a branch main
- Escreva testes para novos utilitários
- Documente mudanças significativas no README ou em CHANGELOG.md

Licença
-------
Defina a licença do repositório (por exemplo, MIT). Se ainda não definida, adicione um arquivo LICENSE.

Contato
-------
Para dúvidas, entre em contato com os mantenedores do repositório ou a equipe do Devs2Blu Hackathon.