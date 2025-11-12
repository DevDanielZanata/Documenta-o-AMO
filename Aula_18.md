Na aula 18 a gente aprendeu a acelerar a análise de shellcode criando um executável rápido que já contém o payload  assim dá pra rodar e debugar direto, sem ficar copiando bytes ou montando ambientes toda hora.



Como ferramenta foi usado o fasm (flat assembler) ele é rápido, simples e ótimo pra montar esse tipo de coisa.



**FERRAMENTAS PROPOSTAS**



* *FASM*
* *SHELLCODE.EXE*





***FASM***



'''



include 'win32ax.inc' 

.code

start:

&nbsp;   file 'payload.bin'

&nbsp;   ;invoke ExitProcess,0

.end start





'''

