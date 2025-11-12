Aula 4 pegamos o ransomware NEFILIM era desmontando ele no debugger, indo instruçao por instruçao pra ver como a ransomnote é desencriptada.



Foi preciso ver onde o codigo e as libs caem na memoria. Colocar breakpoints em chamadas criticas pra interceptar o fluxo e checar os parametros, e quando precisava prender a execucao sem mexer no binario era usado breakpoints de hardware. Foi mostrado onde as funcoes da wincrypt.h entram em cena e como a logica basica de criptografia do malware funciona. 



Resumindo: nao so ver o que o NEFILIM faz, mas aprender as tecnicas pra desmontar e entender o que ta rolando.



Portanto conseguimos retirar as seguintes informações 





'''



**DIE**


Microsoft Visual C/C++(2010) \[libcmt]

Microsoft Linker (10.0) \[EXE32, signed]

Entropy: 6.46499 (not packed)



Hash do ransoware:

* D4492A9EB36F87A9B3156B59052EBAF10E264D5D1CE4C015A6B0D205614E58E3



**Funções Identificadas:**



* CryptAcquireContext -> Ela é usada para adquirir um identificador (handle)
* CryptCreateHash -> é usada para iniciar o processo de hashing de um fluxo de dados. Ela cria e retorna um identificador para um objeto de hash
* CryptHashData -> é usada para adicionar dados ao objeto de hash especificado;  **A função calcula o valor de hash dos dados fornecidos e os acumula no objeto de hash existente, até que todos os dados tenham sido adicionados**





**Vai fazer o Shal da String:**

*'ya chubstvuu bol' gde-to v grude, i moi rani v serdce ne zalechit'* 66 bytes/0x42

**Esse Shal serve como base para derivar uma chave RC4**







A chave rc4 eh usada para disencriptar os dados da stringona (encodada em base64)

chave = derivação(sha1(string\_ya))

###### **ransomnote = rc4\_decrypt(base64\_decode(stringona), chave)**





'''

