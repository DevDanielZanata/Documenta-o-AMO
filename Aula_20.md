###### Na aula 20, foi mostrado como os malwares usam o **Runtime Linking.**





**Conseguimos observar a seguinte coisa:**



**GetProcAddress:**

* **"Recupera o endereço de memória de uma função ou variável exportada de uma DLL"**



**LoadLibrayA**

* **"Carrega uma biblioteca de vínculo dinâmico (DLL) para o espaço de memória do processo que a chama."** 



Assim vendo pelos registradores observamos o padrão de chamada dessa função. Conseguimos observar dentro de strings a chamdas dessas DLL's

