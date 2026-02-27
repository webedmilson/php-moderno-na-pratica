# 🚀 PHP Moderno na Prática

Repositório com exemplos reais de funcionalidades modernas do **PHP 8.1+ e 8.2**, com código comentado para estudo, entrevistas técnicas e portfólio.

---

## 🎯 Objetivo

Este projeto demonstra:
- ✅ Organização de código orientado a regras de negócio
- ✅ Uso de recursos atuais do PHP para escrever código mais seguro
- ✅ Comentários didáticos para facilitar manutenção e onboarding

---

## 📂 Arquivo Principal

- `funcionalidades_php.php`

---

## 🧠 Funcionalidades Implementadas

### 1) `declare(strict_types=1)`
🔒 Força tipagem estrita e reduz bugs silenciosos de conversão.

### 2) `enum StatusPedido`
🏷️ Substitui strings soltas por um conjunto fechado de estados.

### 3) `readonly class Produto` (PHP 8.2)
🧱 Garante imutabilidade do DTO após construção.

### 4) `ProdutoService`
⚙️ Centraliza regras de negócio:
- `aplicarDesconto(float $preco, int|float $percentual): float`
- `calcularTotal(array $produtos): float`

### 5) `match expression`
🧩 Usado em `mensagemStatus()` e `classificarPrioridade()` para condições mais legíveis.

### 6) `null coalescing assignment (??=)`
🛟 Usado em `obterCidadeCliente()` para fallback seguro de valores.

### 7) Validação de versão
📌 `validarVersaoPhpMinima()` evita executar recursos não suportados.

---

## ▶️ Como Executar

### Requisito
- PHP `8.2+`

### Rodar no terminal
```bash
php funcionalidades_php.php
```

### Saída esperada (exemplo)
```text
Versão PHP atual: 8.2.x
Total dos produtos: R$ 849,70
Preço original: R$ 299,90
Preço com desconto (15%): R$ 254,92
Status: Pedido em preparação.
Cidade do cliente: São Paulo
Prioridade score 87: alta
```

---

## 📈 Estratégia Para Manter o GitHub Atualizado

Para fortalecer autoridade técnica:

1. 🗓️ Publique uma melhoria pequena por semana
2. 🧾 Use commits semânticos (`feat:`, `refactor:`, `docs:`, `test:`)
3. 📚 Atualize o README sempre que adicionar recurso
4. 🏷️ Crie tags mensais (`v1.0.0`, `v1.1.0`) com changelog curto
5. 🛠️ Use Issues como roadmap público

---

## 🔭 Próximos Passos

- Adicionar testes unitários com PHPUnit/Pest
- Separar em estrutura `src/` com autoload via Composer
- Incluir exemplos de API com validação de entrada
- Adicionar CI com GitHub Actions

---

## 📜 Licença

Sugestão: **MIT**

---

## 👨‍💻 Autor

**Desenvolvido por Edmilson Rodrigues**
