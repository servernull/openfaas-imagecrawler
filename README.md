# OpenFaaS ImageCrawler

An [OpenFaaS](https://www.openfaas.com/) function which is an image crawler that returns a list of jpg and png images on a site
```bash
# deploy
faas-cli deploy -f stack.yml

# invoke synchronously
echo http://scottleedavis.com | faas-cli invoke openfaas-imagecrawler | jq

# invoke asynchonously
echo http://scottleedavis.com | faas-cli invoke openfaas-imagecrawler --async --header "X-Callback-Url=http://192.168.0.22:9999"

[
  "http://scottleedavis.com/assets/img/tortoise.jpg",
  "http://scottleedavis.com/assets/img/linkedin.png",
  "http://scottleedavis.com/assets/img/achilles.jpg",
  "http://scottleedavis.com/assets/img/github.png",
  "http://scottleedavis.com/assets/img/ijmuiden-gps-data-1.jpg",
  "http://scottleedavis.com/assets/img/circadia.png",
  "http://scottleedavis.com/assets/img/twitter.png",
  "http://scottleedavis.com/assets/img/scott.jpeg",
  "http://scottleedavis.com/assets/img/light_art.png",
  "https://github.com/scottleedavis/google-earth-toolbox/raw/master/screenshot.png"
]
```
