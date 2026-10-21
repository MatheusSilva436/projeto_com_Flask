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

Verificar versão do uv no terminal:

uv --version
Verificar versão do Python:

python --version

4. Inicialização e Configuração do Ambiente
Siga a sequência abaixo no terminal, dentro da pasta do seu projeto:

Passo 1: Inicializar o Projeto
Cria a estrutura base do projeto e gera o arquivo de configuração pyproject.toml.

terminal:
uv init
Passo 2: Criar o Ambiente Virtual
Gera a pasta isolada .venv para guardar as dependências do projeto.

terminal:
uv venv
Passo 3: Instalar Dependências e Sincronizar
Instala os pacotes declarados no pyproject.toml e sincroniza o ambiente virtual .venv.

terminal:
uv sync (Instala as dependências listadas no pyproject.toml e atualiza a .venv)

5. Template (templates/ola.html)
A renderização visual da aplicação segue a condicional abaixo:

Com parâmetro de nome: Se o parâmetro nome for informado na URL, o template exibe: Olá, {nome}!.

Sem parâmetro de nome: Se o parâmetro for omitido, o template exibe a mensagem padrão: Olá, Flask!.

6. Execução da Aplicação
Inicie o servidor de desenvolvimento do Flask utilizando o contexto isolado do uv.