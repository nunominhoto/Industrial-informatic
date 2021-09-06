Projeto MES plc Fábrica do grupo A3_ES_B

Conteúdo:

1.Pasta MES
->Aplicacao.exe - MES do nosso projeto, ao abrir terá que indicar o device name do plc onde corre o servidor opc.
Se o plc/codesys correr no próprio pc, basta escrever "localhost", senão terá que escrever o device name do plc onde corre o servidor opc. 
Este device name encontra-se ao ter o codesys aberto ir à secção onde diz "Device (CODESYS Control Win V3 x64)" e escrever o Device Name que aparece.
A base dados do programa é local, e quando abre a aplicação, se não estiver criada, cria-a automaticamente na pasta onde corre o exe.
->ConsolaFabrica.exe - Permite fazer reset da base dados para quando quiser recomeçar o plc/chão de fábrica.
Permite ao utilizador monitorizar a estatística e ordens presentes na base dados, mesmo com o programa a correr.

2.Pasta codesys
->PRAT1_alt1.project - Ficheiro codesys, basta abrir e usar. Usa o device CODESYS Control Win V3 x64.

A nossa BD (SQLite Java), como referido, é local. Irá guardar as ordens e estatística decorrida até ao momento, sendo 
que se for abaixo o MES, quando se volta a ligar ele irá ter a informação que tinha quando se desligou, e retoma processo.
O ConsolaFabrica.exe permite observar as ordens e estatística guardadas na base dados, sendo o nosso programa interface para monitorização dos acontecimentos na fábrica.
Ambiente execução é Windows, o MES foi escrito em Java, compilado para Jar no eclipse e transformado em formato exe para Windows utilizando a ferramenta launch4j (http://launch4j.sourceforge.net/)
Antes ligar o MES, é preciso ter já o PLC ligado.
Antes de enviar ordens/continuar ordens guardadas, é necessário ter o chão fábrica ligado, se ligar o chão fábrica depois de o MES já ter recebido ordens irá processar mal as ordens e peças.
