# Exemplo simples de GitHub Workflow (GitHub Actions)

Projeto mínimo: uma calculadora em Python com testes automatizados.
Toda vez que houver `push` ou `pull request` na branch `main`, o GitHub
executa o workflow `.github/workflows/ci.yml`, que instala o Python,
as dependências e roda os testes.

## Como usar
1. Crie um repositório no GitHub e envie estes arquivos:
   ```
   git init
   git add .
   git commit -m "primeiro commit"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/SEU_REPO.git
   git push -u origin main
   ```
2. Abra a aba **Actions** do repositório e veja o workflow rodando.
3. Para ver uma falha: quebre um teste (ex.: mude `somar` para `a - b`), faça push e observe o ❌.

## Estrutura
```
.
├── .github/workflows/ci.yml   # definição do workflow
├── calculadora.py             # código
├── tests/test_calculadora.py  # testes
└── requirements.txt
```
