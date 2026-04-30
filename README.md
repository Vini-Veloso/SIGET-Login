# SIGET 

Este repositório contém o sistema de **Controle de Acesso Personalizado** desenvolvido para o dashboard do SIGET feito pela Assessoria de Gestão Estratégica do **DER-MG**.

O projeto atua como um *middleware* de segurança, permitindo que apenas técnicos cadastrados acessem o painel de monitoramento no ArcGIS Experience Builder.

---

## 🎯 Objetivo
O principal objetivo deste sistema é garantir a integridade e a confidencialidade dos dados de transporte, restringindo o acesso aos painéis de monitoramento apenas a profissionais autorizados mediante autenticação por CPF.

---

## 🚀 Funcionalidades Principais

* **Validação de CPF:** Consulta em tempo real via API para verificar se o usuário está autorizado a acessar o sistema.
* **Auto-Cadastro:** Interface dedicada (`Cadastro.html`) para que novos técnicos realizem o registro de seus dados.
* **Log de Acessos:** Registro automático de quem acessou o sistema diretamente em uma planilha do Google Sheets.
* **Integração ArcGIS:** Carregamento dinâmico e seguro do Experience Builder em ambiente de iframe após autenticação.

---

## 🖥️ Módulos do Sistema

### 🔐 Tela de Login (`login.html`)
A porta de entrada do sistema, onde o técnico insere o CPF para validação. É totalmente responsiva para funcionar em dispositivos móveis e desktops.

### 📝 Tela de Cadastro (`Cadastro.html`)
Página exclusiva para o registro de novos técnicos, permitindo a inserção de Nome e CPF na base de dados.

---

## 🛠️ Tecnologias Utilizadas

* **Linguagens Front-end:** HTML5, CSS3 (Design Responsivo) e JavaScript Vanilla.
* **Banco de Dados:** Google Sheets integrado via API [SheetDB](https://sheetdb.io/).
* **Ecossistema GIS:** ArcGIS Experience Builder & Survey123.
* **Hospedagem:** GitHub Pages.

---

## 📋 Como funciona o fluxo?

1. **Acesso:** O usuário acessa a página de login e insere o CPF.
2. **Consulta:** O JavaScript realiza um `GET` na API do **SheetDB** procurando pelo CPF informado na planilha.
3. **Decisão:**
    * **Se autorizado:** O formulário de login é ocultado e o Dashboard do ArcGIS é carregado no `iframe`.
    * **Se não autorizado:** O sistema bloqueia o acesso e sugere o redirecionamento para a tela de cadastro.
4. **Finalização:** Cada acesso autorizado gera um log automático para auditoria.

---

**Desenvolvido por Vinícius Veloso de Oliveira** | Assessoria de Gestão Estratégica - DER-MG.
