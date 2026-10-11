# Xpress

Protótipo de painel de vendas com Flask, páginas HTML/CSS/JavaScript e leitura de CSV.

## Executar localmente

Use Python 3.12. Na raiz do repositório:

```sh
python -m venv .venv
# PowerShell: .venv\Scripts\Activate.ps1
# Linux/macOS: source .venv/bin/activate
python -m pip install -r requirements.txt
python backend/app.py
```

Abra `http://127.0.0.1:5000`. O servidor iniciado dessa forma usa o modo de desenvolvimento.

## Validação

A CI verifica a sintaxe Python e JavaScript e exercita as páginas e a resposta JSON
de vendas usando o cliente de teste do Flask, sem iniciar um servidor público.
Ela não chama integrações externas.

## Limites do protótipo

O formulário de login aceita campos não vazios e não autentica usuários. As rotas
do painel não possuem controle de acesso. O protótipo precisa de autenticação e
autorização antes de receber dados reais ou ser usado em produção.

O banco `database/app.db` e o CSV já fazem parte do histórico; não coloque dados
pessoais, credenciais ou registros reais nesses arquivos. A configuração de ignore
evita adicionar novos bancos locais, mas não remove arquivos já versionados.

Consulte [o fluxo de contribuição](CONTRIBUTING.md) antes de abrir alterações.
