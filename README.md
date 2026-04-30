🛡️ SIGET - Portal de Autenticação e Gestão de Acesso
Este repositório hospeda o middleware de segurança e a interface de usuário para o Sistema de Gestão de Transportes (SIGET), desenvolvido para a Assessoria de Gestão Estratégica do DER-MG. O projeto atua como uma camada de proteção para garantir que apenas técnicos autorizados acessem os dados sensíveis hospedados no ArcGIS Experience Builder.

🚀 Funcionalidades Principais
Autenticação de Segurança: Validação de CPF via consulta assíncrona para permitir o acesso ao dashboard.

Auto-Cadastro: Interface amigável para que novos técnicos registrem Nome e CPF diretamente na base de dados.

Log de Acessos: Registro automático de auditoria para cada autenticação bem-sucedida.

Integração ArcGIS: Carregamento dinâmico e seguro do Experience Builder em ambiente de iframe após a validação.

Design Responsivo: Interface otimizada para operação em desktops e dispositivos móveis.

🛠️ Tecnologias Utilizadas
Front-end: HTML5, CSS3 e JavaScript Vanilla.

Banco de Dados: Google Sheets integrado via API SheetDB.

Ecossistema GIS: ArcGIS Experience Builder e Survey123.

Hospedagem: Deploy contínuo via GitHub Pages.

Integrações: Processamento de dados e middleware para compatibilidade GeoJSON.

📂 Estrutura do Projeto
/SIGET-Login
├── /assets            # Arquivos de estilo (CSS), scripts (JS) e imagens
├── index.html         # Portal de Login (Página principal de autenticação)
├── Cadastro.html      # Interface de registro de novos técnicos
├── README.md          # Documentação técnica do repositório
└── .gitignore         # Configurações de arquivos ignorados pelo Git
