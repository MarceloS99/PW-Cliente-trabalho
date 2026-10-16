# Documento de Planeamento do Projeto — Descobrir Gaia & Porto

**Unidade Curricular:** Programação Web - Cliente (15791)  
**Instituição:** ISLA Gaia — 1.º Ciclo em Engenharia Informática  
**Docente:** José Augusto de Araújo Monteiro  
**Grupo:** Marcelo Sousa, Diogo Cruz, Eurico Cunha, João Teixeira  
**Tema:** Guia Turístico e Cultural de Vila Nova de Gaia e Porto  

---

## 1. Etapa de Análise

### 1.1 Identificação do Problema e Oportunidade
Vila Nova de Gaia e Porto partilham um património cultural, histórico e gastronómico único, dividido e ligado pelas pontes sobre o Rio Douro. Contudo, muitos visitantes enfrentam dificuldades em encontrar um guia integrado, leve e acessível que conjugue as duas margens de forma harmoniosa.

### 1.2 Público-Alvo
* **Turistas Nacionais e Estrangeiros:** Interessados em explorar património, gastronomia típica e roteiros a pé de 1 a 2 dias.
* **Cidadãos com Necessidades Especiais:** Utilizadores dependentes de tecnologias de apoio (leitores de ecrã, navegação exclusiva por teclado ou elevado contraste).
* **Utilizadores Móveis:** Visitantes em circulação pedonal com dispositivos móveis de diferentes dimensões (ecrãs a partir de 360 px).

### 1.3 Requisitos Globais do Sistema
* Conformidade rigorosa com os padrões W3C (HTML5 válido).
* Acessibilidade digital orientada pelas normas WCAG 2.2 (Nível AA) e legislação nacional (Decreto-Lei n.º 82/2022).
* Arquitetura estática leve, sem dependências de processamento no lado do servidor ou bases de dados.

---

## 2. Etapa de Planeamento

### 2.1 Âmbito e Estrutura de Páginas
O sítio é composto por 6 páginas estáticas principais com navegação global coerente:
1. `index.html`: Boas-vindas, visão geral e pontos turísticos emblemáticos.
2. `monumentos.html`: Apresentação histórica do património e tabela de visitação.
3. `gastronomia.html`: Roteiro de sabores tradicionais e caves de vinho.
4. `roteiros.html`: Sugestões práticas de itinerários e dicas de percurso.
5. `contactos.html`: Formulário acessível de pedidos de informação com validação nativa.
6. `acessibilidade.html`: Declaração formal de acessibilidade e compromisso normativo.

### 2.2 Metodologia de Trabalho e Gestão de Versões
* **Controlo de Versões:** Gestão em repositório GitHub através do ramo `main`.
* **Trabalho Colaborativo:** Rastreabilidade individual de tarefas e trabalho em par com créditos explícitos via `Co-authored-by`.
* **Marco de Entregas:** Progressão semanal indexada.

---

## 3. Etapa de Desenho

### 3.1 Arquitetura de Informação e Wireframes
* Definição de sitemap hierárquico com matriz de navegação direta (`docs/sitemap.md`).
* Esquemas estruturais de baixa fidelidade (`docs/wireframes.md`), garantindo consistência na colocação de elementos-chave (cabeçalho, barra de menu, conteúdo principal e rodapé).

### 3.2 Princípios de Design e Usabilidade
* **Abordagem Mobile-First:** Conceção focada inicialmente em ecrãs pequenos (360 px) com expansão progressiva por grelhas e flexbox.
* **Hierarquia Visual e Acessibilidade:** Uso exclusivo de um único `<h1>` por página.

---

## 4. Etapa de Implementação

### 4.1 Tecnologias Adotadas
* **Marcação Semântica:** HTML5 puro com elementos estruturais explícitos (`header`, `nav`, `main`, `section`, `article`, `footer`, `figure`, `figcaption`).
* **Estilização e Responsividade:** CSS3 externo estruturado, com recurso a variáveis e regras organizadas (previsto para E3/E4).
* **Validação de Dados:** Mecanismos nativos do cliente em formulários (`required`, `type`, `pattern`, `minlength`), assegurando que utilizadores recebam retorno imediato de erros.

### 4.2 Verificação Contínua de Qualidade
* Validação de sintaxe a 100% no validador do W3C, garantindo 0 erros e 0 avisos em todas as iterações.

---

## 5. Etapa de Marketing 

### 5.1 Otimização para Motores de Busca
* Títulos (`<title>`) únicos e contextuais por página, refletindo a temática exata do conteúdo.
* Meta-etiquetas de descrição (*meta description*), definição correta de idioma (`lang="pt"`) e tags de viewport para indexação mobile prioritária.
* Estrutura de ligações internas descritivas sem quebras e recurso a textos alternativos (`alt`) descritivos e contextuais em todas as imagens.

### 5.2 Estratégia de Divulgação e Publicação
* Publicação contínua e alojamento aberto através de GitHub Pages para testes públicos e verificação docente.
* Divulgação do portal em diretórios locais de turismo e plataformas comunitárias da Área Metropolitana do Porto.