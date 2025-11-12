Nessa aula aprendemos sobre:

API hashing, técnica que substitui nomes de APIs por valores hash e resolve funções comparando esses hashes em runtime.

Usam para ofuscar strings, dificultar detecção e esconder quais APIs serão chamadas.



Basicamente ele pega a tabela exports das dll, calcula o hash da string e pega cada nome, assim compara com a constante se bater ela pega o endereço e faz a chamada.



**Como detectar?** 

* &nbsp;procurar loops que percorrem export table
* &nbsp;constantes numéricas repetidas e operações adição de bytes
* &nbsp;também debuggar em runtime





Exemplo: (Pseudocodigo)

'''

genHash(string nomeFn)

&nbsp;   //Meu calculo

return hash;



for e in exports("KERNEL32.DLL"):

&nbsp; hash = genHash(e)

if hash == 0x310227D0

&nbsp; return pCreateFile

else if hash == .....

&nbsp; 



'''

