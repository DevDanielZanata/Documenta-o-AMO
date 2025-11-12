A **aula 27 mostrou como investigar processos apos uma injeção e como lidar com varias threads no Windows.**



Basicamente a ideia é: primeiro identifique se o processo foi alterado (modulos mapeados estranhos, secoes com codigo diferente do exe em disco, entrypoint apontando pra shellcode) depois devemos focar nas threads, porque o payload costuma rodar como uma thread nova ou reescreve a thread principal.





**Passos praticos que usamos:**



* Verificar as threads do processo (Via ProcessHacker)
* Conferir o start address de cada thread, threads que comecam em enderecos dentro de memoria alocada dinamicamente ou em secoes semecoerencia sao suspeitas
* monitore chamadas de alocacao/escrita (VirtualAlloc,WriteProcessMemory,NtWriteVirtualMemory) e criacao de threads (CreateRemoteThread,SetThreadContext,ResumeThread) pra correlacionar quem injetou o que
* Se tiver multiplas threads concorrendo, isole testando uma a uma (suspende as que sao legitimas, depura a suspeita) ou use breakpoints





