a aula 16 a gente pegou o shellcode que tinha sido identificado no script anterior, extraiu e injetou esse código em um processo pra começar a análise. O foco foi praticar a extração e os passos básicos de injeçã e observar.



* **Injetamos nosso payload alocando memória e copiando o binário dentro dela.**



Durante a análise também apareceram  chamadas como **CreateNamedPipeA e ConnectNamedPipe. A CreateNamedPipeA** é usada pra criar o pipe nomeado que o payload vai usar pra comunicação, e a **ConnectNamedPipe** bloqueia (não retorna) até um cliente se conectar. Esse comportamento é importante pra entender o fluxo: o payload pode ficar esperando pela conexão, então ao instrumentar ou testar a amostra é preciso conectar um cliente (ou simular um) pra destravar a execução e capturar as trocas.

