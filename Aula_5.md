###### Nesta aula foi focada em fazermos um script onde que reproduzimos a ransonote, scriptzinho que para antes da decrypt, apenas executamos um step e exibimos como log o resultado.





* mov $len dword(eax) -> Foi Utilizado Para captarmos o tamanho da string





**Script:**



'''

bpc

bp 004014A5

run (paradp)

mov $len, dword(eax)

step

Log "String Decodificada: {ASCII;$len@esi}"



'''

