<h1 align="center"> Sprint 4 (EDGE) - SERVIDOR IOT </h1>

<h3>Integrantes do grupo: </h3>

<ul> 
  <li> RM550233 - Fellype Dos Santos Laes </li>
  <li> RM550539 - Guilherme Fazito </li>
  <li> RM551528 - Henrique Lima </li>
  <li> RM98860  - Ian Xavier Kuraoka </li>
  <li> RM98287  - Raí Gumieri dos Santos </li>
</ul>

<h3> Link do vídeo: </h3>

<br>

<h2 align="center"> Introdução </h2>
<p> O IoT (Internet das Coisas) vem se tornando cada vez mais importante na sociedade, por conta de seus resultados impressionantes na transformação de objetos do dia a dia em entidades conectadas e inteligentes. À medida que a tecnologia evolui, ela abre um mundo de possibilidades, desde a automação residencial até aplicações industriais avançadas. </p>

<p> À medida que o IoT continua a moldar o nosso mundo, a chave para desbloquear todo o potencial desses dispositivos conectados muitas vezes reside na capacidade de criar um servidor robusto e confiável. Esses servidores desempenham um papel central na coleta, processamento e distribuição eficiente dos dados gerados por dispositivos IoT. Ao criar um servidor adaptado às necessidades específicas de seus dispositivos, você pode habilitar a comunicação contínua, a segurança dos dados e a análise inteligente, permitindo que sua rede de IoT funcione de maneira suave e eficaz. </p>

<p> Diante disso, neste README, vamos entender o processo que deve ser feito para criar um servidor, utilizando uma Máquina Virtual <b> VMWARE WORKSTATION </b> como plataforma base. Além disso, utilizaremos a ferramenta <b> POSTMAN </b> para testar e validar o funcionamento desse servidor </p>

<div align="center"> 
  <img src="https://github.com/raigumieri/Sprint4_EDGE/assets/127215645/af2c8fa9-dfb7-4079-a8f9-01b60ea653e1" width=350px> 
</div>

<br>

<h2 align="center"> Instalações necessárias </h2>
<p> Antes de começar o processo de criação de um servidor, é necessário instalar alguns itens que fazem parte deste processo, que seriam: </p>

<ul> 
  <li> Virtual Machine (VMware Workstation): https://www.vmware.com/br/products/workstation-player/workstation-player-evaluation.html </li>
  <li> Ubuntu Desktop 22.04.3 LTS: https://ubuntu.com/download/desktop </li>
  <li> Postman: https://www.postman.com/downloads/ </li>
  <li> Collection de comandos Postman (Fiware descomplicado): https://github.com/fabiocabrini/fiware/blob/main/FIWARE.postman_collection.json </li>
</ul>

<p align="center"> Vale ressaltar que este arquivo da Collection deve ser importada na plataforma Postman, para fazer os devidos testes do servidor. </p>

<br>

<h2 align="center"> Instruções de criação da Máquina Virtual </h2>
<h3 align="center"> Após as instalações serem feitas, vamos seguir o passo a passo para a criação da Máquina Virtual: </h3>

<br>

<div align="center"> 
  <p> 1. Acesse o VMware Workstation; </p>
  <p> 2. Crie uma nova máquina virtual; </p>
  <img src="https://github.com/raigumieri/Sprint4_EDGE/assets/127215645/9906f7e9-70b6-4408-b353-bd6df1e584f8">
  
  <p> 3. Clique em "Browse..." e selecione o arquivo Ubuntu; </p>
  <img src="https://github.com/raigumieri/Sprint4_EDGE/assets/127215645/58446223-731c-4c0c-b5eb-e5b59f5d4478" width=400px>

  <p> 4. Faça um registro simples; </p>
  <img src="https://github.com/raigumieri/Sprint4_EDGE/assets/127215645/ea240bb5-995d-4266-8291-f4fcec517831" width=400px>
  
  <p> 5. Clique na opção "Next" até finalizar o processo; </p>
  <p> 6. Depois de alguns procedimentos, a máquina virtual já está pronta! </p>
  <img src="https://github.com/raigumieri/Sprint4_EDGE/assets/127215645/a3e95513-e7f9-42a7-9bb1-16f646a2a50f" width=900px>
</div>

<br>

<h2 align="center"> Criação do Servidor </h2>
<p align="center"> Agora que já está tudo pronto, vamos avançar para os comandos necessários para criar o servidor. Primeiro, acesse sua máquina virtual e faça a seguinte combinação: <b> CTRL + ALT + T </b> </p>
<p> Isso vai dar acesso ao cmd da Máquina Virtual. Após esse passo, siga essas instruções: </p>

<ul> 
  <li> Instalar o "ifconfig" para identificar o IP da máquina virtual: <b> sudo apt-get install net-tools </b> </li>
  <li> Comando para ler o IP da Máquina Virtual: <b> ifconfig </b> </li>
  <li> Fazer a instalação do git: <b> sudo apt install git </b> </li>
  <li> Link para instalação do Docker: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04-pt </li>
  <li> Copiar os arquivos do repositório Fiware Descomplicado: <b> git clone https://github.com/fabiocabrini/fiware </b> </li>
  <li> Entrar na pasta do Fiware: <b> cd fiware </b> </li>
  <li> Rodar os containers: <b> sudo docker compose up -d </b> </li>
  <li> status dos containers: <b> sudo docker stats </b> </li>
</ul>

<h3> Após esses passos, vai aparecer essas informações: </h3>
<img src="https://github.com/raigumieri/Sprint4_EDGE/assets/127215645/ff10668e-4084-4de6-9d4c-6e87e73b687f">

<h2 align="center"> Realizando Testes </h2>
<p> Agora que o servidor já está pronto, precisamos fazer alguns testes com ele com o intuito de descobrir se está realmente funcionando, vamos utilizar o Postman para fazer os testes. </p>







