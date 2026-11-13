# Relatório de Auditoria Técnica: Google Lighthouse & WAVE
**Projeto:** Descobrir Gaia e Porto  
**Ferramentas:** Google Lighthouse (Chrome DevTools) e WAVE Evaluation Tool  
**Páginas Auditadas:** `index.html`, `monumentos.html` e `gastronomia.html`  

---

## 1. Resultados Google Lighthouse (Mobile)

| Página Auditada | Performance | Accessibility | Best Practices | SEO | Observações Técnicas |
| :--- | :---: | :---: | :---: | :---: | :--- |
| `index.html` | 90 | 100 | 96 | 91 | Grelha Bootstrap responsiva validada; contraste e semântica conformes. |
| `monumentos.html` | 88 | 100 | 96 | 91 | Tabela `.table-custom` encapsulada em `.table-responsive` com `caption-top`. |
| `gastronomia.html` | 84 | 100 | 96 | 91 | Estrutura semântica validada; imagens otimizadas com atributos `alt`. |

---

## 2. Auditoria WAVE: Deteção e Correção de Conformidade (WCAG 2.2)

### 2.1. Diagnóstico Inicial ("Antes")
Durante a análise inicial com a extensão **WAVE** nas páginas `monumentos.html` e `gastronomia.html`, registou-se um **AIM Score de 9.1 / 10**, identificando-se:
* **0 Errors** (sem erros estruturais críticos);
* **1 Contrast Error (`2.77:1`)** no link ativo da barra de navegação (`Gastronomia` / `Monumentos`), devido ao texto em Dourado Vinho do Porto (`#975A16`) aplicado diretamente sobre fundo Azul Rio Douro (`#1A365D`), abaixo do limiar mínimo de `4.5:1` exigido pelo Critério de Sucesso 1.4.3 das WCAG 2.2;
* **2 Alerts** (avisos de estrutura): ausência de cabeçalho de primeiro nível (`<h1>` substituído por `<h2>`) e link redundante entre o título da marca (`navbar-brand`) e a opção `Início`.

### 2.2. Correções Aplicadas e Validação Final ("Depois")
1. **Correção de Contraste (`bootstrap.css`):** O estado ativo e `:hover`/`.focus` da classe `.navbar-custom .nav-link` foi atualizado para fundo `#975A16` com texto em Branco Puro (`#FFFFFF`), elevando o rácio de contraste para **`5.14:1`** (conformidade WCAG 2.2 AA).
2. **Hierarquia Semântica (`<h1>`):** O título principal de cada página foi promovido a `<h1 class="h2">`, preservando a escala visual e assegurando a estrutura documental correta para leitores de ecrã.
3. **Eliminação de Link Redundante:** O elemento `navbar-brand` foi convertido para `<span>`, mantendo apenas o item `Início` como hiperligação para a página principal.

### 2.3. Resultados Finais WAVE (3 Páginas)
* **Errors:** `0`
* **Contrast Errors:** `0`
* **Alerts:** `0`
* **AIM Score:** `10 / 10`
