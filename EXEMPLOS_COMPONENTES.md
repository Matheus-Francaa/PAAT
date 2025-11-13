# 🧩 Exemplos de Componentes Gov.br

Este arquivo contém exemplos práticos de como usar os componentes do Design System do Governo Federal no projeto PAAT.

---

## 📋 Índice

1. [Botões](#botões)
2. [Campos de Entrada](#campos-de-entrada)
3. [Cards](#cards)
4. [Breadcrumb](#breadcrumb)
5. [Mensagens](#mensagens)
6. [Tabelas](#tabelas)
7. [Modais](#modais)
8. [Navegação](#navegação)

---

## 🔘 Botões

### Botão Primário
```html
<button class="br-button primary" type="button">
  Texto do Botão
</button>
```

### Botão Secundário
```html
<button class="br-button secondary" type="button">
  Texto do Botão
</button>
```

### Botão Circular (Ícone)
```html
<button class="br-button circle" type="button" aria-label="Descrição">
  <i class="fas fa-search" aria-hidden="true"></i>
</button>
```

### Botão com Ícone e Texto
```html
<button class="br-button primary" type="button">
  <i class="fas fa-download" aria-hidden="true"></i>
  <span>Download</span>
</button>
```

### Botão Desabilitado
```html
<button class="br-button primary" type="button" disabled>
  Botão Desabilitado
</button>
```

---

## 📝 Campos de Entrada

### Input Simples
```html
<div class="br-input">
  <label for="input-text">Nome</label>
  <input id="input-text" type="text" placeholder="Digite seu nome" />
</div>
```

### Input com Ícone
```html
<div class="br-input input-icon">
  <label for="input-email">E-mail</label>
  <input id="input-email" type="email" placeholder="seu@email.com" />
  <i class="fas fa-envelope" aria-hidden="true"></i>
</div>
```

### Input com Botão de Busca
```html
<div class="br-input input-button">
  <label for="search-input">Pesquisar</label>
  <input id="search-input" type="text" placeholder="Digite sua busca..." />
  <button class="br-button circle" type="button" aria-label="Pesquisar">
    <i class="fas fa-search" aria-hidden="true"></i>
  </button>
</div>
```

### Textarea
```html
<div class="br-textarea">
  <label for="textarea-message">Mensagem</label>
  <textarea id="textarea-message" rows="4" placeholder="Digite sua mensagem..."></textarea>
</div>
```

### Select
```html
<div class="br-select">
  <label for="select-state">Estado</label>
  <select id="select-state">
    <option value="">Selecione</option>
    <option value="SP">São Paulo</option>
    <option value="RJ">Rio de Janeiro</option>
    <option value="MG">Minas Gerais</option>
  </select>
</div>
```

---

## 🃏 Cards

### Card Básico
```html
<div class="br-card">
  <div class="card-header">
    <h3>Título do Card</h3>
  </div>
  <div class="card-content">
    <p>Conteúdo do card aqui.</p>
  </div>
  <div class="card-footer">
    <button class="br-button primary" type="button">Ação</button>
  </div>
</div>
```

### Card com Imagem
```html
<div class="br-card">
  <div class="card-image">
    <img src="imagem.jpg" alt="Descrição da imagem" />
  </div>
  <div class="card-content">
    <h3>Título</h3>
    <p>Descrição do card.</p>
    <a href="#" class="br-button secondary">Saiba mais</a>
  </div>
</div>
```

---

## 🍞 Breadcrumb

### Breadcrumb Simples
```html
<nav class="br-breadcrumb" aria-label="Breadcrumb">
  <ol class="breadcrumb-list">
    <li class="breadcrumb-item">
      <a href="/">Início</a>
      <i class="fas fa-chevron-right" aria-hidden="true"></i>
    </li>
    <li class="breadcrumb-item">
      <a href="/repositorios">Repositórios</a>
      <i class="fas fa-chevron-right" aria-hidden="true"></i>
    </li>
    <li class="breadcrumb-item active" aria-current="page">
      Detalhes
    </li>
  </ol>
</nav>
```

**CSS necessário:**
```css
.br-breadcrumb {
  padding: 1rem 0;
}

.breadcrumb-list {
  display: flex;
  align-items: center;
  list-style: none;
  padding: 0;
  margin: 0;
  flex-wrap: wrap;
}

.breadcrumb-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.breadcrumb-item a {
  color: var(--blue-warm-vivid-70);
  text-decoration: none;
}

.breadcrumb-item.active {
  color: var(--gray-60);
}

.breadcrumb-item i {
  font-size: 0.75rem;
  color: var(--gray-60);
}

.breadcrumb-item:last-child i {
  display: none;
}
```

---

## 💬 Mensagens

### Mensagem de Sucesso
```html
<div class="br-message success" role="alert">
  <div class="message-icon">
    <i class="fas fa-check-circle" aria-hidden="true"></i>
  </div>
  <div class="message-content">
    <strong>Sucesso!</strong> Operação realizada com êxito.
  </div>
  <button class="message-close" aria-label="Fechar mensagem">
    <i class="fas fa-times" aria-hidden="true"></i>
  </button>
</div>
```

### Mensagem de Erro
```html
<div class="br-message error" role="alert">
  <div class="message-icon">
    <i class="fas fa-exclamation-circle" aria-hidden="true"></i>
  </div>
  <div class="message-content">
    <strong>Erro!</strong> Não foi possível completar a operação.
  </div>
</div>
```

### Mensagem de Aviso
```html
<div class="br-message warning" role="alert">
  <div class="message-icon">
    <i class="fas fa-exclamation-triangle" aria-hidden="true"></i>
  </div>
  <div class="message-content">
    <strong>Atenção!</strong> Verifique os dados antes de continuar.
  </div>
</div>
```

### Mensagem de Informação
```html
<div class="br-message info" role="alert">
  <div class="message-icon">
    <i class="fas fa-info-circle" aria-hidden="true"></i>
  </div>
  <div class="message-content">
    <strong>Informação:</strong> Esta operação pode levar alguns minutos.
  </div>
</div>
```

**CSS necessário:**
```css
.br-message {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 1rem;
  border-radius: 8px;
  margin: 1rem 0;
}

.br-message.success {
  background-color: #E8F5E9;
  border-left: 4px solid var(--green-cool-vivid-50);
  color: #1B5E20;
}

.br-message.error {
  background-color: #FFEBEE;
  border-left: 4px solid var(--red-vivid-50);
  color: #B71C1C;
}

.br-message.warning {
  background-color: #FFF8E1;
  border-left: 4px solid #FFA000;
  color: #F57F17;
}

.br-message.info {
  background-color: var(--blue-warm-10);
  border-left: 4px solid var(--blue-warm-vivid-70);
  color: var(--blue-warm-vivid-80);
}

.message-icon {
  font-size: 1.5rem;
}

.message-content {
  flex: 1;
}

.message-close {
  background: none;
  border: none;
  font-size: 1.25rem;
  cursor: pointer;
  color: inherit;
  padding: 0.25rem;
}
```

---

## 📊 Tabelas

### Tabela Simples
```html
<div class="br-table">
  <table>
    <thead>
      <tr>
        <th>Nome</th>
        <th>E-mail</th>
        <th>Status</th>
        <th>Ações</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>João Silva</td>
        <td>joao@email.com</td>
        <td><span class="badge success">Ativo</span></td>
        <td>
          <button class="br-button circle small" aria-label="Editar">
            <i class="fas fa-edit"></i>
          </button>
        </td>
      </tr>
      <tr>
        <td>Maria Santos</td>
        <td>maria@email.com</td>
        <td><span class="badge warning">Pendente</span></td>
        <td>
          <button class="br-button circle small" aria-label="Editar">
            <i class="fas fa-edit"></i>
          </button>
        </td>
      </tr>
    </tbody>
  </table>
</div>
```

**CSS necessário:**
```css
.br-table {
  overflow-x: auto;
  margin: 1rem 0;
}

.br-table table {
  width: 100%;
  border-collapse: collapse;
  background: var(--pure-0);
}

.br-table th,
.br-table td {
  padding: 1rem;
  text-align: left;
  border-bottom: 1px solid var(--gray-20);
}

.br-table th {
  background-color: var(--gray-5);
  color: var(--gray-80);
  font-weight: 600;
}

.br-table tr:hover {
  background-color: var(--gray-5);
}

.badge {
  padding: 0.25rem 0.75rem;
  border-radius: 100px;
  font-size: 0.875rem;
  font-weight: 600;
}

.badge.success {
  background-color: #E8F5E9;
  color: var(--green-cool-vivid-50);
}

.badge.warning {
  background-color: #FFF8E1;
  color: #F57F17;
}
```

---

## 🪟 Modais

### Modal Simples
```html
<div class="br-modal" id="modal-example" hidden>
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h2>Título do Modal</h2>
        <button class="modal-close" aria-label="Fechar modal" onclick="closeModal()">
          <i class="fas fa-times"></i>
        </button>
      </div>
      <div class="modal-body">
        <p>Conteúdo do modal aqui.</p>
      </div>
      <div class="modal-footer">
        <button class="br-button secondary" onclick="closeModal()">Cancelar</button>
        <button class="br-button primary">Confirmar</button>
      </div>
    </div>
  </div>
</div>
```

**JavaScript necessário:**
```javascript
function openModal() {
  document.getElementById('modal-example').removeAttribute('hidden');
  document.body.style.overflow = 'hidden';
}

function closeModal() {
  document.getElementById('modal-example').setAttribute('hidden', '');
  document.body.style.overflow = '';
}
```

**CSS necessário:**
```css
.br-modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1000;
}

.modal-dialog {
  background: var(--pure-0);
  border-radius: 8px;
  max-width: 500px;
  width: 90%;
  max-height: 90vh;
  overflow-y: auto;
}

.modal-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.5rem;
  border-bottom: 1px solid var(--gray-20);
}

.modal-body {
  padding: 1.5rem;
}

.modal-footer {
  display: flex;
  justify-content: flex-end;
  gap: 1rem;
  padding: 1.5rem;
  border-top: 1px solid var(--gray-20);
}

.modal-close {
  background: none;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
  color: var(--gray-60);
}
```

---

## 🧭 Navegação

### Menu Horizontal
```html
<nav class="br-menu" aria-label="Menu principal">
  <ul class="menu-list">
    <li class="menu-item active">
      <a href="/">Início</a>
    </li>
    <li class="menu-item">
      <a href="/repositorios">Repositórios</a>
    </li>
    <li class="menu-item">
      <a href="/artefatos">Artefatos</a>
    </li>
    <li class="menu-item">
      <a href="/ajuda">Ajuda</a>
    </li>
  </ul>
</nav>
```

**CSS necessário:**
```css
.br-menu {
  background-color: var(--blue-warm-vivid-70);
  padding: 0 2rem;
}

.menu-list {
  display: flex;
  list-style: none;
  padding: 0;
  margin: 0;
  gap: 2rem;
}

.menu-item a {
  display: block;
  padding: 1rem 0;
  color: var(--pure-0);
  text-decoration: none;
  border-bottom: 3px solid transparent;
  transition: border-color 0.2s;
}

.menu-item.active a,
.menu-item a:hover {
  border-bottom-color: var(--pure-0);
}
```

---

## 💡 Dicas de Uso

### 1. **Sempre use ARIA labels**
```html
<button aria-label="Descrição clara da ação">
  <i class="fas fa-icon" aria-hidden="true"></i>
</button>
```

### 2. **Mantenha hierarquia de headings**
```html
<h1>Título principal (apenas um por página)</h1>
<h2>Seção</h2>
<h3>Subseção</h3>
```

### 3. **Use roles quando apropriado**
```html
<div role="alert">Mensagem importante</div>
<nav role="navigation" aria-label="Menu principal">...</nav>
```

### 4. **Forneça feedback visual e textual**
```html
<button class="br-button primary" disabled>
  <i class="fas fa-spinner fa-spin"></i>
  Carregando...
</button>
```

---

## 📚 Recursos Adicionais

- [Design System Gov.br - Componentes](https://www.gov.br/ds/components)
- [Font Awesome Icons](https://fontawesome.com/icons)
- [WCAG 2.1 Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)

---

**✨ Use estes componentes para manter consistência com o Design System do Governo Federal!**
