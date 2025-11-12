Na aula 24 a parada foi ***DLL injection***, a ideia era colocar codigo dentro de outro processo pra rodar com as permissoes dele. Mostraram 3 programas na pratica:



* **TargetApp.Exe** -> Processo que sera manipulado.



* **Injector.Dll** -> DLL simples que so fazia um MessageBox (o payload que a gente injeta).



* **Injetor.Exe** -> o programa que faz a injeção usando o PID do processo alvo. Ele abre o processo com OpenProcess pedindo PROCESS\_ALL\_ACCESS, aloca memoria remota com VirtualAllocEx e escreve o caminho da DLL ali via WriteProcessMemory. Depois cria uma thread remota com CreateRemoteThread e aponta pra LoadLibrary, passando como parametro o endereco (ESI -> 0x5B000 no exemplo) onde o caminho da DLL foi escrito.



O processo alvo que recebe a DLL e executa o DllMain quando o loader carrega o modulo.



Resumo: o exe pega o PID, abre o processo, injeta o caminho da DLL na memoria do alvo, e dispara LoadLibrary dentro do processo remoto via CreateRemoteThread pra carregar a Injector.Dll, ai o MessageBox roda com as permissoes do processo injetado.

