# Lucas Humberto jesus de Lima - 12011ECP011

## Semana 03b – Amplificadores Operacionais

### Da playlist: https://www.youtube.com/watch?v=U0XaljeXVn8&list=PLf1lowbdbFIBSLXMLK4NoGgml7l5rK922assista aos vídeos, de 8à 11e produza um material explicando: 
### a) as características dos Amplificadores Ideais;

1. Ganho infinito de malha aberta (Aol): Um amplificador operacional ideal tem um ganho de tensão de malha aberta infinitamente grande. Isso significa que ele pode amplificar pequenos sinais de entrada para uma tensão de saída arbitrariamente alta. Em termos matemáticos, Aol → ∞.
1. Impedância de entrada infinita: A impedância de entrada de um amplificador operacional ideal é infinita. Isto implica que nenhuma corrente flui para os terminais de entrada do amplificador operacional, garantindo que ele não carregue a fonte conectada a ele. Em termos práticos, isso significa que o amplificador operacional não consome corrente de entrada.
1. Zero Output Impedance: The output impedance of an ideal op-amp is zero. This means it can supply any amount of current to the load without affecting the voltage at its output terminals.
1. Largura de banda infinita: Um amplificador operacional ideal tem uma largura de banda infinitamente ampla, o que significa que pode amplificar sinais de qualquer frequência sem distorção. Na realidade, os amplificadores operacionais reais têm uma largura de banda limitada.
1. Taxa de rejeição de modo comum infinita (CMRR): Os amplificadores operacionais ideais rejeitam completamente qualquer sinal de entrada que seja comum a ambas as entradas (ou seja, o sinal de modo comum). Isso resulta em um CMRR infinitamente alto.
1. Zero Input Offset Voltage: An ideal op-amp has no input offset voltage, meaning that its inverting and non-inverting inputs are perfectly balanced and have identical voltages when the inputs are equal.
1. Zero Input Bias Current: The ideal op-amp has zero input bias current, meaning that no current flows into or out of its input terminals.
1. Infinite Slew Rate: An ideal op-amp has an infinite slew rate, meaning it can change its output voltage instantaneously in response to changes at its input. In practice, real op-amps have limited slew rates.
1. No Noise: In the ideal case, op-amps are completely noise-free, meaning they do not add any noise to the signals they amplify. However, real-world op-amps do introduce some noise.
1. Sem limitações de fonte de alimentação: Os amplificadores operacionais ideais podem operar com uma faixa ilimitada de tensão de fonte de alimentação, permitindo-lhes lidar com tensões de entrada e saída positivas e negativas sem saturação.


### b) o funcionamento do seguidor de tensão e suas possíveis aplicações.

O Amp-op pode ser usado como um seguidor de tensão curto-circuitando o terminal V<sub>O</sub> com o terminal V<sub>-</sub>, e ligando a entrada em V<sub>+</sub>. Considerando o curto virtual entre V<sub>+</sub> e V<sub>-</sub>, e as correntes de entrada serem nulas, existe uma isolação entre o sinal de entrada e o de saída, porém, o segundo possui o mesmo valor de tensão do primeiro. Esse circuito pode ser aplicado em ocasiões em que se necessite uma isolação entre os sinais de entrada e o restante do circuito, como em entradas ADC de microcontroladores.

### c) Amplificador Subtrator.

Dado o circuito:
![exemplo de circuito subtrator](/3b/imagens/subtractor.jpg)

É necessário retirar uma equação para V<sub>O</sub>. Para isso, primeiro são montadas as equações de V<sub>+</sub> e V<sub>-</sub>.

Para V<sub>+</sub>
$$
\begin{align}
    i_2 = i_3\\[5mm]
    
    \frac{v_B-v_+}{R_2}=\frac{v_+}{R_3}\\[5mm]
    
    v_+(\frac{1}{R_2}+\frac{1}{R_3})=\frac{v_B}{R_2}\\[5mm]
    
    v_+(\frac{R_2+R_3}{R_2R_3})=\frac{v_B}{R_3}\\[5mm]
    
    v_+=v_B(\frac{R_3}{R_2+R_3})
    
\end{align}
$$
Para V<sub>-</sub>:
$$
\begin{align}
    i_1=i_2\\[5mm]

    \frac{v_A-v_-}{R1}=\frac{v_-v_O}{R_f}\\[5mm]
    v_-(\frac{R_1+R_f}{R_1R_f})=\frac{v_O}{R_f}+\frac{v_A}{R_1}\\[5mm]
    v_-=(\frac{R_1R_f}{R_1+R_f})(\frac{v_O}{R_f}+\frac{v_A}{R_1})\\[5mm]

\end{align}
$$

