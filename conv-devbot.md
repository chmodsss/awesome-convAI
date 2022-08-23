# Conv-devbot

An attempt to develop conversational bots for assisting Software development process.
This work[WIP] is an integration of several technologies such as Speech recognition system (STT), Dialog systems (Chatbots), Speech synthesis (TTS).
The use-case in the project is to help developers search for solutions without leaving the development environment.

## Software tools

The study is experimented with an existing tool [Seahawk](http://seahawk.inf.usi.ch/index.html). Seahawk is an eclipse plugin, which helps to search for stackoverflow solutions in the IDE itself without having to leave the environment.

The study will evaluate the usage of Seahawk plugins vs a conversational bot which uses seahawk in the background. By effectively evaluation of the interfaces being used, one can estimate the potential of conversational interfaces in software development domain.

##### Seahawk installation
* Install Apache Solr
* Instantiate solr at localhost:8983
* Create a database so_db and let it running at port:3306 (follow seahawk installation page)
* Execute `java -jar xml_importer.jar -a localhost -c so\Comments.xml -d so_db -o 3306 -p so\Posts.xml -s root -t mysql -u so\Users.xml -w password`
* Execute `java -jar -Xmx1200m solr_importer.jar http://localhost:8983/solr gamedev so_db root password 127.0.0.1 3306 mysql`


## Automatic Speech recognition(ASR) system or Speech-to-text(STT)

Various ASR engines are available as open-source. Based on the underlying architecture, they are classified as Hidden Markov Models (HMM) and Deep learning models.

HMM ASR:
* [Cmusphinx](https://cmusphinx.github.io/)
* [Kaldi](https://kaldi-asr.org/)

DL ASR:
* [DeepSpeech](https://github.com/mozilla/DeepSpeech)
* [ESPnet](https://github.com/espnet/espnet)

Commercial ASR (Cloud based solutions):
* [Dragon Medical one](https://www.nuance.com/healthcare/provider-solutions/speech-recognition.html)
* [Azure Speech](https://azure.microsoft.com/en-us/services/cognitive-services/speech-to-text/)
* [Google STT](https://cloud.google.com/speech-to-text)
* [Aiva health](https://www.aivahealth.com/)
* [eCare](https://ecarenotes.com/)

##### For patients:
* [Care Angel](https://www.careangel.com/)
* [Lifepod](https://lifepod.com/)

## Speech synthesizer or Text-to-Speech(TTS)

TTS helps to synthesize audio-speech from text. Eventhough lots of previous TTS systems sound robotic, recent developments in TTS lead to human-like speeches.

* [wavenet](https://github.com/ibab/tensorflow-wavenet)
* [Tacotron](https://github.com/keithito/tacotron)
* [Deepvoice](https://github.com/r9y9/deepvoice3_pytorch)
* [voiceloop](https://research.fb.com/downloads/voiceloop/)

## Conversational agent (NLU)

* [Google Dialogflow](https://cloud.google.com/dialogflow)
* [Amazon Lex](https://aws.amazon.com/lex/)
* [IBM Watson](https://www.ibm.com/watson)
* [Wit](https://wit.ai/)
* [Microsoft LUIS](https://www.luis.ai/)
* [Rasa](https://rasa.com/)
* [Xenioo](https://www.xenioo.com/en/)

##### Language support:
Amazon lex is restricted to English language.

##### Automatic Speech recognition(ASR) support:
Rasa does not have ASR support directly, but connecting with an external ASR engine is possible.
