🛡️ SIGET - Portal de Autenticação e Gestão de Acesso
Este repositório hospeda o middleware de segurança e a interface de usuário para o Sistema de Gestão de Transportes (SIGET), desenvolvido para a Assessoria de Gestão Estratégica do DER-MG. O sistema atua como uma camada de proteção para os dados sensíveis hospedados no ArcGIS Experience Builder.

📋 Sobre o Projeto
O portal garante que apenas técnicos autorizados visualizem os painéis de monitoramento. A solução utiliza uma arquitetura leve baseada em tecnologias web modernas e integração com APIs de planilhas para gerenciamento dinâmico de usuários.

🚀 Módulos do Sistema
🔐 1. Tela de Login (index.html)
A porta de entrada do sistema.

Interface Responsiva: Desenvolvida em HTML5 e CSS3 para operação em desktops e dispositivos móveis.

Fluxo de Autenticação: O JavaScript realiza uma consulta assíncrona via API para validar o CPF e as permissões de acesso.

📝 2. Tela de Cadastro (Cadastro.html)
Interface dedicada à integração de novos técnicos.

Auto-Cadastro: Permite que novos usuários registrem nome e CPF diretamente na base de dados.

Validação: Verifica campos obrigatórios antes do envio para garantir a integridade dos dados.

🛡️ 3. Verificação de CPF e Segurança
Integração SheetDB: Utiliza o Google Sheets como banco de dados NoSQL por meio da API SheetDB.

Segurança de Iframe: O dashboard do ArcGIS só é exibido após a validação positiva da autenticação.

🛠️ Tecnologias Utilizadas
Front-end: HTML5, CSS3 e JavaScript Vanilla.

Banco de Dados: Google Sheets via API SheetDB.

Ecossistema GIS: ArcGIS Experience Builder e Survey123.

Hospedagem: GitHub Pages.

Integrações: Middleware para processamento de dados GeoJSON.

🔄 Fluxo de Operação
Acesso: O técnico acessa o Portal de Login.

Consulta: O sistema executa um GET no SheetDB filtrando pelo CPF inserido.

Decisão:

Autorizado: O formulário é substituído pelo dashboard interativo.

Não Autorizado: O acesso é bloqueado e o usuário é direcionado para a Tela de Cadastro.

Log: Registro automático de auditoria para cada acesso bem-sucedido.

🏗️ Estrutura do Repositório
├── index.html          # Portal de Login (Home)
├── Cadastro.html       # Sistema de registro de técnicos
├── README.md           # Documentação do projeto
└── assets/             # Pasta para CSS, JS e Imagens
