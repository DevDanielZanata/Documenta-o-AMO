Na Aula 19 foi apresentado o Runtime linking e o processo de resolver e ligar funcoes de bibliotecas (DLLs) durante a execucao do programa, em vez de deixar tudo resolvido pelo loader do Windows quando o exe inicia. 



Em vez de ter todas as funcoes listadas na tabela de importacao do PE (Import Table) e ja prontas no load, o programa carrega DLLs e pega enderecos de funcoes so quando precisa isso permite codigo mais flexivel (e tambem e util pra ofuscacao).





* No decorrer da aula ele apresentou um .exe que ele próprio fez na onde nos mostra o uso da "MessageBox", na qual precisa da "USER32.DLL". Porém nos imports não possui ela apenas a Kernal32.dll e as chamdas de GetProcAddress e a LoadLibrayA. Ou seja debbugando esse código conseguimos ver que a biblioteca estava rodando em tempo de execução com as chamdas da LoadLibrayA
