You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css",
    "context": {
      "path": "css/138575cd4810b87ba229d0ae35cbc7b8.css"
    }
  },
  {
    "path": "css/2bbb144255adda9d07ceef7a88019836.css",
    "context": {
      "path": "css/2bbb144255adda9d07ceef7a88019836.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/67a53f1cb74a2e85ef448f42951113fc.css",
    "context": {
      "path": "css/67a53f1cb74a2e85ef448f42951113fc.css"
    }
  },
  {
    "path": "css/7279f652e317fec6054375cf49ca1b96.css",
    "context": {
      "path": "css/7279f652e317fec6054375cf49ca1b96.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d550fed54e8dea5d2e32837b06788126.css",
    "context": {
      "path": "css/d550fed54e8dea5d2e32837b06788126.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "gallery.html",
    "context": {
      "title": "Villa Rashmi | Gallery",
      "first_heading": "Front Yard"
    }
  },
  {
    "path": "history.html",
    "context": {
      "title": "Villa Rashmi | History",
      "first_heading": "History of Villa Rashmi"
    }
  },
  {
    "path": "imgs/007618e6e786b32bfde6425c62285a1f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e562c61955cec01f8aa585ac00e2b13.webp",
    "context": {
      "refs": [
        {
          "alt": "PARKING AREA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/248c8a48e47b13fce67a3458f2b62552.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2bd64afe00719c3fb5791b18e3537d46.webp",
    "context": {
      "refs": [
        {
          "alt": "Props",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2d5ed08f0748876e652ff359b457b696.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/341aaba51f3948d09ac4d81210365f6f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3b57e5193f778c8ed36e5806a441d326.webp",
    "context": {
      "refs": [
        {
          "alt": "WASHROOMS FOR CREW",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/40289990077d7474e10efee1950471a4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/422ceece0e2056ef72a87eba05077cef.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4781dbcfebc37b4633d3043bbb035a81.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/49a195b1313a1972c130a1fd07b50e03.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4f81109a63c489237cb0d736c36f7a63.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/58f09dcf3c787d9193abb98b5ea7da16.webp",
    "context": {
      "refs": [
        {
          "alt": "First Level (Ground floor)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/612b2ddc7836075827867d2712024487.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/639f2c94dba122386d033ee063b8c937.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/668496b3063fda0e0d0ca97ca18ad6d4.webp",
    "context": {
      "refs": [
        {
          "alt": "Plants",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6a25467fc4e60039035af8db24e0b779.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/8009c5a102136fa5d2881730366b7920.webp",
    "context": {
      "refs": [
        {
          "alt": "CCTV",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86995ba649106e6b174b8f0514b58ca3.webp",
    "context": {
      "refs": [
        {
          "alt": "View more on",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8871c2fa1efeba0ae21140c7bc29070e.webp",
    "context": {
      "refs": [
        {
          "alt": "Front yard",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/92f5e9ede3309439e3f9e6a1173f74ed.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/93fc37ac127fbac69c5b64f4a98d201d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9797d62f2ed925aaced4919ba1b29d8f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9e2a942674c060e6e3985bbdbd1f2b06.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ea75710dfb65f26203902d4e1325354.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9f427eaa2fc1863f30201ac7356371e5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af45954ac20f3194d1c6c4c3fd0e8e4a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9a09daa5e053663954bbe30b5ada8eb.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bae7a0ad3fab444dd1b47af140824f07.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bf706c805f533736d4fd9ba84c198153.webp",
    "context": {
      "refs": [
        {
          "alt": "FURNITURE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c3367bd03a570489dacacaf77f04fd42.webp",
    "context": {
      "refs": [
        {
          "alt": "Second Level (First floor)",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c92c75ac6e74f230c851e58a37bcab63.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/caf11adbbf182ab7cdd33ae27096a507.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d1232936722a594f4f5769f7f793859a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d5d9cce2f548da004ff7b3d715de228d.webp",
    "context": {
      "refs": [
        {
          "alt": "MAKEUP ROOM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de4799b433dc7b43ce1ea690cd7f59bb.webp",
    "context": {
      "refs": [
        {
          "alt": "Download Presentation",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e3e77497e7bb9a6b287ef4a8421479fc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e49c3168cc9b6cf1bd69b19719eeb35e.webp",
    "context": {
      "refs": [
        {
          "alt": "CATERING AREA",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa19dee474340bf5882ea5703fc184ed.webp",
    "context": {
      "refs": [
        {
          "alt": "Back yard",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc34bd48d4cd4af5fd207bc9ec62be0a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ff5f3236ee1d28b083ec8e2d14f027c2.webp",
    "context": {
      "refs": [
        {
          "alt": "View more on",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Villa Rashmi is a one-of-a-kind 100-year old heritage villa in Mumbai | Home",
      "first_heading": "Vintage Villa in the City"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "js/faf9ce4e848522206b5c3043551fb2d7.js",
    "context": {
      "path": "js/faf9ce4e848522206b5c3043551fb2d7.js"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.