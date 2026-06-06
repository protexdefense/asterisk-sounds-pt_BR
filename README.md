# asterisk-sounds-pt_BR
Repositório contendo sons e prompts de voz para Asterisk e Issabel, destinados à criação de URAs, anúncios de atendimento, filas, gravações automáticas e personalização de centrais telefônicas IP.


# Instalar os Sons do Asterisk em Português do Brasil

Conecte ao servidor via SSH utilizando o usuário root.

Crie o diretório de idiomas do Asterisk:

```bash
mkdir -p /var/lib/asterisk/sounds/pt_BR
cd /var/lib/asterisk/sounds/pt_BR
```

Baixe os pacotes de sons em Português do Brasil:

```bash
wget https://github.com/protexdefense/asterisk-sounds-pt_BR/raw/main/asterisk-sounds-core-pt-BR-3.8.3.zip

wget https://github.com/protexdefense/asterisk-sounds-pt_BR/raw/main/asterisk-sounds-extra-pt-BR-1.11.10.zip
```

Extraia os arquivos:

```bash
unzip asterisk-sounds-core-pt-BR-3.8.3.zip

unzip asterisk-sounds-extra-pt-BR-1.11.10.zip
```

Ajuste as permissões:

```bash
chown -R asterisk:asterisk /var/lib/asterisk/sounds/pt_BR
chmod -R 755 /var/lib/asterisk/sounds/pt_BR
```

Recarregue o Asterisk:

```bash
asterisk -rx "core reload"
```

Para utilizar os sons em Português do Brasil, configure o idioma nos ramais ou no dialplan:

```asterisk
Set(CHANNEL(language)=pt_BR)
```

Verifique se os arquivos foram instalados corretamente:

```bash
ls -la /var/lib/asterisk/sounds/pt_BR
```

Após a instalação, os prompts poderão ser utilizados em URAs, filas de atendimento, conferências e demais recursos do Asterisk.
