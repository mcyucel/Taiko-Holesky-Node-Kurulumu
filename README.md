# Taiko-Holesky-Node-Kurulumu
Taiko Holesky Node Kurulumu

Gereksinimler: 2 CPU 4 RAM 200 GB Yeterli

Sistemimizi Güncelleyelim

```shell
sudo apt update & sudo apt upgrade```

Docker Kuralım

```shell
sudo apt install docker-compose```


```shell
sudo apt-get update && sudo apt install jq && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin && sudo apt-get install docker-compose-plugin```

Git Kurulumu

```shell
sudo apt-get install git-all```

Versiyon Kontrolü

```shell
git version```

Kuruluma Geçebiliriz

```shell
git clone https://github.com/taikoxyz/simple-taiko-node.git```

```shell
cd simple-taiko-node```

```shell
cp .env.sample .env```

Nano İçine Girelim

```shell
nano .env```

Ok Tuşlarıyla İlgili yerlere Girelim

Endpointleri Dolduruyoruz

Alchemy, Infura gibi RPC sağlayıcılarda şu an Holesky yok. Bununla ilgili bir bilgi de yok ancak muhtemelen kendi RPC'sini gireceğiz. Aşağıdaki gibi dolduralım.

L1_ENDPOINT_HTTP=https://ethereum-holesky.publicnode.com
L1_ENDPOINT_WS=wss://ethereum-holesky.publicnode.com

Gerekli Yerleri Aşağıdaki Gibi Dolduruyoruz

ENABLE_PROVER=true
L1_PROVER_PRIVATE_KEY="Metamask Adresinizin Private Key'i" (Tırnakları Kaldırın)

CTRL+X sonrasında y ve entera basıp kaydediyoruz.

Nodeu başlatalım

```shell
docker compose up -d```



www.x.com/0xMultijet
