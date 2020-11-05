# Plugin-Arduino
<p align='justify'>O plugin possibilita a comunicação entre o <a target='_new' href='http://lite.acad.univali.br/portugol/'>Portugol Studio</a> e o Arduino através do protocolo Firmata. É necessário que o ambiente de desenvolvimento do Arduino, disponível em <a target='_new' href='https://www.arduino.cc/en/software'>https://www.arduino.cc/en/software</a>, esteja instalado no computador e o programa <b>StandardFirmata</b> carregado no Arduino.<br>&nbsp;</p>
<h2>Exemplos</h2>
<p align='justify'><b>Saída Digital</b><br>O programa irá ligar e desligar o LED conectado ao pino 13 do Arduino por 10 vezes.</p>

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
<a target='_new' href='https://github.com/kurbatov/firmata4j'>https://github.com/kurbatov/firmata4j</a></li>
<li><b>Official jSSC (Java Simple Serial Connector)</b><br>
<a target='_new' href='https://github.com/scream3r/java-simple-serial-connector'>https://github.com/scream3r/java-simple-serial-connector</a></li>
<li><b>Simple Logging Facade for Java (SLF4J)</b><br>
<a target='_new' href='http://www.slf4j.org/'>http://www.slf4j.org/</a></li>
</ul>
