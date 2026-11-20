# Decisão Fundamentada da Framework CSS — Portal "Descobrir Gaia e Porto"

*Projeto:* Descobrir Gaia e Porto  
*Etapa:* 7 (Sessão 10 — Frameworks e Finalização de Conteúdos)  
*Framework Escolhida:* *Bootstrap v5.3.3*  

---

## 1. Enquadramento e Critérios de Avaliação

Para selecionar a biblioteca CSS definitiva do portal turístico *"Descobrir Gaia e Porto", realizou-se uma comparação empírica (comparacao.html) implementando o mesmo componente funcional (cartão de ponto turístico da Ponte D. Luís I) em **Bootstrap v5.3.3, **Foundation v6.8.1* e *W3.CSS v4.15*. A avaliação incidiu sobre seis critérios objetivos: peso transferido (KB), volume de código, qualidade da documentação, facilidade de personalização, acessibilidade nativa (WCAG 2.2 / WAI-ARIA) e completude de componentes sem JavaScript adicional.

---

## 2. Análise Comparativa Resumida

* *W3.CSS v4.15 (Descartada):* Apesar de apresentar o menor peso de rede (23 KB bruto / ~5 KB gzip), revelou limitações críticas para um portal sujeito ao Decreto-Lei n.º 82/2022. Não oferece gestão nativa de foco por teclado nem atributos WAI-ARIA integrados nos seus componentes e exige o uso recorrente de !important para sobrepor estilos base, dificultando a manutenção da paleta institucional (#1A365D e #975A16).
* *Foundation v6.8.1 (Descartada):* Apresenta boa estrutura semântica e suporte ARIA (154 KB bruto / ~21 KB gzip), mas exige marcação HTML ligeiramente mais verbosa (16 linhas contra 14 no Bootstrap), possui menor cadência de atualização documental e depende de dependências adicionais para componentes interativos.
* *Bootstrap v5.3.3 (Selecionada):* Embora transfira 232 KB brutos (~31 KB comprimidos em gzip via CDN com cache global), destaca-se como a solução mais equilibrada e fiável para o projeto.

---

## 3. Justificação da Escolha Final (Bootstrap v5.3.3)

A equipa decidiu manter o *Bootstrap v5.3.3* na versão final do sítio pelos seguintes motivos técnicos:

1. *Conformidade Nativa com Acessibilidade (WCAG 2.2):* Fornece suporte integrado para aria-current="page", gestão de foco visível, tabelas responsivas acessíveis (.table-responsive com caption-top) e componentes interativos validados com *100 pontos no Google Lighthouse* e *0 erros no WAVE*.
2. *Personalização Limpa e Escalável:* Permite aplicar rigorosamente a identidade visual do portal (Azul Rio Douro #1A365D e Dourado Vinho do Porto #975A16, com rácio de contraste 5.14:1) através de uma folha externa (bootstrap-custom.css) sem comprometer a responsividade mobile-first.
3. *Documentação Atualizada e Rapidez de Manutenção:* A documentação oficial da série 5.3 inclui exemplos explícitos de acessibilidade para leitores de ecrã e garante estabilidade a longo prazo para todas as seis páginas do portal.