# 📱 PiHoleMonitor – Guia do Usuário

Este manual auxilia na configuração e utilização da aplicação **PiHoleMonitor**. O PiHoleMonitor é um cliente não oficial para o **Pi-hole®**, permitindo-lhe monitorizar e gerir convenientemente as suas instâncias de filtragem de anúncios através de uma interface nativa construída com Jetpack Compose.

---

### 📖 Índice
* [1. Segurança e Privacidade](#1-segurança--privacidade)
* [2. Configuração do Servidor](#2-configuração-do-servidor)
* [3. Dashboard](#3-dashboard)
* [4. Gestão](#4-gestão)
* [5. Logs de Consulta](#5-logs-de-consulta)
* [6. Sistema](#6-sistema)
* [7. Definições](#7-definições)

---

## 🛡️ 1. Segurança e Privacidade
Uma vez que a aplicação interage com a sua infraestrutura de rede, a proteção de dados é a nossa maior prioridade.

* **Encriptação**: Dados sensíveis como palavras-passe e IDs de sessão nunca são armazenados em texto simples. A aplicação utiliza **encriptação AES-GCM** dentro do **Android KeyStore** protegido por hardware.
* **Autenticação**: A comunicação segue o protocolo oficial da API utilizando IDs de sessão seguros (`sid`) e tokens CSRF.
* **Localidade**: O PiHoleMonitor é "Offline-First". **Nenhum dado é transmitido** para servidores cloud externos do programador. Todas as ligações ocorrem diretamente entre o seu smartphone e a sua instância Pi-hole.
* **Biometria**: Pode opcionalmente proteger o acesso à aplicação utilizando a sua impressão digital, reconhecimento facial ou PIN.

---

## ⚙️ 2. Configuração do Servidor
Para utilizar a aplicação, deve registar a sua instância Pi-hole (suporte API v6+).

* **Nome do Servidor**: Um nome livremente definível para identificação dentro da app.
* **Domínio / IP**: O endereço da sua instância (ex: `192.168.178.5`).
* **Porta**: A porta da interface web (Predefinição: `80` para HTTP ou `443` para HTTPS).
* **Sub-rota (Opcional)**:
    > 💡 **Nginx / Reverse-Proxy**: Se o seu Pi-hole estiver acessível através de um sub-caminho como `dominio.com/pihole`, introduza `/pihole` aqui. A aplicação adiciona automaticamente o sufixo `/api/` necessário internamente.
* **Palavra-passe**: A palavra-passe da sua interface web Pi-hole.
* **Tipo de Ligação**: Escolha entre **HTTPS** (recomendado) ou **HTTP**.

### Teste de Ligação e Gravação
* **Verificar Ligação**: Realiza um pedido de teste para validar a acessibilidade e a correção da palavra-passe.
* **Guardar (Ícone de Disco)**: Grava os dados no armazenamento encriptado. Na configuração inicial, este servidor é automaticamente marcado como a instância ativa.

![Screenshot Server Setup](screenshots/new_server.jpg)
---

## 📊 3. Dashboard
O Dashboard fornece uma visão geral em tempo real da saúde da sua rede.

* **Histórico 24h**: Acompanhe as consultas DNS nas últimas 24 horas num gráfico detalhado.
* **Estatísticas Totais**: Resumo do total de consultas, pedidos bloqueados e taxa de bloqueio atual.
* **Ranking de Clientes**: Identifique os clientes mais ativos na sua rede.

---

## 🗂️ 4. Gestão
Gira a configuração do seu Pi-hole diretamente na aplicação.

* **Clientes**: Visualize, crie e edite clientes de rede.
* **Listas de Anúncios (Gravity)**: Gira as suas fontes de listas de bloqueio utilizadas para filtrar publicidade.
* **Domínios**: Mantenha listas brancas e negras (exatas ou baseadas em regex).
* **Grupos**: Organize clientes e listas em grupos lógicos.

---

## 🔍 5. Logs de Consulta
Insights profundos sobre o tráfego DNS da sua rede.

* **Filtro de Estado**: Filtre especificamente por consultas permitidas, bloqueadas o em cache.
* **Pesquisa**: Pesquise domínios específicos ou endereços IP de clientes.

---

## 💻 6. Sistema
Monitorização do hardware e do ambiente de rede.

* **Sistema Anfitrião**: Apresenta informações do host, carga do CPU, utilização de RAM e o estado do processo `pihole-FTL`.
* **Pi-hole**: Ative/desative o filtro DNS, monitorize a utilização da cache DNS, execute ações do Pi-hole e visualize notificações do sistema.
* **Rede**: Visão geral detalhada de gateways, interfaces e rotas.
* **DHCP**: Gestão de concessões (leases) DHCP ativas.

### Ações Disponíveis:
* **Reiniciar FTL**: Reinicia o serviço DNS na sua instância.
* **Atualização Gravity**: Aciona uma atualização da lista de bloqueio.
* **Flush Logs/ARP**: Limpa os logs de consulta DNS ou limpa a tabela de rede.

> [!CAUTION]
> **Aviso**: A execução de ações do Pi-hole, como reiniciar o FTL ou atualizar o Gravity, causará uma breve interrupção da resolução DNS em toda a sua rede.
> 
> **Limpar Logs e ARP**: Estas ações eliminam permanentemente todos os logs de consulta e limpam a lista de dispositivos de rede conhecidos (tabela de rede).

---

## 🛠️ 7. Definições
Personalize a sua experiência no PiHoleMonitor.

* **Tema e Idioma**: Alterne entre o modo Escuro/Claro e selecione o idioma do sistema preferido.
* **Notificações**: Configure alertas ao nível do sistema.
* **Widgets**: Personalize a aparência dos widgets do seu ecrã principal.
* **Segurança**: Configure as definições de início de sessão biométrico.
* **Manutenção**: Ative ou desative o envio de relatórios de falhas.
* **Gravador de Logs de Debug**: Utilize o gravador de logs para auxiliar na resolução de problemas.
