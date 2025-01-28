# Ataque-de-Phishing
Criar um ataque de phishing usando o Kali Linux envolve o uso de ferramentas poderosas, como o Social-Engineer Toolkit (SET), para gerar páginas falsas de login e capturar informações sensíveis como nome de usuário e senha.
Porém, antes de executar qualquer tipo de ataque, é importante lembrar que isso deve ser feito apenas em ambientes controlados e com permissão explícita da vítima, como em testes de penetração (pentests) ou simulações de phishing em ambientes de laboratório.

A seguir, está o passo a passo para configurar um ataque de phishing usando o Kali Linux com o SET. Vamos criar uma página falsa de login do Facebook e usar a ferramenta SET para capturar as credenciais fornecidas por vítimas fictícias.

Passo a Passo para Criar um Ataque de Phishing no Kali Linux
1. Configuração do Ambiente no Kali Linux
Primeiro, é necessário garantir que o Kali Linux está atualizado e tem as ferramentas necessárias instaladas, como o Social-Engineer Toolkit (SET).

Abra o terminal e atualize o sistema:

bash
Copiar
Editar
sudo apt update && sudo apt upgrade -y
Verifique se o SET está instalado:

bash
Copiar
Editar
setoolkit --help
Caso o SET não esteja instalado, use o comando abaixo para instalá-lo:

bash
Copiar
Editar
sudo apt install set
2. Iniciar o Social-Engineer Toolkit (SET)
Para iniciar o SET, use o comando:

bash
Copiar
Editar
sudo setoolkit
3. Seleção da Opção para Ataque de Phishing
Ao executar o SET, você verá um menu interativo. Selecione a opção para realizar um ataque de phishing:

bash
Copiar
Editar
1) Social-Engineering Attacks
Agora, você precisará escolher a opção para realizar um ataque com o servidor de credenciais (credential harvester):

bash
Copiar
Editar
2) Website Attack Vectors
Selecione a opção de ataque usando a técnica de Harvester:

bash
Copiar
Editar
3) Credential Harvester Attack Method
Agora, escolha a opção Clone a website para criar uma página falsa de login:

bash
Copiar
Editar
2) Site Cloner
4. Clonar a Página de Login
O SET pedirá para você inserir o IP de destino ou o IP de onde você deseja que a página falsa esteja hospedada. Isso será o IP do seu Kali Linux:

bash
Copiar
Editar
IP address for the POST back in Harvester/Tabnabbing [172.26.33.215]:
Deixe o valor padrão ou insira o IP da sua máquina no qual o SET estará escutando.

O SET pedirá para você inserir a URL do site que você deseja clonar, como por exemplo o Facebook:

bash
Copiar
Editar
Enter the URL to clone: https://www.facebook.com
5. Iniciar o Servidor de Phishing
Depois de clonar o site, o SET configurará um servidor local para hospedar a página falsa. O servidor estará escutando na porta 80 e você pode compartilhá-lo com suas vítimas fictícias.

O SET pode solicitar que você desative serviços de web (como Apache) para garantir que a porta 80 esteja livre para o servidor phishing.

Se você for solicitado a desativar o Apache, digite y para confirmar.

Após a confirmação, o SET começará a capturar as credenciais digitadas nas páginas falsas de login.

6. Visualizando as Credenciais Capturadas
O SET exibirá as credenciais no terminal conforme forem inseridas na página falsa.

As credenciais serão armazenadas no arquivo /root/.set/harvester/logs/credentials.log ou no local configurado.

Código para o GitHub
Agora, para configurar esse ataque em um repositório GitHub, você pode criar um repositório e adicionar os arquivos necessários, incluindo o código ou comandos para execução.

Crie um repositório no GitHub com um nome como phishing-attack-SET.
No repositório, crie um arquivo chamado README.md e adicione as instruções detalhadas para executar o ataque.
Crie um script em Python ou Bash (para automatizar a execução no Kali Linux) e adicione ao repositório.
