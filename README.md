# Taiko-Holesky-Node-Kurulumu
Taiko Holesky Node Kurulumu

Gereksinimler: 2 CPU 4 RAM 200 GB Yeterli

Sistemimizi Güncelleyelim

```shell
sudo apt update & sudo apt upgrade```

Docker Kuralım

```sudo apt install docker-compose```


```sudo apt-get update && sudo apt install jq && sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin && sudo apt-get install docker-compose-plugin```

Git Kurulumu

```sudo apt-get install git-all```

Versiyon Kontrolü

```git version```

Kuruluma Geçebiliriz

```git clone https://github.com/taikoxyz/simple-taiko-node.git```

```cd simple-taiko-node```

```cp .env.sample .env```

Nano İçine Girelim

```nano .env```

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

```docker compose up -d```



www.x.com/0xMultijet
