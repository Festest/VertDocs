# A Carteira Vertcoin Core
![CoreWallet](https://i.imgur.com/gl5am5j.png)
## Instalação

### Download através do GitHub

Para instalar a carteira Vertcoin Core, navega até ao repositório do Vertcoin Core [Página das versões lançadas] (https://github.com/vertcoin/vertcoin/releases) no GitHub e faz o download dos ficheiros da versão mais recente. Versões para o Windows, Linux e OSX estão disponíveis.

Dentro do ficheiro zip que descarregou, encontram-se 4 aplicações: vertcoin-qt, vertcoind, vertcoin-cli e ainda o vertcoin-tx.

| Aplicação    | Descrição                                                        |
|--------------|------------------------------------------------------------------|
| vertcoin-qt  | Carteira Core com a interface GUI.                               |
| vertcoind    | "Daemon" da carteira Core.                                       |
| vertcoin-cli | Interface de Terminal para interagir com o vertcoind.            |
| vertcoin-tx  | Interface de Terminal para criar, validar e modificar transações |

Para iniciar o Vertcoin Core, execute o ficheiro vertcoin-qt. Isto irá iniciar a carteira com a interface GUI. Poderá, opcionalmente, escolher executar a carteira como um "deamon", que ficará ativo no background, através do ficheiro vertcoind.

### Download PPA no Linux Ubuntu
Pode instalar k vertcoind (headless deamon) ou a carteira com interface GUI,
vertcoin-qt via Vertcoin ppa.

``` shell
$ sudo add-apt-repository ppa:vertcoin/ppa
$ sudo apt-get update
```

##### vertcoind
Seguidamente, para instalar o vertcoind execute:
``` shell
$ sudo apt-get install vertcoind
```

Inicie o vertcoind através do terminal com o seguinte comando:
``` shell
$ vertcoind -daemon
```

Pode interagir com o vertcoind via:
``` shell
$ vertcoin-cli help
```

##### vertcoin-qt
Para instalar a carteira com interface GUI:
``` shell
$ sudo apt-get install vertcoin-qt
```

Completados estes passos, poderá executar o Vertcoin através do icon da aplicação que estará no seu launcher.

##  Executar o Vertcoin Core
Na primeira vez que executar o Vertcoin Core poderá escolher onde gostaria de armazenar os dados. Neste passo, pode deixar o diretório padrão ou escolher aquele que lhe é mais favorável. Depois de selecionado o diretório e avançar, o Vertcoin Core tentará conectar-se a outros Vertcoin Core nodes para que possa fazer o download completo da blockchain do Vertcoin.

![FirstRun](https://i.imgur.com/C0HQXyI.png)

!!!Atenção "Nota"
    A carteira Vertcoin Core necessita de pelo menos 5 GB de espaço livre no seu computador para que possa armazenar a blockchain. Fazer o download desta pela primeira vez pode ser um processo demoroso.

À medida que a blockchain é descarregada, poderá ver o progresso do download, assim como os últimos blocks a serem sincronizados. Cada vez que a carteira é executada, a sua cópia local da blockchain precisará de ser sincronizada até ao bloco atual.

## Backing Up Your Wallet
It is important to understand that vertcoin wallets contain only keys. The "coins" are recorded in the blockchain on the vertcoin network. Users control the coins on the network by signing transactions with the keys in their wallets. In a sense, a vertcoin wallet is a keychain.`[1]`

Vertcoin Core creates a nondeterministic wallet,where each key is independently generated from a random number. The keys are not related to each other. This type of wallet is also known as a JBOK wallet from the phrase "Just a Bunch Of Keys."`[1]`

It is crucial that you back up your `wallet.dat` file found in your Vertcoin data directory. 

## Sending & Recieving Vertcoin
Once your Vertcoin Core client has finished syncing to the blockchain you are ready to send and recieve Vertcoin. 

![RequestPay](https://i.imgur.com/jRdy3eQ.png)  
**To recieve Vertcoin press the `Receive` button**  
* Fill out `optional` fields 
* Click `Request payment`  

------------------------------------------------

![SendVTC](https://i.imgur.com/lRAIxl2.png)  
**To send Vertcoin press the `Send` button**
* Enter `recieve` address you want you want to pay Vertcoin
* Enter the amount of VTC to send
* Attach an `optional` label  

![Confirm](https://i.imgur.com/0WF7QFs.png)

### Addresses
In the payment portion of a vertcoin transaction, the recipient’s public key is represented by its digital fingerprint, called a vertcoin address, which is used in the same way as the beneficiary name on a check (i.e., "Pay to the order of"). In most cases, a vertcoin address is generated from and corresponds to a public key.`[1]` 

In vertcoin, we use public key cryptography to create a key pair that controls access to vertcoin. The key pair consists of a private key and—​derived from it—​a unique public key. The public key is used to receive funds, and the private key is used to sign transactions to spend the funds.`[2]`

### Coin Controls
When you send vertcoin to someone else, the vertcoin client chooses automatically picks which addresses you own that hold VTC balance will send coins. Coin control allows control over what coins you send, and which of your addresses sends VTC. More specifically, which of your unspent outputs will be the sending inputs.`[3]`

## References
`[1] Mastering Bitcoin 2nd Edition - Keys, Addresses - https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch04.asciidoc#keys-addresses`  
`[2] Mastering Bitcoin 2nd Edition - Public Key Cryptography and Cryptocurrency - https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch04.asciidoc#public-key-cryptography-and-cryptocurrency`  
`[3] Yet another Coin Control Release - https://bitcointalk.org/index.php?topic=144331.0` 

