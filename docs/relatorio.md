# Relatório de Teste de Navegação por Teclado e Foco Visível — Etapa 4 (E4)

**Projeto:** Descobrir Gaia & Porto  
**Grupo:** Marcelo Sousa, Diogo Cruz, Eurico Cunha, João Teixeira
**Data:** 30 de Outubro de 2026  
**Conformidade:** WCAG 2.2 — Critérios 2.1.1 (Teclado), 2.1.2 (Sem Armadilha de Teclado) e 2.4.7 (Foco Visível)

---

## 1. Objetivo do Teste

Verificar se todas as páginas da plataforma são totalmente operáveis utilizando exclusivamente a tecla <kbd>Tab</kbd>, <kbd>Shift</kbd> + <kbd>Tab</kbd>, <kbd>Enter</kbd> e <kbd>Espaço</kbd>, sem dependência de dispositivo de apontamento (rato) e garantindo que o indicador de foco permanece visível com rácio de contraste adequado.

---

## 2. Checklist de Verificação de Teclado

| Elemento Interativo | Teclas Utilizadas | Comportamento Esperado | Resultado |
| :--- | :--- | :--- | :---: |
| **Links do Menu Global** | <kbd>Tab</kbd> / <kbd>Enter</kbd> | Contorno Azul Douro visível (`outline`); navegação funcional entre páginas | **APROVADO** |
| **Campos do Formulário** | <kbd>Tab</kbd> / Escrita | Foco destacado no campo ativo; transição suave entre `input` e `textarea` | **APROVADO** |
| **Checkbox de Consentimento** | <kbd>Tab</kbd> / <kbd>Espaço</kbd> | Ativa e desativa a seleção sem bloquear o cursor | **APROVADO** |
| **Botão 'Enviar Mensagem'** | <kbd>Tab</kbd> / <kbd>Enter</kbd> | Destaque visual nítido no foco e submissão do formulário | **APROVADO** |
| **Blocos Expansíveis (`<details>`)** | <kbd>Tab</kbd> / <kbd>Enter</kbd> | Expande e recolhe o conteúdo de perguntas frequentes sem travamentos | **APROVADO** |
| **Links do Artigo Académico** | <kbd>Tab</kbd> / <kbd>Enter</kbd> | Salta diretamente para as secções internas via índice de conteúdos | **APROVADO** |

---

## 3. Evidências de Foco Visível

As capturas de ecrã a comprovar o indicador visual de foco nos elementos interativos encontram-se arquivadas na pasta `docs/`:

* `docs/validacao_link.jpeg` — Destaque visual no link de navegação ativo via teclado.
* `docs/validacao_campo_de_texto.jpeg` — Foco visível nos campos de texto.
* `docs/validacao_checkbox.jpeg` — Foco visível na checkbox de consentimento.

---

## 4. Conclusão

A plataforma cumpre 100% dos requisitos de acessibilidade por teclado da E4. Não foram detetadas armadilhas de teclado (*keyboard traps*), e o estilo `:focus` garante visibilidade clara em conformidade com as normas WCAG 2.2.