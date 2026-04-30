🛡️ SIGET - Portal de Autenticação e Gestão de Acesso
Este repositório hospeda o middleware de segurança e interface de usuário para o Sistema de Gestão de Transportes (SIGET), desenvolvido para a Assessoria de Gestão Estratégica do DER-MG. O sistema atua como uma camada de proteção entre o público externo e os dados sensíveis hospedados no ArcGIS Experience Builder.

📋 Sobre o Projeto
O portal garante que apenas técnicos devidamente autorizados visualizem os painéis de monitoramento. A solução utiliza uma arquitetura leve baseada em tecnologias web modernas e integração com APIs de planilhas para gerenciamento dinâmico de usuários.

🚀 Módulos do Sistema
🔐 1. Tela de Login (login.html)
A porta de entrada do sistema.

Interface Responsiva: Desenvolvida em HTML5 e CSS3 para operação em desktops e dispositivos móveis.

Fluxo de Autenticação: Ao informar o CPF, o JavaScript realiza uma consulta assíncrona via API para validar as permissões de acesso.

📝 2. Tela de Cadastro (Cadastro.html)
Interface dedicada à integração de novos técnicos.

Auto-Cadastro: Permite que novos usuários registrem suas informações básicas (Nome e CPF) diretamente na base de dados.

Validação em Tempo Real: Verifica campos obrigatórios antes do envio para garantir a integridade dos dados.

🛡️ 3. Verificação de CPF e Segurança
Integração SheetDB: Utiliza o Google Sheets como banco de dados NoSQL por meio da API SheetDB, facilitando a gestão por pessoal administrativo.

Segurança de Iframe: O dashboard do ArcGIS só é injetado no DOM e exibido após o retorno positivo da API de autenticação.

🛠️ Tecnologias Utilizadas
Front-end: HTML5, CSS3 (Design Responsivo) e JavaScript Vanilla.

Banco de Dados: Google Sheets integrado via API SheetDB para gestão de usuários.

Ecossistema GIS: ArcGIS Experience Builder para os dashboards e Survey123 para coleta de dados.

Infraestrutura: Hospedagem e deploy contínuo via GitHub Pages.

Integrações: Middleware desenvolvido em Node.js/PHP para processamento de dados GeoJSON.

🔄 Fluxo de Operação
Acesso: O técnico acessa o Portal de Login.

Consulta: O sistema executa um GET no SheetDB filtrando pelo CPF inserido.

Decisão:

Autorizado: O formulário é substituído dinamicamente pelo dashboard interativo.

Não Autorizado: O sistema bloqueia o acesso e sugere o redirecionamento para a Tela de Cadastro.

Log: Cada acesso bem-sucedido gera um registro automático de auditoria.

🏗️ Estrutura do Repositório
├── login.html          # Portal de Login (Home)
├── Cadastro.html       # Sistema de registro de novos técnicos
├── README.md           # Documentação do projeto
└── assets/             # (Opcional) Pasta para CSS, JS e Imagens
