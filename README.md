## ARQUITETURA E IMPLEMENTAÇÃO DO CONVERSOR PYTHON PARA SISTEMAS NUMÉRICOS (BINÁRIO E HEXADECIMAL)

Universidade Anhanguera  
São Paulo — 2025

    Trecho extraído do relatório:  
    Este relatório técnico apresenta o desenvolvimento, a fundamentação teórica e a análise de desempenho de um software conversor implementado em linguagem Python 3.12+. O sistema realiza a transformação de cadeias de caracteres em representações hexadecimal e binária de 8 bits, utilizando o padrão de codificação UTF-8.

Resumo

Este relatório técnico apresenta o desenvolvimento, a fundamentação teórica e a análise de desempenho de um software conversor implementado em linguagem Python 3.12+. O sistema realiza a transformação de cadeias de caracteres em representações hexadecimal e binária de 8 bits, utilizando o padrão de codificação UTF-8.

A implementação priorizou eficiência computacional por meio da utilização de expressões geradoras e interpolação de strings com f-strings. Os resultados demonstram precisão absoluta na conversão de caracteres pertencentes ao padrão ASCII. A documentação segue as diretrizes da ABNT, assegurando padronização e qualidade técnico-científica.

Palavras-chave: sistema binário; sistema hexadecimal; Python; codificação UTF-8; documentação técnica.
Sumário

    1 Introdução

    2 Objetivos

    3 Fundamentação Teórica

        3.1 Sistemas de Numeração Posicionais

        3.2 Estrutura de Bits e Bytes

        3.3 Tabela de Equivalência

    4 Metodologia e Implementação

        4.1 Análise do Código Fonte

        4.2 Eficiência e Tratamento de Dados

    5 Análise de Resultados

        5.1 Validação

    6 Conclusões

    Referências

1 Introdução

A representação de dados constitui o fundamento da computação moderna. Apesar da abstração promovida por linguagens de alto nível, todo processamento computacional é realizado por meio da manipulação de bits organizados em bytes.

Ferramentas de conversão entre sistemas numéricos são essenciais para o estudo de arquitetura de computadores, depuração de protocolos de comunicação, análise de tráfego de rede e implementação de mecanismos criptográficos. A precisão na conversão de bases numéricas garante integridade durante processos de transmissão e armazenamento de dados.
2 Objetivos

O objetivo geral deste projeto é desenvolver um conversor funcional em ambiente Python 3.12+ capaz de:

    Processar entradas textuais;

    Gerar representações exatas em hexadecimal;

    Gerar representações binárias alinhadas em 8 bits;

    Utilizar o padrão UTF-8 como codificação base.

Este relatório documenta a transição entre a fundamentação matemática dos sistemas posicionais e sua implementação prática em software.
3 Fundamentação Teórica
3.1 Sistemas de Numeração Posicionais

Um sistema de numeração posicional atribui valor aos algarismos conforme sua posição e a base adotada.

    Sistema Decimal (Base 10): utiliza dez símbolos (0–9).

    Sistema Binário (Base 2): utiliza dois símbolos (0 e 1), sendo o sistema natural dos computadores digitais.

    Sistema Hexadecimal (Base 16): utiliza dezesseis símbolos (0–9 e A–F), permitindo representar um byte com apenas dois caracteres.

3.2 Estrutura de Bits e Bytes

    Bit (Binary Digit): menor unidade de informação digital.

    Byte: agrupamento de 8 bits; unidade básica de armazenamento.

    No padrão UTF-8, caracteres da faixa ASCII ocupam exatamente um byte, permitindo mapeamento direto para representações binárias e hexadecimais.

3.3 Tabela de Equivalência
Decimal	Binário (4 bits)	Hexadecimal
0	0000	0
1	0001	1
2	0010	2
3	0011	3
4	0100	4
5	0101	5
6	0110	6
7	0111	7
8	1000	8
9	1001	9
10	1010	A
11	1011	B
12	1100	C
13	1101	D
14	1110	E
15	1111	F
4 Metodologia e Implementação

A implementação foi desenvolvida em Python 3.12, utilizando o método encode('utf-8') para converter strings Unicode em bytes reais.

A arquitetura lógica baseia-se em:

    Conversão explícita para bytes;

    Iteração sobre valores numéricos individuais;

    Formatação via f-strings;

    Geração eficiente de saída por meio de expressões geradoras.

4.1 Análise do Código Fonte

    O método de conversão para hexadecimal utiliza formatação de dois dígitos com padding zero.

    O método de conversão para binário utiliza formatação de oito bits, garantindo alinhamento completo de byte.

4.2 Eficiência e Tratamento de Dados

    Complexidade algorítmica: O(n), onde n é o número de bytes processados.

    Uso de expressões geradoras reduz consumo de memória temporária.

    f-strings oferecem desempenho otimizado na interpolação de strings.

Bloco de código (implementação em Python)
python
