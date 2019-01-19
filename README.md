# Goka
## Painless stream processing with Go and Kafka

## Agenda
* Setup
  * getting the dependencies
  * starting kafka locally
* Sarama Example
* Goka concepts
  * starting an emitter
  * starting a producer
  * starting a view
  * some monitoring
  * testing our code

# Set up your working environment

* Golang https://golang.org/dl/
* Docker/Git
  * Mac:
```bash
brew install git
brew cask install docker
open /Applications/Docker.app
```

  * Linux:
```bash
sudo apt-get install docker git
```

* Setup a Gopath (if you don't have it yet)
```bash
mkdir -p $HOME/gocode/
cd $HOME/gocode
export GOPATH=$HOME/gocode
```

* Get the Workshop Code
```bash
# need to have $GOPATH set
go get github.com/frairon/goka-godays2019
```

* Start Kafka locally
```bash
make restart-kafka
```

* Get the workshop data
```bash
# tiny data set is located in testdata/taxidata_tiny.csv
# 100k dataset can be loaded from https://storage.googleapis.com/lv-goka-godays2019/taxidata_100k.csv
make get-100

# [Optional]
# full dataset (~320MB) can be downloaded from https://storage.googleapis.com/lv-goka-godays2019/taxidata_complete.csv
make get-complete
```



## Now you're ready to start working with the code
