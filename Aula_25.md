###### Aula 25, apenas fizemos um código no qual ele localiza os processos:



**Código:**



'''



\#include <iostream>

\#include <Windows.h>

\#include <TlHelp32.h>





int main()

{

&nbsp;   HANDLE hSnap;

&nbsp;   PROCESSENTRY32 pe;

&nbsp;   hSnap = CreateToolhelp32Snapshot(TH32CS\_SNAPPROCESS, 0);



&nbsp;   pe.dwSize = sizeof(pe);

&nbsp;   Process32First(hSnap, \&pe);



&nbsp;   do {

&nbsp;       printf("%ls\\n", pe.szExeFile);

&nbsp;   } while (Process32Next(hSnap, \&pe));







&nbsp;   return 0;

}



'''



No contexto da injeção em processos e válido termos facilmente o controle dos processos que estão ***sendo executados*** em nossa máquina.

