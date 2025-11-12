Aula 26 foi sobre ***"Process Hollowing"*** uma tecnica muito usada por malwares pra executar codigo malicioso dentro de um processo legitimo. Em vez de injetar direto numa thread, o malware cria (ou reutiliza) um processo valido em estado suspenso, desaloca ou substitui o corpo legitimo na memoria e grava seu paload em seu lugar.



depois ajusta o entrypoint e resume o processo, ***fazendo o sistema rodar o codigo malicioso com a imagem e permissoes do processo original***.

Pontos praticos que vimos:





**Devemos prestar atenção em certas chamadas como:**


* VirtualAlloc 
* WriteProcessMemory
* NtUnmapViewOfSection 
* CreateProcess 
* observar modificacoes no entrypoint/context da thread.





Basicamente a técnica process hollowing é = pegar um processo legitimo + substituir seu conteudo em memoria pelo payload malicioso + retomar execucao — o resultado e o malware rodando disfarcado com a identidade do processo alvo.

