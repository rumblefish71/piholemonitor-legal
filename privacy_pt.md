# Política de Privacidade do PiHoleMonitor

Última atualização: 16 de abril de 2026

## 1. Informações Gerais
Esta política de privacidade informa sobre a natureza, o âmbito e a finalidade da recolha e utilização de dados pessoais ao utilizar a aplicação "PiHoleMonitor".

Responsável:
Christian Jurtz
Haubachstr. 48
16540 Hohen Neuendorf
Alemanha
mountainfields@jurtz.de

## 2. Princípio Básico
A aplicação foi concebida para monitorizar a sua **própria** instância Pi-hole®.
**Não temos acesso aos seus dados do Pi-hole.**
A comunicação ocorre exclusiva e diretamente entre o seu dispositivo (smartphone) e o seu servidor Pi-hole. As suas credenciais (tokens API, palavras-passe) são armazenadas de forma encriptada no seu dispositivo e não saem dele.

## 3. Permissões e Processamento de Dados

### 3.1 Acesso à Rede (INTERNET)
A aplicação requer acesso à rede para se ligar ao seu servidor Pi-hole configurado.
* **Dados:** Endereço IP, nomes de host, token API.
* **Processamento:** Os dados são processados exclusivamente de forma local e não são enviados para nós ou para terceiros.
* **Base Legal:** Interesse legítimo (Art. 6 par. 1 lit. f RGPD) na funcionalidade da aplicação.

### 3.2 Bloqueio da App e Biometria (USE_BIOMETRIC)
Pode, opcionalmente, proteger o acesso à aplicação. Isto utiliza os métodos de segurança configurados no seu dispositivo (ex: impressão digital, reconhecimento facial seguro ou PIN/padrão).
* **Processamento:** A verificação é realizada exclusivamente de forma local pelo sistema operativo Android (Android Biometric API).
* **Privacidade de Dados:** A aplicação nunca tem acesso aos seus dados biométricos em bruto (como imagens de impressões digitais) ou ao seu PIN. Apenas recebemos uma confirmação ("Sucesso" ou "Erro") do sistema. Os dados biométricos nunca saem do armazenamento de hardware seguro do seu dispositivo (Art. 9 RGPD).

### 3.3 Relatório de Erros (Crash Reporting)
Para melhorar a estabilidade da aplicação, pode optar por enviar um relatório em caso de falha.
* **Tipo:** Opt-In (Desativado por defeito). Deve consentir explicitamente nas definições ("Crash Reporting Consent").
* **Destinatário:** Os dados são enviados para o nosso próprio servidor (`https://www.mountainfields.de/crash`). **Sem** partilha com terceiros.
* **Dados Recolhidos:**
    * Tipo de dispositivo, modelo, fabricante, versão Android.
    * Uso de memória (RAM) no momento da falha.
    * Relatório técnico do erro (Stacktrace).
    * Extrato do log do sistema (Logcat, máx. 200 linhas).
* **Retenção:** Os relatórios são armazenados no nosso servidor por até 30 dias para análise e depois eliminados. No dispositivo, são eliminados imediatamente após a transmissão.
* **Base Legal:** O seu consentimento (Art. 6 par. 1 lit. a RGPD). Pode revogá-lo a qualquer momento.

### 3.4 Depuração Avançada (Session Recording)
Pode iniciar manualmente uma gravação de erros detalhada ("Session Recording").
* **Tipo:** Manual (Opt-In).
* **Processamento:** O ficheiro (`debug_reports`) é gerado **exclusivamente de forma local**. **Não existe upload automático.** O utilizador decide se partilha este ficheiro.
* **Retenção:**
    * Os **dados em bruto** são **eliminados imediatamente** após a geração do relatório.
    * O relatório gerado é **temporariamente armazenado para exportação** e é **automaticamente eliminado após, no máximo, 1 hora**.
* **Conteúdo do Relatório:**
    * Versão da app, tipo de build, hash Git.
    * Informações de rede (status WiFi/Dados/VPN).
    * **Dados Mascarados:** Domínio Pi-hole, **endereços IP ofuscados** (ex: `192.168.xxx.xxx`), endereços MAC e IDs de Sessão (SID).
    * Status do certificado SSL.
    * Log de atividades da app durante a sessão.
* **Nota:** Apesar do mascaramento, este relatório pode conter **metadados técnicos**. **Partilhe apenas com pessoas de confiança.**

## 4. Armazenamento de Dados Sensíveis
Os tokens API e palavras-passe são armazenados no **Android Keystore System** e em `SharedPreferences` (encriptados com AES-256 GCM).

## 5. Os Seus Direitos
Tem o direito ao acesso, retificação, apagamento, limitação do tratamento e portabilidade dos dados (Art. 15–20 RGPD).
* **Contacto:** Para exercer os seus direitos, contacte o e-mail acima.
* **Reclamação:** Tem o direito de apresentar reclamação a uma autoridade de controlo.

## 6. Segurança de Dados
Implementamos medidas técnicas e organizativas (ex: encriptação) para proteger os seus dados (Art. 32 RGPD).

## 7. Alterações
Reservamo-nos o direito de atualizar esta política. As alterações serão publicadas aqui.