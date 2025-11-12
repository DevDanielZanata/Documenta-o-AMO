Vimos como o Windows carrega DLLs e o papel da ***DllMain*** (ex: DLL\_PROCESS\_ATTACH). Aprendemos que código malicioso costuma ficar em **DllMain** (na attach), em TLS callbacks, em funções exportadas ou em seções incomuns e que existe ainda o reflective loading, quando a DLL se carrega sem passar pelo loader normal.





**DLL\_PROCESS\_ATTACH:** *"acionado quando a DLL entra num processo (LoadLibrary ou loader); usado pra inicializar recursos roda uma vez por processo."*

**DLL\_PROCESS\_DETACH:** *"acionado quando a DLL sai do processo (FreeLibrary ou processo terminando); usado pra liberar recursos também roda uma vez por processo."*





Pra achar esse código: monitorar LoadLibrary e GetProcAddress, checar o entry point do módulo, inspecionar TLS callbacks, analisar seções suspeitas no disassembler e colocar breakpoints no DllMain, nas exports ou nas APIs que a DLL chama. 



Um código de chamada de Malware. (**Exe -> DLL**)



'''

LoadLibray("dll.dll") //fdwReason = 1



dll -> DllMain(hInstDLL, fdwReason, lpReserved)



if (fdwReason == 1)

&nbsp;	......;



//



exe loadlibray("nomemalware.dll");

f = getprocaddress(nome\_function\_export)

f()





'''



***"fdwReason é um parâmetro utilizado na programação de software para sistemas operacionais Windows, especificamente na função de ponto de entrada de uma DLL (Dynamic Link Library), chamada DllMain***"



[https://learn.microsoft.com/pt-br/windows/win32/dlls/dllmain](https://learn.microsoft.com/pt-br/windows/win32/dlls/dllmain)

