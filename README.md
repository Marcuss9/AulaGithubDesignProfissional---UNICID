# Aula de GitHub — UNICID

Projeto demonstrativo de uma página HTML para aprender a versionar, validar e publicar um site utilizando **GitHub**, **GitHub Actions** e **GitHub Pages**.

## Tecnologias

- HTML5: estrutura e conteúdo da página.
- CSS3: estilos incorporados ao `index.html`.
- Git e GitHub: versionamento e colaboração.
- GitHub Actions: automação da validação e publicação.
- GitHub Pages: hospedagem do site estático.

## Estrutura do projeto

```text
.
├── .github/
│   └── workflows/
│       └── build.yml
├── index.html
└── README.md
```

## Como executar localmente

1. Clone o repositório:

   ```bash
   git clone https://github.com/Marcuss9/AulaGithubDesignProfissional---UNICID.git
   ```

2. Entre na pasta do projeto:

   ```bash
   cd AulaGithubDesignProfissional---UNICID
   ```

3. Abra o arquivo `index.html` no navegador.

Não é necessário instalar dependências ou executar um servidor para visualizar a página.

## Como funciona o GitHub Actions

O workflow `.github/workflows/build.yml` é acionado automaticamente a cada **push na branch `main`** ou manualmente por **Actions → Build e publicação do site → Run workflow**.

O processo tem dois jobs:

1. **build:** baixa o código, confirma que existe o arquivo `index.html`, copia a página para `dist/` e envia o artefato para publicação.
2. **deploy:** utiliza o artefato gerado e solicita a publicação no GitHub Pages.

> Como é um site estático, o *build* não envolve compilação: apenas validação e preparação do arquivo HTML.

## Como publicar com GitHub Pages

1. Acesse **Settings → Pages** no repositório.
2. Em **Build and deployment → Source**, selecione **GitHub Actions**.
3. Faça um push na `main` (ou execute o workflow manualmente).
4. Confira a execução em **Actions** e, após o deploy bem-sucedido, acesse o endereço disponibilizado pelo GitHub Pages.

Endereço esperado, caso a publicação esteja habilitada:

https://marcuss9.github.io/AulaGithubDesignProfissional---UNICID/

**Atenção:** este repositório está privado no momento da configuração. A disponibilidade do GitHub Pages para repositórios privados depende do plano e das configurações da conta. Para uma demonstração pública, é possível avaliar tornar o repositório público.

## Fluxo de aprendizagem sugerido

1. Edite o título da página em `index.html`.
2. Confira as alterações com `git status` e `git diff`.
3. Faça um commit e envie as alterações ao GitHub.
4. Observe o workflow na aba **Actions**.
5. Confira o resultado no GitHub Pages após a publicação.

---

**UNICID — Aula prática de publicação com GitHub.**
