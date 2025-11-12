Na aula 3, foi passado sobre o Software **API MONITOR**, onde que por meio desse software conseguimos monitorar as chamadas a ***API's do Windows***. Assim diante a isto observamos todo o processo que o Ransoware **"NEFILIN"**, faz para obter os arquivos e criptografar, quanto a busca que ele faz por certos arquivos do sistema operacional para ele criptografar, porém apenas aqueles que não danifiquem o sistema.





Um exemplo de chamadas que observamos do NEFILIN:



* **GetFileSize** -> Tamanho Do Arquivo 
* **FindNextFile** -> Procurando os arquivos em diretórios
* **CryptEncrypt** -> Chamada que criptografava.





Também foi mostrado a prática de fazermos "patchs", ou seja identificamos a linha Assembly que faz a criptografia. Assim substituímos ela por um ***"ret"*** e salvamos como patch.

