Equipe Capivara: AG
*   Anthony Santos
*   Renan de Barros
*   Ariane Fernandes
*   Jhonata Martins
*   Felipe Nascimento
*   Vivia Câmara

# Otimizacao Plano Cultivo

Otimização do Plano de Cultivo de uma Multinacional com implementação do Algoritmo Genético para otimização do plano de cultivo.

## Objetivo
Selecionar a melhor combinação Produto-Estado para maximizar o lucro total, respeitando:
1.  *Área Máxima:* 15.000 hectares.
2.  *Diversidade Mínima:*
    * Bananas em pelo menos 10 estados.
    * Laranjas em pelo menos 5 estados.
    * Maracujá em pelo menos 5 estados.

## Estrutura do Projeto
* src/: Código fonte modularizado (Engine do AG e Utilitários).
* data/: Base de dados (PAM - Produção Agrícola Municipal)
* figures/: Gráficos de convergência gerados.
* notebook.ipynb: Relatório executável com análises.

## 🚀 Como Executar
1. Abra o notebook.ipynb no Colab.
2. Instale as dependências: pip install pandas numpy matplotlib
3. Execute todas as células para rodar a bateria de 5 testes.

## 📊 Resultados da Experimentação
O algoritmo foi executado 5 vezes para validação estatística.
* *Melhor Lucro Encontrado:* R$ 654,245,915.00
* *Tempo Médio de Execução:* 0.254 segundos
* *Comportamento:* O algoritmo demonstrou convergência estável, superando máximos locais através de uma taxa de mutação ajustada (5%) e elitismo (20%).
* *Convergência:* Em todas as rodadas, o algoritmo foi capaz de sair de uma zona de penalidade (fitness negativo) para uma zona de lucro positivo dentro das primeiras 10 gerações.
* *Variação:* Embora o número de amostras seja reduzido ($N=5$), observou-se que a diferença entre a melhor e a pior execução não foi significativa a ponto de invalidar o modelo. Isso sugere que as restrições impostas (penalidades de 1 milhão) funcionam bem para guiar a busca, independentemente da população inicial.
* *Gráfico:* A análise visual da curva de evolução do fitness (no gráfico) demonstra uma convergência robusta. Observa-se um crescimento acentuado do lucro nas primeiras 15 gerações, indicando a rápida eliminação de soluções penalizadas (inviáveis). A partir da 60ª geração, o sistema atinge um platô de estabilidade, sugerindo que o algoritmo encontrou um ponto de saturação (convergência) próximo a 650 milhões. A ausência de quedas bruscas ao longo da curva reforça que a estratégia de Elitismo foi eficaz em preservar as melhores características genéticas ao longo do processo evolutivo.

O desenvolvimento deste projeto demonstrou a eficácia da computação evolutiva na resolução de problemas complexos de otimização agrícola. Através da implementação de operadores genéticos clássicos (crossover de ponto único, mutação e seleção por elitismo) aliados a uma função de aptidão com penalidades rigorosas, foi possível maximizar o lucro da safra respeitando todas as restrições de área e diversidade de culturas. As simulações realizadas indicam que o modelo é robusto, apresentando convergência estável e rápida.


## License

MIT License

Copyright (c) 2025 Ariane Fernandes

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
