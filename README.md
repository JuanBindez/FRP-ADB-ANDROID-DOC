# Factory Reset Protetion


# Recuperação FRP conta Google

## INSTALANDO O ESSENCIAL

    sudo apt install android-tools-adb
    
----------

## DESBLOQUEANDO A VALIDAÇÃO

- Você precisará desligar o aparelho e logo em seguida, apertar ao mesmo tempo os botões de LIGAR e VOLUME - e aguardar uns 4 a 6 segundos, soltar e ele entrará em modo Fastboot.

- Com o modo Fastboot ativado, deve ir até a opção BP TOOLS (utilizando o volume -) e selecionar com o VOLUME +, o aparelho reiniciará.

- Após reiniciar o aparelho, basta conectar um cabo USB no aparelho e em seu computador e em seguida, digitar ou colar o seguinte código no terminal:


      sudo adb devices
    
- Seu aparelho deverá aparecer na lista. Enquanto na tela do mesmo deverá aparecer uma solicitação para autorizar a depuração USB, selecione o campo de opção e aperte OK.

## Com a depuração bloqueada, agora utilize o seguinte código em seu terminal:

    sudo adb shell content insert --uri content://settings/secure --bind name:s:user_setup_complete --bind value:s:1
    
- Este código liberará seu dispositivo da validação de conta requisitada.
- Obs.: Caso não consiga a autorização, reinicie o serviço de depuração com o código: adb kill-server.

https://www.madrutech.com.br/2017/06/desbloquear-conta-google-no-moto-pelo-linux.html
