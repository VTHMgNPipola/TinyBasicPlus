TinyBasic Plus BR Edition
==============

Esta é uma versão em português brasileiro do firmware/os TinyBasic Plus, desenvolvido em C.

# Lista completa de comandos suportados

## Sistema
- SHH		- *Sai do BASIC (faz um soft-reboot no Arduino)*
- FIM 		- *Termina a execução do programa, igual à "PARE"*
- MEM		- *Imprime as estatísticas de uso de memória*
- NVO		- *Cria um novo programa limpando todo o código existente*
- EXE		- *Executa o programa*

## I/O de arquivos/Cartão SD
- ARQVS		- 	*Lista os arquivos no cartão SD*
- CARREGAR filename.bas	- *Carrega um arquivo do cartão SD*
- CHAIN filename.bas - *equivalente: NVO, CARREGAR filename.bas, EXE*
- SALVAR filename.bas	- *Salva o programa sendo editado no cartão SD, sobre-escrevendo*

## EEProm
- EFORMAT	- Limpa o EEPrin
- ELOAD		- Carrega o programa no EEProm
- ESAVE		- Salva o programa atual no EEProm
- ELIST		- Lista o programa dentro do EEProm
- ECHAIN	- Carrega o programa no EEProm e executa-o

## I/O
- PEEK( endereco )	- *Define um valor na memória* (não implementado)
- POKE			- *Retorna um valor na memória* (não implementado)
- SAIDA expressao	- *Imprime (escreve) "expressao" na tela. Igual à "?"*
- REM coisas		- *Remarca/comenta. Igual à "'"*

## Expressões e Matemática
- A=V, DEF A=V	- *Define um valor a uma variável*
- +, -, \*, / - *Matemática geral*
- <,<=,=,<>,!=,>=,> - *Comparações*
- ABS( expression )  - *Retorna o valor absoluto da expressão*
- SRAND( v ) - *Define a semente randômica para "v"*
- RND( m ) - *Retorna um valor randômico de 0 a "m"*

## Controle
- SE expressao comando - *Executa o comando se "expressao" for verdade*
- PARA variavel = comeco PR fim	- *Começa o bloco "para"*
- PARA variavel = comeco PR fim PSSO valor - *Começa o bloco "para" com um certo número de passos*
- PRXM - *Fim do bloco "para"*
- VAPR linha - *Continua a execução de "linha"*
- VASUB linha - *Chama a subrotina em "linha"*
- RETORNE	- *Retorna de uma subrotina*

## I/O de pinos
- DELAY	timems*- Espera (em milisegundos)*
- DWRITE pin,value - *Define o valor do pino (ALTO,AL,BXO,BX)*
- AWRITE pin,value - *Define o valor do pino com analógico (pwm) 0..255*
- DREAD( pin ) - *Retorna o valor do pino* 
- AREAD( analogPin ) - *Retorna o valor analógico do pino*

## Som - Piezo Speaker
- TONE freq,timems - toca "freq" por "timems" milisegundos (1000 = 1 segundo)
- TONEW freq,timems - O mesmo que o de cima, mas espera que ele termine
- NOTONE - Para a execução de todos os "tones"

NOTA: O comando TONE é desativado por padrão

# Programas de exemplo
Infelizmente, esta modificação do TinyBasic Plus original ainda não foi testada, e por isso não podemos ofereces programas de exemplo, tendo em mente que eles podem não funcionar.

# Autores e contribuidores
- Tiny Basic 68k - Gordon Brandly [Project Page](http://members.shaw.ca/gbrandly/68ktinyb.html)
- Arduino Basic / Tiny Basic C - Michael Field [Project Page](http://hamsterworks.co.nz/mediawiki/index.php/Arduino_Basic)
- Tiny Basic Plus - Scott Lawrence <yorgle@gmail.com> [Github Page](http://github.com/BleuLlama/TinyBasicPlus)

- Jurg Wullschleger - Fix for unary operations and whitespace in expressions

- João Henrique - Tradução para o português

# Links
- [Arduino Microcontroller](http://arduino.cc)

# MIT License

Copyright (c) 2012-2013

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

