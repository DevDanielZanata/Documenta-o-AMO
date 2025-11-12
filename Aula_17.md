Na aula 17 avançamos na análise do payload que vinha via .bat: desmontamos o funcionamento completo e escrevemos um pequeno programa para interagir com o named pipe que o payload cria, o que permitiu testar respostas e comportamentos. 



Também usamos bp de hardware para parar a execução em pontos críticos sem modificar o binário, o que ajudou a entender rotinas internas, comunicação  e a automatizar testes para reproduzir o comportamento do payload.



Assim fizemos um código que chama essa função **"CallNamedPipe"**



'''



int main(void)



&nbsp;CallNamedPipe("\\\\\\\\.\\\\pipe\\\\status\_b5ba",

&nbsp;		(LPVOID)"\\x04\\x00\\x00\\x00\\x90\\x90\\x90\\x90",

&nbsp;		8,

&nbsp;		NULL,

&nbsp;		0,

&nbsp;		NULL,

&nbsp;		NMPWAIT\_NOWAIT);

&nbsp;return 0;





'''

