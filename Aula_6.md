###### Basicamente na aula 6, continuamos analisando a criptografia do arquivo.



Descobrimos que ele encripta cada arquivo com uma chave diferente, **além de adicionar tal chave encriptada no final do arquivo**





###### Assim nossa sequencia fica:



--------------------------------------------------------------------------------------------------



Vai fazer o Shal da String:

'ya chubstvuu bol' gde-to v grude, i moi rani v serdce ne zalechit' 66 bytes/0x42

Esse Shal serve como base para derivar uma chave RC4



A chave rc4 eh usada para disencriptar os dados da stringona (encodada em base64)

chave = derivação(sha1(string\_ya))

ransomnote = rc4\_decrypt(base64\_decode(stringona), chave)



a = rsa\_enc(gen128bits\_a)

b = rsa\_enc(gen128bits\_b)



write(arq, a) -> ***Escreve no Fim do Arquivo***



//chave 128bits gerada em runtime para cada arquivo

//coloca no fim porem e encriptada em a chave publica RSA-2048



-------------------------------------------------------------------------------------------------







