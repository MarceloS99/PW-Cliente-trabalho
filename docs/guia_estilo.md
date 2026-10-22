# Guia de Estilo e Acessibilidade Visual — Descobrir Gaia & Porto

**Unidade Curricular:** Programação Web - Cliente (15791)  
**Instituição:** ISLA Gaia — 1.º Ciclo em Engenharia Informática  
**Docente:** José Augusto de Araújo Monteiro  
**Grupo:** Marcelo Sousa, Diogo Cruz, Eurico Cunha, João Teixeira 
**Fase:** Etapa 3 (E3) — CSS base e validação  

---

## 1. Introdução e Filosofia Visual

O guia de estilo do projeto **"Descobrir Gaia & Porto"** reflete a ligação histórica, fluvial e cultural entre Vila Nova de Gaia e o Porto. A identidade visual assenta numa paleta cromática equilibrada, tipografia de elevada legibilidade e conformidade rigorosa com as diretrizes de acessibilidade **WCAG 2.2 (Nível AA)**.

A estrutura visual adota um modelo limpo:
* Cabeçalho e navegação integrados num tom azul profundo alusivo ao Rio Douro.
* Fundo de leitura em tom claro e suave para prevenir a fadiga visual.
* Destaques em tom dourado remetendo às caves de Vinho do Porto.
* Cantos arredondados discretos e modernos aplicados a figuras e botões.

---

## 2. Paleta de Cores do Projeto (Mínimo de 5 Cores)

| Nome da Cor | Hexadecimal | RGB | Aplicação no Projeto |
| :--- | :---: | :---: | :--- |
| **Azul Rio Douro** | `#1A365D` | `rgb(26, 54, 93)` | Fundo do cabeçalho (`header`), navegação principal e títulos principais (`h1`, `h2`). |
| **Dourado Vinho do Porto** | `#975A16` | `rgb(151, 90, 22)` | Realces, detalhes, indicadores ativos de página e contornos decorativos. |
| **Fundo Neutro Suave** | `#F7FAFC` | `rgb(247, 250, 252)` | Fundo geral da página (`body`), proporcionando leitura confortável. |
| **Texto Grafite Escuro** | `#1A202C` | `rgb(26, 32, 44)` | Cor principal para parágrafos, listas e texto corrido. |
| **Cinzento Granito** | `#4A5568` | `rgb(74, 85, 104)` | Fundo do rodapé (`footer`), bordas estruturais e legendas secundárias. |
| **Branco Puro** (Apoio) | `#FFFFFF` | `rgb(255, 255, 255)` | Texto sobre áreas escuras e fundos de cartões/formulários. |

---

## 3. Tipografia e Escala Hierárquica

A tipografia utiliza um sistema *system font stack* robusto, dispensando dependências de rede externas e assegurando tempos de carregamento instantâneos e máxima legibilidade em todos os sistemas operativos.

### 3.1 Fontes
* **Fonte Principal (Interface e Texto):** `system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif`
* **Fonte Monospaçada (Dados técnicos/código):** `ui-monospace, "Cascadia Code", "Source Code Pro", Menlo, Consolas, monospace`

### 3.2 Escala Tipográfica
* **`h1` (Título Principal da Página):** `2.0rem` (32px), `font-weight: 700`, `line-height: 1.2`
* **`h2` (Títulos de Secção):** `1.5rem` (24px), `font-weight: 600`, `line-height: 1.3`
* **`h3` (Subtítulos de Artigo):** `1.25rem` (20px), `font-weight: 600`, `line-height: 1.4`
* **Corpo de Texto (`p`, `li`, `td`):** `1.0rem` (16px), `font-weight: 400`, `line-height: 1.6`
* **Texto Secundário / Rodapé (`small`, `footer`):** `0.875rem` (14px), `font-weight: 400`, `line-height: 1.5`

---

## 4. Cálculo e Validação dos Rácios de Contraste (WCAG 2.2)

De acordo com as diretrizes WCAG 2.2 (Critério de Sucesso 1.4.3 - Contraste Mínimo):
* **Texto Normal (< 18pt / 24px regular ou < 14pt / 18.66px negrito):** Rácio mínimo de **4,5:1**.
* **Texto Grande (>= 18pt / 24px regular ou >= 14pt / 18.66px negrito):** Rácio mínimo de **3:1**.

### Fórmula de Luminância Relativa
Para cada canal sRGB ($R, G, B \in [0, 1]$):
$$C_{\text{linear}} = \begin{cases} \frac{C}{12.92}, & C \le 0.04045 \\ \left(\frac{C + 0.055}{1.055}\right)^{2.4}, & C > 0.04045 \end{cases}$$

Luminância relativa ($L$):
$$L = 0.2126 \times R_{\text{linear}} + 0.7152 \times G_{\text{linear}} + 0.0722 \times B_{\text{linear}}$$

Rácio de Contraste ($CR$):
$$CR = \frac{L_1 + 0.05}{L_2 + 0.05} \quad (\text{onde } L_1 > L_2)$$

### Tabela de Verificação dos Pares de Cores

| Par de Cores (Frente / Fundo) | Rácio Calculado | Exigência Mínima | Classificação WCAG 2.2 |
| :--- | :---: | :---: | :---: |
| **Texto Grafite (`#1A202C`) sobre Fundo Neutro (`#F7FAFC`)** | **15.57:1** | 4,5:1 (Texto Normal) | **Aprovado (AAA)** |
| **Texto Branco (`#FFFFFF`) sobre Azul Douro (`#1A365D`)** | **12.14:1** | 4,5:1 (Texto Normal) | **Aprovado (AAA)** |
| **Título Azul Douro (`#1A365D`) sobre Fundo Neutro (`#F7FAFC`)** | **11.58:1** | 3,0:1 (Texto Grande) | **Aprovado (AAA)** |
| **Dourado Vinho (`#975A16`) sobre Fundo Neutro (`#F7FAFC`)** | **5.29:1** | 4,5:1 (Texto Normal) | **Aprovado (AA)** |
| **Texto Branco (`#FFFFFF`) sobre Rodapé Granito (`#4A5568`)** | **7.53:1** | 4,5:1 (Texto Normal) | **Aprovado (AAA)** |
| **Texto Secundário (`#4A5568`) sobre Fundo Neutro (`#F7FAFC`)** | **7.18:1** | 4,5:1 (Texto Normal) | **Aprovado (AAA)** |

---

## 5. Regras de Componentes Visuais

1. **Imagens e Elementos Multimédia:**
   * Todas as imagens de destaque possuem cantos arredondados suaves (`border-radius: 12px;`).
   * Sombras discretas para dar destaque sobre o fundo (`box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);`).
2. **Navegação Global (`nav`):**
   * Disposição horizontal limpa com espaçamento confortável entre ligações.
   * Destaque na ligação ativa através de sublinhado inferior com a cor Dourado Vinho do Porto (`border-bottom: 2px solid #975A16`).
3. **Formulários e Controlos Interativos:**
   * Áreas de toque confortáveis com preenchimento interno (`padding`).
   * Realce de foco acessível com indicador nítido para navegação por teclado (`outline: 2px solid #1A365D; outline-offset: 2px;`).