*Leia em outros idiomas: [日本語](README-ja.md).*

> **ISENÇÃO DE RESPONSABILIDADE**: Este aplicativo é usado apenas para fins demonstrativos e ilustrativos e não constitui uma oferta que passou por revisão regulatória. Não se destina a servir como uma aplicação médica. Não há precisão da saída deste aplicativo que possa ser apresentada como garantia.

**__Nível de habilidade__**: Intermediário
**__N.B__**: Todos os serviços utilizados nesta solução utilizam o plano Lite. 

# Pulsação - Um aplicativo de saúde móvel do IoT Waton Machine Learning

A idéia por trás deste aplicativo é ter uma maneira de verificar as taxas de pulso com os dispositivos mais disponíveis, os telefones celulares. Aqui está uma breve descrição do padrão de código:

* Crie um modelo de classificação usando um conjunto de dados que contém os dados de pulso e seus valores derivados relacionados. Implemente o modelo e exponha-o como pontos finais do Watson Machine Learning
* Registre o dispositivo móvel com o Watson IoT Platform
* Usar o aplicativo móvel, gerar os dados de pulso online. Esses dados serão publicados na plataforma IoT e, em seguida, armazenados em um banco de dados NoSQL
* Transmitir os dados de batimentos do aplicativo em tempo real (ou do banco de dados) usando o Watson Machine Learning validando o modelo desenvolvido


![](public/img/arch-diagram-health-model-1.png)

## Passos

* Passos 1 & 5 - [Aplicação Node.js](https://github.com/hovig/pulse-iot-wml-mobile-health/blob/master/NodejsApplication.md)
* Passo 2 - [Watson Machine Learning](https://github.com/hovig/pulse-iot-wml-mobile-health/blob/master/WatsonMachineLearning.md)
* Passo 3 - [Watson IoT Platform](https://github.com/hovig/pulse-iot-wml-mobile-health/blob/master/WatsonIoTPlatform.md)
* Passo 4 - [IBM Studios](https://github.com/hovig/pulse-iot-wml-mobile-health/blob/master/IBMStudios.md)

## Amostra de saída

* Depois de seguir os passos acima, experimente no navegador do seu celular: `http://<YOUR_APP_NAME>.mybluemix.net`

  Você pode experimentar o aplicativo de demonstração em [http://mypulse.mybluemix.net/](http://mypulse.mybluemix.net/) para ter uma ideia de como funciona. Observe que, se o serviço de aprendizado de máquina estiver acima da cota, ele mostrará `undefined` para alguns campos.

![](public/img/plan.png)

* Abrir [Watson IoT Platform Quickstart](https://quickstart.internetofthings.ibmcloud.com/#/)
* Coloque o ID do seu dispositivo lá para exibição de streaming em tempo real de seus dados.

![](public/img/qs.png)

![](public/img/mypulse.gif)

## Links

* [IBM Cloud](https://bluemix.net/)  
* [IBM Cloud Documentation](https://www.ng.bluemix.net/docs/)  
* [IBM Cloud Developers Community](http://developer.ibm.com/bluemix)  
* [IBM Watson Internet of Things](http://www.ibm.com/internet-of-things/)  
* [IBM Watson IoT Platform](http://www.ibm.com/internet-of-things/iot-solutions/watson-iot-platform/)   
* [IBM Watson IoT Platform Developers Community](https://developer.ibm.com/iotplatform/)
* [Savitzky–Golay filtro para suavizar os dados do acelerômetro](https://en.wikipedia.org/wiki/Savitzky%E2%80%93Golay_filter)
* Obrigado a Mark Watson por fazer a biblioteca "[watson-ml-model-utils](https://www.npmjs.com/package/watson-ml-model-utils)"
* [Opcional: pesquisa de caso de uso adicional](https://developer.ibm.com/in/2017/05/31/watson-iot-platform-based-heart-emotion-analysis-using-lyfas-device-apache-spark/)

## Licença
[Apache 2.0](LICENSE)
