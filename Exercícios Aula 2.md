2.Intel Core i9 (14ª geração) — RISC ou CISC?CISC

Apple M3 — RISC ou CISC? RISC

ARM Cortex-A78 (usado em boa parte dos celulares Android) — RISC ou CISC? RISC

AMD Ryzen 9 — RISC ou CISC? CISC

Um núcleo CUDA de uma GPU NVIDIA — se aproxima mais de qual filosofia, e por quê?

Bônus: as CPUs Intel/AMD modernas são CISC 'por fora', mas por dentro traduzem cada instrução CISC em microinstruções parecidas com RISC antes de executar. Pesquise esse conceito (chamado de 'micro-ops') e explique, em 2-3 frases, por que os fabricantes fazem isso.

As CPUs Intel e AMD transformam instruções CISC em micro-ops (µops) antes de executá-las. Isso aumenta o desempenho e mantém a compatibilidade com programas antigos.



4.Exercício quantitativo, sem computador — só matemática. Considere um pipeline de 5 estágios (Busca, Decodifica, Executa, Memória, Escreve), 1 ciclo por estágio.



Sem pipeline (uma instrução só começa depois que a anterior termina TUDO): quantos ciclos levam 4 instruções? E 10 instruções? (fórmula: N instruções × 5 ciclos)

Com pipeline (como no diagrama que vimos): quantos ciclos levam 4 instruções? E 10 instruções? (fórmula: 5 ciclos pra 'encher' o pipeline + 1 ciclo por instrução extra)

Calcule o speedup (quantas vezes mais rápido) do pipeline pra 4 instruções, e de novo pra 10 instruções. O speedup aumenta, diminui, ou fica igual conforme o número de instruções cresce?

Bônus: se o número de instruções crescesse até o infinito, pra que valor o speedup se aproximaria? (Dica: pense no que acontece com o '+5 ciclos iniciais' quando N é gigante.)

Resposta:

1\. Sem pipeline (N × 5 ciclos):



4 instruções: 4 × 5 = 20 ciclos

10 instruções: 10 × 5 = 50 ciclos

2\. Com pipeline (5 + N − 1 = N + 4 ciclos):



4 instruções: 5 + 3 = 8 ciclos

10 instruções: 5 + 9 = 14 ciclos

3\. Speedup (Sem pipeline ÷ Com pipeline):



4 instruções: 20 ÷ 8 = 2,5×

10 instruções: 50 ÷ 14 ≈ 3,6×

Resposta: O speedup aumenta conforme o número de instruções cresce.



Bônus:

Quando o número de instruções tende ao infinito, o speedup se aproxima de 5×, porque os 5 ciclos iniciais passam a ter impacto cada vez menor.



5.Em 2020, a Apple anunciou que ia parar de usar processadores Intel (x86, CISC) nos Macs, e passar a usar chips próprios (Apple Silicon: M1, M2, M3...), baseados em ARM (RISC).



Pesquisa + um parágrafo de análise escrita, conectando com os conceitos técnicos de hoje.

Pra responder / entregar

Pesquise e liste pelo menos 2 vantagens reais que a Apple (ou analistas de mercado) apontaram nessa migração — cite as fontes.

Escreva um parágrafo (5-8 frases) conectando essas vantagens com os conceitos de RISC vistos hoje: simplicidade de instrução, facilidade de pipeline, e o que isso significa pra consumo de energia (importante pra bateria de notebook).

Esse tipo de decisão (trocar toda uma linha de produtos de arquitetura) também está acontecendo em outros lugares — pesquise se alguma empresa de servidores de nuvem (AWS, Google, Microsoft) também está usando chips ARM próprios nos seus data centers, e por quê isso pode interessar especificamente pra quem treina modelos de IA em larga escala.



Resposta:

1\. Vantagens da migração para Apple Silicon (ARM)

Maior desempenho por watt, oferecendo mais desempenho com menor consumo de energia, o que aumenta a autonomia da bateria. 

Integração entre hardware e software, permitindo melhor otimização do macOS e dos aplicativos, além de facilitar o desenvolvimento para todo o ecossistema Apple. 

Fontes:



Apple – anúncio da transição para Apple Silicon. 

Amazon – explicação sobre eficiência da arquitetura ARM. 



2\. Análise

A mudança da Apple para chips ARM está ligada aos princípios da arquitetura RISC, que utiliza instruções mais simples e eficientes. Isso facilita o uso de pipeline, permitindo executar instruções com maior rapidez. Como o processador realiza menos trabalho para cada instrução, o consumo de energia também diminui. Essa eficiência resulta em notebooks com maior duração de bateria e menor aquecimento. Além disso, a integração entre hardware e software melhora ainda mais o desempenho geral. Por isso, a Apple conseguiu oferecer Macs mais rápidos e eficientes com os chips da família M. 





3\. Outras empresas também usam ARM?

Sim. Empresas como a AWS utilizam os processadores Graviton (ARM) em seus data centers, e o Google Cloud usa os processadores Axion (ARM). Esses chips oferecem melhor desempenho por custo e maior eficiência energética. Para treinar e executar modelos de IA em larga escala, isso ajuda a reduzir o consumo de energia, os custos de operação e melhora a eficiência dos servidores, especialmente nas tarefas que dependem da CPU. 















