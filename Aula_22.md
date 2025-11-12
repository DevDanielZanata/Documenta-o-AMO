Na aula 22 a gente entrou no tema de ***DLL side-loading***, um modo onde o malware se disfarça de DLL legítima e é carregado por um programa confiável sem levantar suspeita.



Vimos como esse tipo de ataque acontece, como identificar quando uma DLL maliciosa tá sendo carregada no lugar da original e o que observar.





###### **Oque observar?**



* Ver se a DLL foi carregada de um lugar estranho. 
* Conferir nome, tamanho e assinatura 
* Checar exports unções faltando ou diferentes indicam DLL falsa.
* Observar o comportamento em execução conexões, arquivos, injeções.
* Verificar se a assinatura digital é válida e o hash bate com o original.
