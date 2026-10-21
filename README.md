Projeto Flask com uv

1. Pré-requisitos
Python: Versão 3.10 ou superior instalada no sistema.

uv: Gerenciador de pacotes e dependências Python de alta performance.

2. Instalação do UV (Windows)
Abra o Terminal do Windows ou o PowerShell e execute o comando abaixo para instalar a ferramenta:

PowerShell
powershell -executionpolicy bypass -c "irm https://astral.sh/uv/install.ps1 | iex"

3. Comandos Úteis de Verificação
Para confirmar se as ferramentas estão instaladas e configuradas corretamente no seu ambiente:

Verificar versão do uv:

Bash
uv --version
Verificar versão do Python:

Bash
python --version

4. Inicialização e Configuração do Ambiente
Siga a sequência abaixo no terminal, dentro da pasta do seu projeto:

Passo 1: Inicializar o Projeto
Cria a estrutura base do projeto e gera o arquivo de configuração pyproject.toml.

Bash
uv init
Passo 2: Criar o Ambiente Virtual
Gera a pasta isolada .venv para guardar as dependências do projeto.

Bash
uv venv
Passo 3: Instalar Dependências e Sincronizar
Instala os pacotes declarados no pyproject.toml e sincroniza o ambiente virtual .venv.

Bash
uv sync

5. Regra de Negócio do Template (templates/ola.html)
A renderização visual da aplicação segue a condicional abaixo:

Com parâmetro de nome: Se o parâmetro nome for informado na URL, o template exibe: Olá, {nome}!.

Sem parâmetro de nome: Se o parâmetro for omitido, o template exibe a mensagem padrão: Olá, Flask!.

6. Execução da Aplicação
Inicie o servidor de desenvolvimento do Flask utilizando o contexto isolado do uv:

Bash
uv run flask run
Após a execução do comando, a aplicação estará ativa e acessível pelo navegador no endereço local padrão: [http://127.0.0.1:5000](http://127.0.0.1:5000).