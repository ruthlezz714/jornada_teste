# Personalizando seu GitHub Pages

Este pacote foi preparado para o repositório `ruthlezz714/skills-github-pages`.

## Estrutura

```text
skills-github-pages/
├── index.html
├── _config.yml
└── assets/
    ├── css/
    │   └── style.css
    └── js/
        └── main.js
```

## 1. Antes de alterar

No GitHub, abra o repositório e crie uma branch para a mudança (por exemplo, ` redesign-portfolio`). Assim você preserva a versão atual enquanto testa.

## 2. Envie os arquivos

Copie `index.html` e a pasta `assets/` para a raiz do repositório, mantendo a estrutura indicada.

**Importante:** depois de confirmar que o novo `index.html` está funcionando, remova ou renomeie o `index.md` antigo. Os dois representam a página inicial e podem gerar conflito de saída no Jekyll.

Mantenha o `_config.yml` existente nesta primeira etapa. O HTML usa `layout: null`, portanto não precisa do layout visual do tema Minima.

## 3. Personalize o conteúdo

Abra `assets/js/main.js`.

- `learningAreas`: áreas e trilhas de estudo.
- `certificates`: certificados recebidos.
- `projects`: projetos, laboratórios e registros práticos.

Para adicionar um certificado, copie este modelo para dentro do array `certificates`:

```js
{
  title: "Nome do certificado",
  institution: "Instituição emissora",
  date: "Novembro de 2026",
  category: "Application Security",
  url: "https://link-publico-do-certificado"
}
```

Para adicionar um projeto, copie este modelo para dentro do array `projects`:

```js
{
  title: "Nome do projeto",
  description: "Resumo do que você desenvolveu ou aprendeu.",
  category: "Laboratório",
  status: "Concluído",
  url: "https://github.com/usuario/repositorio"
}
```

Use vírgula entre os objetos do array. Não coloque uma vírgula depois do último objeto.

## 4. Personalize as cores

Abra `assets/css/style.css` e edite as variáveis no início do arquivo, dentro de `:root`.

- `--bg`: fundo geral.
- `--surface`: fundo dos cartões.
- `--text`: texto principal.
- `--muted`: texto secundário.
- `--accent`: cor de destaque.
- `--dark`: fundo da seção final.

## 5. Publique

Faça commit das alterações na branch de teste e abra a prévia pelo GitHub Pages depois que o workflow de publicação terminar. Se tudo estiver correto, faça merge para a branch principal.

O GitHub Pages pode levar alguns minutos para atualizar. Atualize o navegador sem cache se continuar vendo a versão anterior.

## 6. O que estudar neste projeto

1. HTML semântico: `header`, `nav`, `main`, `section`, `article` e `footer`.
2. CSS: variáveis, Grid, Flexbox, media queries e estados `:hover`.
3. JavaScript: arrays, objetos, `map`, `filter`, template literals e eventos.
4. Git: branch, commit, push e pull request.

## Observação

O site é público. Não publique documentos com dados pessoais, números de identificação, códigos de validação privados ou informações que você não queira expor. Prefira links públicos de verificação dos certificados.
