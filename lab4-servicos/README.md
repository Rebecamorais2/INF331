
## Serviços

### Tarefa 1
![Componentes de Negócio](https://github.com/Rebecamorais2/INF331/blob/master/lab4-servicos/images/tarefa1.PNG)

### Tarefa 2

![Componentes Técnicos View-Controller](https://github.com/Rebecamorais2/INF331/blob/master/lab4-servicos/images/tarefa2.PNG)

### Tarefa 3
![Componentes Técnicos-Model-Controller](https://github.com/Rebecamorais2/INF331/blob/master/lab4-servicos/images/tarefa3.PNG)

### Tarefa 4

#### Serviço 1

* **Título do serviço:** Spotify
  
* **Breve descrição:** O Serviço recebe um tipo e um limite e retorna os artistas que eu sigo com suas respectivas imagens


* **URL completa da requisição:** https://any-api.com:8443/https://api.spotify.com/v1/me/following?type=artist&limit=1&after=0
  
* **Cabeçalho HTTP da chamada:**
~~~~htp
:authority: any-api.com:8443
:method: GET
:path: /https://api.spotify.com/v1/me/following?type=artist&limit=1&after=0
:scheme: https
accept: */*
accept-encoding: gzip, deflate, br
accept-language: en-US,en;q=0.9,pt;q=0.8
authorization: Bearer BQDwAhd94fU7e2PN4zN82z9XcSSxpMM1dfwq2P8e6EU1qlDA2srpvGvB9EGTuFjiUs958F2-adB6HqaSbKVKeG6zMONG0cTLwIVSP7d05WLeQ9KpD4d7c-4Zj0O9TLXGUcC9W0CC63RSobkl8HPWbCbKKxXkOfhXfxzH8yxAsG8sIktQp1SeQJOtubjiWjX8ABPgqdLG1tA3KFMhH5JeNNhet3a0JYXYFCL6FsLRhitLaBUGDvtoewhGxMT6J-Sdv7HD
cache-control: no-cache
origin: https://any-api.com
pragma: no-cache
referer: https://any-api.com/spotify_com/spotify_com/console/_me_following/GET
sec-fetch-dest: empty
sec-fetch-mode: cors
sec-fetch-site: same-site
user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.135 Safari/537.36
~~~~

* **Cabeçalho HTTP da resposta:**
~~~~http
access-control-allow-credentials: true
access-control-allow-headers: Accept, App-Platform, Authorization, Content-Type, Origin, Retry-After, Spotify-App-Version, X-Cloud-Trace-Context
access-control-allow-methods: GET, POST, OPTIONS, PUT, DELETE, PATCH
access-control-allow-origin: *
access-control-expose-headers: content-type,cache-control,etag,vary,x-robots-tag,access-control-allow-origin,access-control-allow-headers,access-control-allow-methods,access-control-allow-credentials,access-control-max-age,content-encoding,strict-transport-security,x-content-type-options,date,server,via,alt-svc,connection,transfer-encoding,x-final-url
access-control-max-age: 604800
cache-control: private, max-age=0
cf-cache-status: DYNAMIC
cf-ray: 5c75ebb50e72cff4-GRU
cf-request-id: 04bd91a5260000cff4c3b91200000001
content-encoding: br
content-type: application/json; charset=utf-8
date: Sun, 23 Aug 2020 15:38:28 GMT
etag: W/"MC-IjM4MmVkYzgzMTAyYWRiZTdlYzcyZjk4NjNmNDU4Y2Q0Ig=="
expect-ct: max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"
server: cloudflare
set-cookie: __cfduid=de8a902804d00924e487791c2fc0896951598197108; expires=Tue, 22-Sep-20 15:38:28 GMT; path=/; domain=.any-api.com; HttpOnly; SameSite=Lax
status: 200
strict-transport-security: max-age=31536000
vary: Authorization
via: HTTP/2 edgeproxy, 1.1 google
x-content-type-options: nosniff
x-final-url: https://api.spotify.com/v1/me/following?type=artist&limit=1&after=0
x-request-url: https://api.spotify.com/v1/me/following?type=artist&limit=1&after=0
x-robots-tag: noindex, nofollow
~~~~
* **Conteúdo da resposta:**
~~~~json
{
  "artists" : {
    "items" : [ {
      "external_urls" : {
        "spotify" : "https://open.spotify.com/artist/1elUiq4X7pxej6FRlrEzjM"
      },
      "followers" : {
        "href" : null,
        "total" : 12738165
      },
      "genres" : [ "sertanejo", "sertanejo universitario" ],
      "href" : "https://api.spotify.com/v1/artists/1elUiq4X7pxej6FRlrEzjM",
      "id" : "1elUiq4X7pxej6FRlrEzjM",
      "images" : [ {
        "height" : 640,
        "url" : "https://i.scdn.co/image/10922ac8c851362ca476e41dd0bc6a151c554333",
        "width" : 640
      }, {
        "height" : 320,
        "url" : "https://i.scdn.co/image/04c73e4095fa2e974d5897f7378d1674d6413e4e",
        "width" : 320
      }, {
        "height" : 160,
        "url" : "https://i.scdn.co/image/d983e9389e493b604d334d420fd201307cf6c49d",
        "width" : 160
      } ],
      "name" : "Jorge & Mateus",
      "popularity" : 81,
      "type" : "artist",
      "uri" : "spotify:artist:1elUiq4X7pxej6FRlrEzjM"
    } ],
    "next" : "https://api.spotify.com/v1/me/following?type=artist&after=1elUiq4X7pxej6FRlrEzjM&limit=1",
    "total" : 5,
    "cursors" : {
      "after" : "1elUiq4X7pxej6FRlrEzjM"
    },
    "limit" : 1,
    "href" : "https://api.spotify.com/v1/me/following?type=artist&after=0&limit=1"
  }
}
}
~~~~

#### Serviço 2

* **Título do serviço:** Healthcare
  
* **Breve descrição:** O Serviço recebe um tipo de retorno e um nome de um estado dos EUA e retorna informações sobre como funciona o sistema de saúde no estado


* **URL completa da requisição:** https://any-api.com:8443/https://www.healthcare.gov/Nevada.json
  
* **Cabeçalho HTTP da chamada:**
~~~http
:authority: any-api.com:8443
:method: GET
:path: /https://www.healthcare.gov/Nevada.json
:scheme: https
accept: */*
accept-encoding: gzip, deflate, br
accept-language: en-US,en;q=0.9
cache-control: no-cache
origin: https://any-api.com
pragma: no-cache
referer: https://any-api.com/healthcare_gov/healthcare_gov/console/_stateName_mediaTypeExtension_/GET
sec-fetch-dest: empty
sec-fetch-mode: cors
sec-fetch-site: same-site
user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/84.0.4147.135 Safari/537.36
~~~ 

* **Cabeçalho HTTP da resposta:**
~~~http
access-control-allow-origin: *
access-control-expose-headers: accept-ranges,etag,last-modified,vary,content-encoding,date,content-length,connection,strict-transport-security,content-type,x-xss-protection,x-permitted-cross-domain-policies,x-frame-options,x-final-url,access-control-allow-origin
cf-cache-status: DYNAMIC
cf-ray: 5ca0157d8d74eebe-GRU
cf-request-id: 04d7ebc2790000eebe6692a200000001
content-encoding: br
content-type: application/json
date: Fri, 28 Aug 2020 18:27:01 GMT
etag: W/"3658cc0b86ca1e12187a63fdda94095f:1580425900"
expect-ct: max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"
last-modified: Thu, 30 Jan 2020 23:11:40 GMT
server: cloudflare
set-cookie: __cfduid=d347d499e8c804643487051019f39ab5e1598639221; expires=Sun, 27-Sep-20 18:27:01 GMT; path=/; domain=.any-api.com; HttpOnly; SameSite=Lax
status: 200
strict-transport-security: max-age=31536000 ; preload
vary: Accept-Encoding
x-final-url: https://www.healthcare.gov/Nevada.json
x-frame-options: SAMEORIGIN
x-permitted-cross-domain-policies: master-only
x-request-url: https://www.healthcare.gov/Nevada.json
x-xss-protection: 1; mode=block
~~~
* **Conteúdo da resposta:**
~~~JSON
{
  "draft": false,
  "categories": [],
  "experience": "learn",
  "type": "state",
  "lang": "en",
  "tags": [
    "state"
  ],
  "dropdown": {
    "smb": {
      "apply": {
        "txt": [
          "LEARN MORE NOW"
        ],
        "url": [
          "/small-businesses/provide-shop-coverage/"
        ]
      }
    },
    "emp": {
      "apply": {
        "txt": [
          "LEARN MORE"
        ],
        "url": [
          "/small-businesses/employees-shop/overview/"
        ]
      }
    }
  },
  "date": "0001-01-31 23:59:56 -0456",
  "title": "Nevada",
  "slug": "nevada",
  "ext": ".md",
  "excerpt": "<h3>Consumer Assistance in Nevada</h3>\n\n<p>The Nevada Consumer Assistance Program is run by the Nevada Governor’s Office for Consumer Health Assistance (GovCHA) in partnership with four non-profit groups: Access to Health Care Network (AHN), Rebuilding All Goals Efficiently (RAGE), State Health Insurance Assistance Program (SHIP), and Salud en Accion (SEA). Staff can answer questions about health insurance regulations, rights, and responsibilities. They can help you file a complaint or appeal a health plan decision. <a href=\"http://dhhs.nv.gov/CHA.htm\">Get consumer help with a problem or question</a>.</p>\n\n<h3>Medicaid in Nevada</h3>\n\n<p>You can apply for Medicaid in Nevada by <a href=\"https://dwss.nv.gov/\">contacting your state Medicaid agency</a>.</p>\n\n<h3>SHOP Health Insurance Marketplace in Nevada</h3>\n\n<h3>SHOP Health Insurance Marketplace for Employees in Nevada</h3>\n\n<h3>Health Insurance Marketplace in Nevada</h3>\n\n<p>If you live in Nevada, you’ll use the Nevada Health Link website to enroll in health coverage.</p>\n\n<h3>CHIP in Nevada</h3>\n\n<p>Nevada Check Up covers uninsured children in families with moderate incomes that are too high to qualify for Medicaid. You can find out whether your children qualify for Nevada Check Up right now. <a href=\"https://www.healthcare.gov/marketplace/individual/\">Fill out a Marketplace application</a> and find out whether your children qualify. <a href=\"https://dwss.nv.gov/\">Learn more about Nevada Check Up</a>.</p>\n",
  "url": "/nevada/",
  "content": "<h3>Consumer Assistance in Nevada</h3>\n\n<p>The Nevada Consumer Assistance Program is run by the Nevada Governor’s Office for Consumer Health Assistance (GovCHA) in partnership with four non-profit groups: Access to Health Care Network (AHN), Rebuilding All Goals Efficiently (RAGE), State Health Insurance Assistance Program (SHIP), and Salud en Accion (SEA). Staff can answer questions about health insurance regulations, rights, and responsibilities. They can help you file a complaint or appeal a health plan decision. <a href=\"http://dhhs.nv.gov/CHA.htm\">Get consumer help with a problem or question</a>.</p>\n\n<h3>Medicaid in Nevada</h3>\n\n<p>You can apply for Medicaid in Nevada by <a href=\"https://dwss.nv.gov/\">contacting your state Medicaid agency</a>.</p>\n\n<h3>SHOP Health Insurance Marketplace in Nevada</h3>\n\n<h3>SHOP Health Insurance Marketplace for Employees in Nevada</h3>\n\n<h3>Health Insurance Marketplace in Nevada</h3>\n\n<p>If you live in Nevada, you’ll use the Nevada Health Link website to enroll in health coverage.</p>\n\n<h3>CHIP in Nevada</h3>\n\n<p>Nevada Check Up covers uninsured children in families with moderate incomes that are too high to qualify for Medicaid. You can find out whether your children qualify for Nevada Check Up right now. <a href=\"https://www.healthcare.gov/marketplace/individual/\">Fill out a Marketplace application</a> and find out whether your children qualify. <a href=\"https://dwss.nv.gov/\">Learn more about Nevada Check Up</a>.</p>\n",
  "sort": 0
}
~~~
