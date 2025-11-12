Aula 28 pegamos um .doc, extraímos a macro em VBA (usando a ferramenta **OfficeMalScanner**) e desmontamos o esquema todo. 



Ele gerou um **"ThisDocument"** a macro pra VBScript, adaptamos a rotina de desofuscação de strings pra funcionar a nosso favor e executamos a lógicapra entender passo a passo o que o documento fazia desde a decodificação das strings até a montagem dos comandos e acionamento do payload.



Está aula, o foco em geral foi adaptar do VBA para o VBScript, já que tem algumas diferenças.



* Exemplo "AS, $, Mid".