Igualando $v_+$ e $v_-$
$$
\begin{align}
    v_+=v_-\\[5mm]
    v_B(\frac{R_3}{R_2+R_3})=(\frac{R_1R_f}{R_1+R_f})(\frac{v_O}{R_f}+\frac{v_A}{R_1})\\[5mm]
    A=(\frac{R_3}{R_2+R_3})\\
    v_B(\frac{R_3}{R_2+R_3})=v_O(\frac{R_1}{R_1+R_f})+v_A(\frac{R_2}{R_1+R_f})\\[5mm]
    B=(\frac{R_2}{R_1+R_f})\
    C=(\frac{R_1}{R_1+R_f})\\
    v_O=\frac{1}{\frac{R_1}{R_1+R_f}}(\frac{R_3}{R_2+R_3}v_B-\frac{R_2}{R_1+R_f}v_A) \\[10mm]

\end{align}
$$
Tornando todos os resistores iguais a 1:

$$
\begin{align}
   v_O=2(\frac{1}{2}v_B-\frac{1}{2}v_A)\\[5mm]
   v_o=v_B-v_A

\end{align}
$$




### Veja os vídeos relativos às aulas 10e 11 da playlist apresentada e produza um resumo, detalhado, sobre as diferençasentre os Amplificadores Operacionais ideais e não ideais.
https://www.youtube.com/watch?v=LW_H29iGxXY&list=PLxI8Can9yAHevRkQnSgviIgnzCH3Nss_Y&index=10

Amplificador operacional ideal:

1. Ganho infinito de malha aberta (Aol): Os amplificadores operacionais ideais têm um ganho de tensão de malha aberta infinitamente grande, o que significa que podem amplificar sinais de entrada para uma tensão de saída arbitrariamente alta.

1. Impedância de entrada infinita: A impedância de entrada de um amplificador operacional ideal é infinita, o que significa que ele não consome corrente de entrada e não carrega a fonte.

1. Impedância de saída zero: Os amplificadores operacionais ideais têm impedância de saída zero, permitindo-lhes fornecer qualquer quantidade de corrente à carga sem afetar a tensão de saída.

1. Largura de banda infinita: Os amplificadores operacionais ideais têm uma largura de banda infinitamente ampla, permitindo-lhes amplificar sinais de qualquer frequência sem distorção.

1. Taxa de rejeição de modo comum infinita (CMRR): Eles rejeitam perfeitamente qualquer sinal de modo comum, garantindo que apenas o sinal diferencial seja amplificado.

1. Tensão de deslocamento de entrada zero: Os amplificadores operacionais ideais não têm tensão de deslocamento de entrada, o que significa que suas entradas inversoras e não inversoras são perfeitamente balanceadas.

1. Corrente de polarização de entrada zero: Eles exibem corrente de polarização de entrada zero, o que significa que nenhuma corrente flui para dentro ou para fora de seus terminais de entrada.

1. Taxa de variação infinita: Os amplificadores operacionais ideais têm uma taxa de variação infinita, permitindo-lhes alterar a tensão de saída instantaneamente.

1. Sem ruído: No caso ideal, os amplificadores operacionais são livres de ruído e não adicionam nenhum ruído aos sinais que amplificam.

1. Sem limitações de fonte de alimentação: Eles podem operar com uma faixa ilimitada de tensão de alimentação, lidando com tensões de entrada e saída positivas e negativas sem saturação.

Amplificador operacional não ideal:

1. Ganho finito de malha aberta (Aol): Os amplificadores operacionais do mundo real têm ganhos de tensão finitos em malha aberta, geralmente na faixa de dezenas de milhares a milhões.

1. Impedância de entrada finita: Os amplificadores operacionais não ideais têm impedância de entrada finita, o que significa que consomem alguma corrente de entrada e podem carregar a fonte até certo ponto.

1. Impedância de saída diferente de zero: Eles têm impedância de saída diferente de zero, o que pode afetar sua capacidade de acionar cargas sem distorção.

1. Largura de banda limitada: Amplificadores operacionais reais têm largura de banda limitada e seu desempenho varia com a frequência.

1. CMRR finito: embora tenham um bom CMRR, não é infinito, portanto, ainda podem amplificar alguns sinais de modo comum até certo ponto.

1. Tensão de deslocamento de entrada diferente de zero: Os amplificadores operacionais não ideais têm uma tensão de deslocamento de entrada, resultando em uma pequena diferença de tensão entre suas entradas inversoras e não inversoras.

1. Corrente de polarização de entrada diferente de zero: Eles exibem alguma corrente de polarização de entrada, que pode introduzir erros de deslocamento em circuitos de alta impedância.

1. Taxa de variação limitada: Os amplificadores operacionais reais têm taxas de variação finitas, afetando sua capacidade de responder rapidamente a mudanças rápidas nos sinais de entrada.

1. Ruído: Podem introduzir ruído nos sinais que amplificam, dependendo do seu design e especificações.

1. Limitações da fonte de alimentação: Os amplificadores operacionais não ideais têm limitações de tensão e corrente e podem não lidar com amplas faixas de tensão sem distorção ou saturação.

Em aplicações práticas, os engenheiros selecionam amplificadores operacionais com base em seus requisitos específicos, levando em consideração as características e limitações não ideais para garantir que o circuito funcione conforme pretendido.