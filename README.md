# Web-Application-Enumeration

download golang

https://golang.org/doc/install?download=go1.15.6.linux-amd64.tar.gz

└──╼ $sudo tar -xvf go1.15.6.linux-amd64.tar.gz  -C /usr/local/

└──╼ $sudo chown -R root:root /usr/local/go

└──╼ $sudo gedit ~/.profile                                                                                                                                  

add these two lines 
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin

└──╼ $. ~/.profile                                                                                                                                           

└──╼ $go version
go version go1.15.6 linux/amd64

--------------------------------Finding Subdomains with Assetfinder

https://github.com/tomnomnom/assetfinder

go get -u github.com/tomnomnom/assetfinder

└──╼ $assetfinder tesla.com                                                                                                                                  

└──╼ $assetfinder --subs-only tesla.com                                                                                                                      


------------------------------Finding Subdomains with Amass

https://github.com/OWASP/Amass
https://github.com/OWASP/Amass/blob/master/doc/install.md

└──╼ $export GO111MODULE=on
└──╼ $go get -v github.com/OWASP/Amass/v3/...

└──╼ $amass enum -d tesla.com                                                                                                                                


----------------------------Finding Alive Domains with Httprobe
https://github.com/tomnomnom/httprobe
└──╼ $go get -u github.com/tomnomnom/httprobe

└──╼ $cat test.txt | httprobe                                                                                                                                
└──╼ $cat test.txt | httprobe -s -p https:443                                                                                                                
└──╼ $cat test.txt | httprobe -s -p https:443 | sed 's/https\?:\/\///' | tr -d ':443'



-------------------------------Screenshotting Websites with GoWitness
https://github.com/sensepost/gowitness
https://github.com/sensepost/gowitness/wiki/Installation

└──╼ $go get -u github.com/sensepost/gowitness

└──╼ $gowitness single https://tesla.com                                                                                                               


