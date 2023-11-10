<h1 align="center"> Sprint 3 (EDGE) - SERVIDOR IOT </h1>

<h3>Integrantes do grupo: </h3>

<ul> 
  <li> RM550233 - Fellype Dos Santos Laes </li>
  <li> RM550539 - Guilherme Fazito </li>
  <li> RM551528 - Henrique Lima </li>
  <li> RM98860  - Ian Xavier Kuraoka </li>
  <li> RM98287  - Raí Gumieri dos Santos </li>
</ul>

<h3> Link do vídeo: https://www.youtube.com/watch?v=3pDbBIOw4xU </h3>

<br>

<h2 align="center"> Introdução </h2>
<p align="justify"> O IoT (Internet das Coisas) vem se tornando cada vez mais importante na sociedade, por conta de seus resultados impressionantes na transformação de objetos do dia a dia em entidades conectadas e inteligentes. À medida que a tecnologia evolui, ela abre um mundo de possibilidades, desde a automação residencial até aplicações industriais avançadas. </p>

<p align="justify"> À medida que o IoT continua a moldar o nosso mundo, a chave para desbloquear todo o potencial desses dispositivos conectados muitas vezes reside na capacidade de criar um servidor robusto e confiável. Esses servidores desempenham um papel central na coleta, processamento e distribuição eficiente dos dados gerados por dispositivos IoT. Ao criar um servidor adaptado às necessidades específicas de seus dispositivos, você pode habilitar a comunicação contínua, a segurança dos dados e a análise inteligente, permitindo que sua rede de IoT funcione de maneira suave e eficaz. </p>

<p align="justify"> Diante disso, neste README, vamos entender o processo que deve ser feito para criar um servidor, utilizando uma Máquina Virtual <b> VMWARE WORKSTATION </b> como plataforma base. Além disso, utilizaremos a ferramenta <b> POSTMAN </b> para testar e validar o funcionamento desse servidor </p>

<div align="center"> 
  <img src="https://github.com/raigumieri/Sprint4_EDGE/assets/127215645/af2c8fa9-dfb7-4079-a8f9-01b60ea653e1" width=350px> 
</div>

<br>

<h2 align="center"> Instalações necessárias </h2>
<p align="justify"> Antes de começar o processo de criação de um servidor, é necessário instalar alguns itens que fazem parte deste processo, que seriam: </p>

<ul> 
  <li> Virtual Machine (VMware Workstation): https://www.vmware.com/br/products/workstation-player/workstation-player-evaluation.html </li>
  <li> Ubuntu Desktop 22.04.3 LTS: https://ubuntu.com/download/desktop </li>
  <li> Postman: https://www.postman.com/downloads/ </li>
  <li> Collection de comandos Postman (Fiware descomplicado): https://github.com/fabiocabrini/fiware/blob/main/FIWARE.postman_collection.json </li>
</ul>

<p align="center"> Vale ressaltar que este arquivo da Collection deve ser importada na plataforma Postman, para fazer os devidos testes do servidor. </p>

<br> 

<h3> Requisitos de Hardware: </h3>
<p> Memória RAM: 4GB </p>
<p> Armazenamento (HD/SSD): 20GB </p>

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
  <p> 6. Depois de alguns procedimentos, a Máquina Virtual já está pronta! </p>
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
<p> Agora que o servidor já está pronto, precisamos fazer alguns testes com ele para descobrir se está realmente funcionando, vamos utilizar o Postman para fazer os testes. </p>

<ol> 
  <li> Abra o Postman e importe o arquivo.json </li>
  <li> Abra a pasta "FIWARE" </li>
  <li> Abra a pasta "IOT Agent MQTT" </li>
  <li> Clique em "Health Check" </li>
  <li> Coloque o IP da Máquina Virtual no lugar da url </li>
  <img src="https://github.com/raigumieri/Sprint4_EDGE/assets/127215645/9a0f10b5-ea72-4345-ad3d-b52ff5c4790b"> 
  <li> Depois clique em "Send" </li>
  <img src="https://github.com/raigumieri/Sprint4_EDGE/assets/127215645/8a30a4fc-d4c3-497e-bb6a-b29da045af18">
</ol>

<p> Esse processo deve ser feito nos 3 componentes: IOT Agent MQTT, Orion Context Broker, STH-Comet. Eles fazem parte do back-end do projeto, cada um possuindo suas funções: </p>

<h3> IOT Agent MQTT </h3>
<p align="justify"> O IoT-Agent MQTT atua como uma ponte de comunicação entre dispositivos IoT e um servidor MQTT. Ele facilita a coleta e a transmissão de dados de dispositivos IoT para o servidor MQTT, permitindo a troca eficiente de informações em tempo real entre os dispositivos e a plataforma IoT. </p>

