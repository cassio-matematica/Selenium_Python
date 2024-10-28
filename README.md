# 🐍 Selenium com Python

Bem-vindo ao repositório **Selenium com Python**! Este repositório contém automações diversas para navegadores web usando o Selenium em Python. Desde tarefas simples, como preencher formulários automaticamente, até fluxos de trabalho complexos, o projeto oferece exemplos e práticas para facilitar a automação web.

## 📑 Visão Geral

O **Selenium** é uma poderosa ferramenta para automação de navegadores. Usando o Selenium com Python, você pode:
- Realizar testes automáticos em sites.
- Extrair dados de sites dinâmicos.
- Automação de tarefas repetitivas, como preenchimento de formulários e downloads.
- Simular interações reais de usuários em páginas web.

## 🚀 Funcionalidades

- **Acesso e navegação** em sites.
- **Preenchimento de formulários** e envio de dados.
- **Extração de informações** e web scraping.
- **Interação com elementos dinâmicos**, como pop-ups, alertas e mais.
- **Tarefas customizadas**, como login automático e execução de ações condicionais.

## 🛠️ Tecnologias Utilizadas

- **Python** – Linguagem principal.
- **Selenium WebDriver** – Para controle e automação de navegadores.
- **ChromeDriver / GeckoDriver** – Para compatibilidade com Chrome e Firefox.

## 📦 Instalação

1. **Clone este repositório:**
   ```bash
   git clone https://github.com/seu_usuario/selenium-python-automation.git
   cd selenium-python-automation
   ```

2. **Instale as dependências:**

```
pip install -r requirements.txt
```
Baixe o WebDriver adequado:

- **ChromeDriver**: baixe a versão compatível com o seu navegador [aqui](https://sites.google.com/a/chromium.org/chromedriver/downloads).
- **GeckoDriver para Firefox**: baixe a versão compatível [aqui](https://github.com/mozilla/geckodriver/releases).

> **Nota**: Lembre-se de adicionar o WebDriver ao PATH do sistema.

⚙️ Configuração

Edite o arquivo config.py (ou o equivalente no repositório) com as configurações desejadas, como URL, credenciais de login, etc.

Exemplo de configuração:
```
# config.py
BASE_URL = "https://exemplo.com"
USERNAME = "seu_usuario"
PASSWORD = "sua_senha"
```
🖱️ Exemplos de Uso

Aqui estão alguns exemplos de automações disponíveis:
1. Acessar uma página e fazer login
```
#Subtitua a url por uma página que você costuma acessar e fazer o login

from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()
driver.get("https://exemplo.com/login")

driver.find_element(By.ID, "username").send_keys("seu_usuario")
driver.find_element(By.ID, "password").send_keys("sua_senha")
driver.find_element(By.ID, "login").click()
```
2. Extração de dados de uma tabela:
```
from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome()
driver.get("https://exemplo.com/tabela")

tabela = driver.find_element(By.ID, "minhaTabela")
linhas = tabela.find_elements(By.TAG_NAME, "tr")

for linha in linhas:
    colunas = linha.find_elements(By.TAG_NAME, "td")
    for coluna in colunas:
        print(coluna.text)
```

🧪 **Testes**

Para garantir a qualidade do código e a funcionalidade do projeto, os testes são uma etapa fundamental. Certifique-se de que as configurações estejam corretas para o ambiente de testes, incluindo variáveis de ambiente e dependências.

### Executando os testes

1. **Instale as dependências de testes**:
   
   Caso utilize o `pytest` como framework de testes, instale-o com o seguinte comando:
   ```bash
   pip install pytest
   ```
Configure o ambiente de testes:

Verifique se todas as variáveis de ambiente necessárias para o ambiente de testes estão corretamente configuradas. Isso pode incluir a configuração de um banco de dados de teste ou chaves de API.

Execute os testes:

Para rodar todos os testes do projeto, utilize o comando abaixo
```
pytest
```

Testes com cobertura de código:

Para analisar a cobertura de código, utilize o pytest-cov. Primeiro, instale-o:

```
pip install pytest-cov
```
Depois, execute:

```
pytest --cov=nome_do_pacote
```

Análise dos resultados

Após a execução dos testes, revise os relatórios gerados para identificar possíveis falhas e áreas com baixa cobertura de código. Corrija os erros e reexecute os testes para garantir que o projeto esteja funcionando conforme o esperado.

📄 **Documentação**

Para mais informações sobre o Selenium e suas funcionalidades, consulte a [documentação oficial do Selenium](https://www.selenium.dev/documentation/).

📞 Contato

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/cassio-matematica/)

[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:cassio.matematica@gmail.com)

🌟 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir um issue ou pull request para melhorias, correções ou novas funcionalidades.

Aproveite e boas automações!
