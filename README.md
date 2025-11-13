# PAAT - Plataforma de Adaptação de Artefatos Textuais

![Design System Gov.br](https://www.gov.br/++theme++padrao_govbr/img/govbr-logo-large.png)

Plataforma desenvolvida seguindo o **Design System do Governo Federal** (gov.br) para adaptação e gerenciamento de artefatos textuais.

## 🎨 Design System

Este projeto utiliza o [Design System do Governo Federal](https://www.gov.br/ds/), seguindo todas as diretrizes de:
- ✅ Identidade Visual do Governo Federal
- ✅ Acessibilidade (WCAG 2.1)
- ✅ Responsividade
- ✅ Padrões Web em Governo Eletrônico (ePWG)

## 📋 Pré-requisitos

- Node.js (versão 18 ou superior)
- npm (versão 9 ou superior)
- Angular CLI (versão 19.2.7)

## 🚀 Instalação

```bash
# Clone o repositório
git clone <url-do-repositorio>
cd PAAT

# Instale as dependências
npm install
```

## 💻 Desenvolvimento

Para iniciar o servidor de desenvolvimento:

```bash
npm start
# ou
ng serve
```

Acesse `http://localhost:4200/` no navegador. A aplicação recarregará automaticamente ao modificar os arquivos.

## 🏗️ Build

Para compilar o projeto para produção:

```bash
npm run build
# ou
ng build
```

Os arquivos compilados estarão na pasta `dist/`.

## 🧪 Testes

### Testes Unitários

```bash
npm test
# ou
ng test
```

### Testes End-to-End

```bash
ng e2e
```

## 📦 Tecnologias Utilizadas

- **Angular 19.2.0** - Framework JavaScript
- **@govbr-ds/core** - Design System do Governo Federal
- **TypeScript** - Linguagem de programação
- **RxJS** - Programação reativa
- **Font Awesome** - Biblioteca de ícones

## 🎯 Funcionalidades

- 🔍 Busca de repositórios
- 📁 Gerenciamento de repositórios pessoais
- 📄 Procura de artefatos textuais
- 🎨 Interface seguindo padrões gov.br
- ♿ Totalmente acessível (WCAG 2.1)
- 📱 Responsivo para todos os dispositivos

## 📂 Estrutura do Projeto

```
PAAT/
├── src/
│   ├── app/
│   │   ├── app.component.ts          # Componente principal
│   │   ├── app.component.css         # Estilos do componente
│   │   └── app.home.component.html   # Template home
│   ├── assets/                       # Recursos estáticos
│   ├── styles.css                    # Estilos globais
│   └── index.html                    # HTML principal
├── angular.json                      # Configuração Angular
├── package.json                      # Dependências
├── DESIGN_SYSTEM_GOVBR.md           # Documentação do Design System
└── README.md                         # Este arquivo
```

## 🎨 Padrões de Cores

O projeto utiliza a paleta oficial do gov.br:

- **Azul Principal**: `#1351B4`
- **Azul Escuro**: `#0C326F`
- **Cinza Texto**: `#333333`
- **Branco**: `#FFFFFF`

## ♿ Acessibilidade

Este projeto segue as diretrizes WCAG 2.1 nível AA:
- Contraste adequado de cores
- Navegação por teclado
- Labels descritivos
- ARIA labels
- Estrutura semântica HTML5

## 📖 Documentação Adicional

- [Design System Gov.br](https://www.gov.br/ds/)
- [Documentação Angular](https://angular.dev)
- [Guia de Acessibilidade](https://www.gov.br/governodigital/pt-br/acessibilidade-digital)

## 📝 Licença

Este projeto segue as diretrizes do Governo Federal para software público.

## 👥 Contribuindo

Para contribuir com o projeto, por favor siga as diretrizes do Design System do Governo Federal.

---

**Desenvolvido com ❤️ seguindo os padrões do Governo Federal**