<h3> Orion Context Broker </h3>
<p align="justify"> O Orion Context Broker é um componente-chave em arquiteturas de IoT. Sua função principal é gerenciar e armazenar informações contextualmente relevantes de dispositivos e objetos conectados. Ele permite que sistemas IoT coletem, processem e forneçam dados em tempo real sobre o estado e as condições desses dispositivos. Ele opera com base no modelo de Contexto, que significa que ele mantém informações atualizadas sobre o contexto dos objetos IoT, como localização, status, temperatura, e outros dados relevantes. Quando os dispositivos enviam informações para o Orion Context Broker, ele as armazena e disponibiliza para aplicativos e serviços que podem consultar e usar esses dados em tempo real. </p>

<h3> STH-Comet </h3>
<p align="justify"> A função do STH-Comet é lidar com o armazenamento e recuperação eficientes de séries temporais de dados históricos gerados por dispositivos IoT. Isso significa que ele é responsável por coletar, armazenar e permitir o acesso a informações temporais, como dados de sensores que se acumulam ao longo do tempo. Ele trabalha em conjunto com o Orion Context Broker, que lida com dados em tempo real, para fornecer uma solução completa para a gestão de informações em sistemas IoT. Enquanto o Orion gerencia os dados em tempo real e em contexto, o STH-Comet é responsável por manter um registro histórico desses dados, permitindo a análise retrospectiva, a geração de relatórios e a pesquisa de séries temporais. </p>

<div align="center">
  <h3> Arquitetura Back-End </h3>
  <img src="https://github.com/raigumieri/Sprint4_EDGE/assets/127215645/edf32d78-be40-45a1-b787-bddb4c822250">
</div>

<hr>
<br>

<h1 align="center"> Sprint 4 - Detector de Enchentes (AquaAlert) </h1>

<br>

<h2  align="center"> Introdução </h2>
<p align="justify"> Após a conclusão do Sprint 3, avançaremos para a etapa de elaboração do projeto AquaAlert. Este projeto consiste em um detector de risco de enchentes, projetado para alertar a população sobre a probabilidade de enchentes em uma determinada região. Para implementar este projeto, serão necessárias as seguintes peças: </p>

<ul> 
  <li> Placa de ensaio; </li> 
  <li> ESP32; </li>
  <li> DHT11 ou DHT22; </li>
  <li> Display LCD I2C; </li>
  <li> Resistor de 10kΩ. </li>
</ul>

<p align="justify"> Se você não tiver as peças físicas à disposição, existe a opção de montar o projeto no site Wokwi. Vamos seguir o procedimento online, mas sinta-se à vontade para realizar a montagem presencialmente, caso prefira. </p>
<h3> Link do site: https://wokwi.com/ </h3>

<p align="center"> Montando o projeto com essas peças, é possível chegar nesse resultado: </p>
<img src="https://github.com/raigumieri/Sprint3_EDGE/assets/127215645/6a152561-8539-43f1-b5e4-0d505cc2a248">

<br>

<h2 align="center"> Análise dos Componentes </h2>
<p align="justify"> Iniciaremos a explicação com a Placa de Ensaio, peça fundamental neste projeto. É nela que acomodaremos os demais componentes, assegurando o correto funcionamento do projeto. </p>
<p align="justify"> O ESP32 desempenha um papel crucial neste projeto ao estabelecer a conexão com a internet, possibilitando a visualização dos valores coletados pelos sensores na nuvem. Além disso, é responsável por coordenar o funcionamento do sensor de umidade e temperatura DHT22 (ou DHT11), bem como do Display LCD I2C. Por meio do ESP32, os dados coletados tornam-se acessíveis através da nuvem. Isso significa que, contanto que haja conexão com a internet, é possível acessar o projeto de qualquer região do mundo. </p>
<p align="justify"> Quanto ao sensor, o DHT22 é empregado para medir tanto a temperatura quanto a umidade. No entanto, no projeto físico, há também a opção do DHT11, que realiza as mesmas medições. Em resumo, independentemente da escolha entre DHT22 e DHT11, ambos proporcionarão resultados idênticos. </p>
<p align="justify"> O Display LCD I2C desempenha um papel crucial na transmissão de informações para o usuário. Através dele, é possível analisar o nível de umidade (em %), a temperatura e receber um alerta de enchente caso os valores atinjam níveis elevados. Sua interface intuitiva proporciona uma experiência de usuário eficaz na monitorização dos dados coletados. </p>

<br>

<h2 align="center"> Montagem do Código </h2>
<p> Após a conclusão da montagem do projeto, partiremos para o desenvolvimento do código. Sinta-se à vontade para acessar o código disponível neste repositório. No entanto, observe que será necessário efetuar algumas alterações nos tópicos marcados no código para estabelecer a conexão com a nuvem e visualizar os dados fornecidos pelo sensor DHT22. (Linhas 9, 10, 11, 12 e 13) </p>

