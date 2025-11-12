Nesta aula a gente criou um desofuscador em VBScript usando as rotinas de desofuscação adaptadas na aula passda portamos ajustamos as funcoes pra VBScript, resultado foi um script que automatiza a decodificacao dos itens ofuscados.





###### **Script:**



'''



posInicial-1

Do While (posInicial > 0)

&nbsp;	"InStr(\[start, string1, string2\[,compare])

&nbsp;	posInicial InStr(1, contents, "ThisDocument.bQYHDG(""")



&nbsp;	If posInicial Then Exit Do

&nbsp;	posFinal InStr(posInicial, contents, """, 15)")

&nbsp;	"WScript.Echo(posInicial)

&nbsp;	"WScript.Echo(posFinal)



&nbsp;	strofuscada Mid(contents, posInicial 21, posFinal posInicial21)

&nbsp;	strDesofuscada desofusca (strofuscada, 15)



&nbsp;	contents Replace(contents, "ThisDocument.bQYHDG(""" \& strofuscada \& """, 15)", """" \& strDesofuscada \& """")

Loop

&nbsp;	WScript.Echo contentes



'''

