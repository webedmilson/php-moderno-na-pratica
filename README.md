# PHP Moderno: Funcoes, Boas Praticas e Atualizacoes

Repositorio com exemplos reais de funcionalidades modernas do PHP 8.1+ e 8.2, com codigo comentado para estudo, entrevista tecnica e portifolio.

## Objetivo

Este projeto demonstra:
- Organizacao de codigo orientado a regras de negocio
- Uso de recursos atuais do PHP para escrever codigo mais seguro
- Comentarios didaticos para facilitar manutencao e onboarding

## Arquivo principal

- `funcionalidades_php.php`

## Funcionalidades implementadas

1. `declare(strict_types=1)`
- Forca tipagem estrita e reduz bugs silenciosos de conversao.

2. `enum StatusPedido`
- Substitui strings soltas por um conjunto fechado de estados.

3. `readonly class Produto` (PHP 8.2)
- Garante imutabilidade do DTO apos construcao.

4. `ProdutoService`
- Centraliza regras de negocio:
  - `aplicarDesconto(float $preco, int|float $percentual): float`
  - `calcularTotal(array $produtos): float`

5. `match expression`
- Usado em `mensagemStatus()` e `classificarPrioridade()` para condicoes mais legiveis.

6. `null coalescing assignment (??=)`
- Usado em `obterCidadeCliente()` para fallback seguro de valores.

7. Validacao de versao
- `validarVersaoPhpMinima()` evita executar recursos nao suportados.

## Como executar

### Requisito
- PHP `8.2+`

### Rodar no terminal
```bash
php funcionalidades_php.php
```

### Saida esperada (exemplo)
```text
Versao PHP atual: 8.2.x
Total dos produtos: R$ 849,70
Preco original: R$ 299,90
Preco com desconto (15%): R$ 254,92
Status: Pedido em preparacao.
Cidade do cliente: Sao Paulo
Prioridade score 87: alta
```

## Estrategia para manter o GitHub atualizado

Para mostrar consistencia tecnica e autoridade:

1. Publique uma melhoria pequena por semana.
2. Use commits com padrao semantico (`feat:`, `refactor:`, `docs:`, `test:`).
3. Sempre atualize o README quando adicionar recurso novo.
4. Crie uma tag mensal (`v1.0.0`, `v1.1.0`) com changelog curto.
5. Abra `Issues` com roadmap e feche conforme evolucao.

## Sugestoes de proximos passos

- Adicionar testes unitarios com PHPUnit/Pest
- Separar em estrutura `src/` com autoload via Composer
- Incluir exemplos de API com validacao de entrada
- Adicionar CI no GitHub Actions

## Licenca

Sugestao: MIT