<div align="center">
  <img src="https://github.com/raigumieri/Sprint3_EDGE/assets/127215645/3915fb3c-ed1f-42b6-9108-b79fdefaa670">
</div>

<br>

<p align="justify"> Após realizar a alteração mencionada, é necessário configurar as linhas de conexão com a internet. Para isso, siga as instruções no código e insira o nome e a senha da sua rede Wi-Fi nas posições indicadas. Isso possibilitará que o ESP32 se conecte à rede e envie os dados do sensor para a nuvem. (Linhas 16 e 17) </p>

<div align="center">
  <img src="https://github.com/raigumieri/Sprint3_EDGE/assets/127215645/3b954812-f646-4271-ad97-8d7bb09cd7ad">
</div>

<br>

<p align="justify"> Neste caso estamos usando o nome da rede “Wokwi-GUEST”, porque o site está fornecendo essa rede para ser feito os testes necessários, garantindo o funcionamento do ESP32 ao enviar os dados na nuvem. Após realizar essas modificações, execute o código e aguarde a mensagem indicando que o ESP32 está tentando se conectar à rede. Isso confirma que as configurações foram feitas corretamente e o dispositivo está buscando ativamente a conexão com a rede especificada. </p>

<div align="center">
  <img src="https://github.com/raigumieri/Sprint3_EDGE/assets/127215645/3b1c6151-8b80-4205-9149-63f7a7e9b3be">
</div>

<br>

<p align="justify"> Se você estiver realizando o procedimento com o material em mãos, lembre-se de pressionar o botão "BOOT" do ESP32 para estabelecer a conexão. Isso é necessário para iniciar o processo de conexão com a rede após as modificações no código. </p>

<div align="center">
  <img src="https://github.com/raigumieri/Sprint3_EDGE/assets/127215645/61e46b3e-1612-4cc8-9ccd-6da7be441294">
</div>

<br>

<p align="center"> Após a conexão ser feita, vai aparecer a seguinte informação: </p>

<div align="center">
  <img src="https://github.com/raigumieri/Sprint3_EDGE/assets/127215645/aa4f816f-e963-405c-a923-18681dcf2265">
</div>

<br>

<p align="justify"> Após esse procedimento, os valores de temperatura e umidade serão adquiridos pelo sensor DHT22 e serão exibidos tanto no Monitor Serial quanto no Display LCD I2C: </p>

<div align="center">
  <img src="https://github.com/raigumieri/Sprint3_EDGE/assets/127215645/2c742afb-ad54-4e2c-9d7b-dca568c88a82">
</div>

<br>

<div align="center">
  <img src="https://github.com/raigumieri/Sprint3_EDGE/assets/127215645/3c42cb94-3b94-46e0-a161-84b9d4e0aca6">
</div>

<br>

<h2 align="center"> Acessando os Dados na Rede </h2>
<p align="justify"> Agora que o projeto está pronto e operacional, é crucial testar se os valores estão sendo enviados pela rede. Para isso, acesse o Google Colab e utilize o código disponibilizado neste repositório, especificamente o Paho MQTT. Essa ferramenta é fundamental para estabelecer a comunicação direta com o broker. </p>
<p> Primeiro faça a instalação do Paho MQTT </p>

<div align="center">
  <img src="https://github.com/raigumieri/Sprint3_EDGE/assets/127215645/a299202b-d004-42aa-9f11-8dfc7e0e7bb9">
</div>

<br>

<p> Em seguida, realize as modificações nos tópicos conforme as instruções no código do projeto. Certifique-se de ajustá-los de acordo com as especificações fornecidas e, posteriormente, execute o código no Google Colab para garantir o correto envio e recebimento dos valores na rede. </p>

<div align="center">
  <img src="https://github.com/raigumieri/Sprint3_EDGE/assets/127215645/4a345aa9-3a87-40b1-a0dd-3ebd7d28720b">
</div>

<br>

<p> Após executar o código, os valores de temperatura e umidade serão exibidos, semelhantemente ao que é mostrado no Monitor Serial e no Display LCD I2C. </p>

<div align="center">
  <img src="https://github.com/raigumieri/Sprint3_EDGE/assets/127215645/3dfa4131-2684-4d8c-8e41-d1dee3dea62a">
</div>

<h2 align="center"> Considerações Finais 📘 </h2>
<p align="center"> Diante de todos esses passos, podemos afirmar que o projeto está concluído. Se todos os procedimentos foram seguidos corretamente, será possível verificar que o projeto está funcionando conforme o esperado. Agradecemos pela atenção e pelo esforço ao acompanhar essas etapas! </p>
