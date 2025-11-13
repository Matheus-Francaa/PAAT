# Design System do Governo Federal - Implementação PAAT

## 📋 Visão Geral

Este documento descreve a implementação do Design System do Governo Federal (gov.br) no projeto PAAT.

## 🎨 Mudanças Implementadas

### 1. **Biblioteca Instalada**
- `@govbr-ds/core` - Pacote oficial do Design System do Governo Federal

### 2. **Fontes Tipográficas**
- **Rawline**: Fonte principal para textos e títulos
- **Raleway**: Fonte complementar
- Carregadas via CDN do gov.br no `index.html`

### 3. **Cores do Sistema**

As cores seguem a paleta oficial do gov.br:

```css
--blue-warm-vivid-70: #1351B4  /* Azul principal */
--blue-warm-vivid-80: #0C326F  /* Azul escuro */
--blue-warm-20: #C5D4EB        /* Azul claro */
--blue-warm-10: #E6ECF5        /* Azul muito claro */
--gray-80: #333333             /* Texto principal */
--gray-60: #636363             /* Texto secundário */
--gray-20: #CCCCCC             /* Bordas */
--gray-5: #F8F8F8              /* Fundo */
--pure-0: #FFFFFF              /* Branco */
--green-cool-vivid-50: #168821 /* Verde (sucesso) */
--yellow-vivid-20: #FEE685     /* Amarelo (atenção) */
--red-vivid-50: #E52207        /* Vermelho (erro) */
```

### 4. **Componentes Atualizados**

#### **Header (Cabeçalho)**
- Logo do Governo Federal
- Nome do sistema "PAAT"
- Menu de acesso rápido (Perfil, Configurações)
- Botão de login/entrar
- Responsivo e acessível

#### **Conteúdo Principal**
- Título estilizado com tipografia Rawline
- Subtítulo descritivo
- Campo de busca com ícone
- Botões primário e secundário seguindo padrões gov.br

#### **Footer (Rodapé)**
- Informações do sistema
- Links para redes sociais
- Logo do Governo Federal

### 5. **Componentes de Interface**

#### **Botões**
- `.br-button.primary` - Botão de ação principal (azul)
- `.br-button.secondary` - Botão de ação secundária (outline azul)
- `.br-button.circle` - Botão circular para ícones

#### **Campos de Entrada**
- `.br-input` - Campo de texto padrão
- `.br-input-lg` - Campo de texto grande
- `.input-button` - Campo com botão integrado

### 6. **Acessibilidade**

✅ Implementado conforme diretrizes WCAG 2.1:
- Labels descritivos em todos os campos
- ARIA labels em botões de ícone
- Navegação por teclado
- Contraste de cores adequado
- Indicadores de foco visíveis

### 7. **Responsividade**

Breakpoints seguindo padrões Bootstrap/gov.br:
- **Mobile**: < 576px
- **Tablet**: 576px - 768px
- **Desktop**: > 768px

## 🚀 Como Usar

### Executar o Projeto

```bash
npm install
npm start
```

### Estrutura de Arquivos Modificados

```
src/
├── index.html                      # Adicionadas fontes e Font Awesome
├── styles.css                      # Estilos globais com variáveis gov.br
└── app/
    ├── app.component.css           # Estilos específicos do componente
    └── app.home.component.html     # Template atualizado com componentes gov.br
```

## 📚 Referências

- [Design System do Governo Federal](https://www.gov.br/ds/)
- [Documentação @govbr-ds/core](https://www.gov.br/ds/components)
- [Padrões Web em Governo Eletrônico (ePWG)](https://www.gov.br/governodigital/pt-br/governanca-de-dados/padroes-web-em-governo-eletronico)

## 🎯 Próximos Passos

1. **Adicionar mais componentes** do Design System conforme necessário:
   - Cards
   - Tabelas
   - Breadcrumbs
   - Modais
   - Notificações

2. **Implementar tema escuro** (se aplicável)

3. **Criar página de acessibilidade** com controles de fonte e contraste

4. **Adicionar testes de acessibilidade** automatizados

## ⚠️ Notas Importantes

- O Design System do gov.br é obrigatório para sistemas do Governo Federal
- Mantenha sempre a biblioteca `@govbr-ds/core` atualizada
- Siga as diretrizes de acessibilidade e identidade visual
- Teste em diferentes navegadores e dispositivos

## 📞 Suporte

Para dúvidas sobre o Design System:
- Acesse: https://www.gov.br/ds/
- Email: design-system@economia.gov.br
