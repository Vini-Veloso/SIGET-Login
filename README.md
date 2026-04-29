Este repositório contém o sistema de **Controle de Acesso Personalizado** desenvolvido para o dashboard do SIGET da Assessoria de Gestão Estratégica do **DER-MG**.

O projeto atua como um *middleware* de segurança, permitindo que apenas técnicos cadastrados acessem o painel de monitoramento no ArcGIS Experience Builder.

## 🚀 Funcionalidades

* **Validação de CPF:** Consulta em tempo real via API para verificar se o usuário está autorizado.
* **Auto-Cadastro:** Interface amigável para novos técnicos registrarem nome e CPF.
* **Log de Acessos:** Registro automático de quem acessou o sistema diretamente em uma planilha do Google Sheets.
* **Integração ArcGIS:** Carregamento seguro do Experience Builder em ambiente de iframe após autenticação bem-sucedida.

## 🛠️ Tecnologias Utilizadas

* **Front-end:** HTML5, CSS3 (Responsivo) e JavaScript (Vanilla).
* **Banco de Dados:** Google Sheets (via [SheetDB](https://sheetdb.io/)).
* **GIS:** ArcGIS Experience Builder & Survey123.
* **Hospedagem:** GitHub Pages.

## 📋 Como funciona o fluxo?

1.  O usuário acessa a página de login.
2.  O JavaScript realiza um `GET` na API do **SheetDB** procurando pelo CPF informado.
3.  **Se autorizado:** O card de login é ocultado e o Dashboard do ArcGIS é carregado dinamicamente no `iframe`.
4.  **Se não autorizado:** O sistema exibe um alerta e oferece a opção de cadastro.

## ⚙️ Configuração Técnica

Para replicar este projeto, é necessário configurar as seguintes constantes no arquivo `index.html`:

```javascript
const API_URL = "SUA_URL_DO_SHEETDB";
const DASHBOARD_URL = "LINK_PUBLICO_DO_EXPERIENCE_BUILDER";
