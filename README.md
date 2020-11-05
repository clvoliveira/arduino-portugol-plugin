# arduino-portugol-plugin
<p align='justify'>O plugin possibilita a comunicação entre o <a href='http://lite.acad.univali.br/portugol/'>Portugol Studio</a> e o Arduino através do protocolo Firmata. É necessário que o ambiente de desenvolvimento do Arduino, disponível em <a href='https://www.arduino.cc/en/software'>https://www.arduino.cc/en/software</a>, esteja instalado no computador e o programa <b>StandardFirmata</b> carregado no Arduino.<br>&nbsp;</p>
<p align='justify'>Exemplo de uso - <b>Saída Digital</b>: </p>

    programa {
        inclua biblioteca Arduino --> arduino
        inclua biblioteca Util --> util
	
        funcao inicio() {
            arduino.conectar("COM3")
            para (inteiro i = 0; i < 10; i++) {
                arduino.escreverDigital(13, 1)
                util.aguarde(250)
                arduino.escreverDigital(13, 0)
                util.aguarde(250)
            }
            arduino.desconectar()
        }
    }

<p align='justify'>Este plugin utiliza as seguintes bibliotecas de terceiros:</p>
<ul>
<li><b>firmata4j</b><br>
https://github.com/kurbatov/firmata4j</li>
<li><b>Official jSSC (Java Simple Serial Connector)</b><br>
https://github.com/scream3r/java-simple-serial-connector</li>
<li><b>Simple Logging Facade for Java (SLF4J)</b><br>
http://www.slf4j.org/</li></ul>
