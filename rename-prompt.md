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
    "path": "Privacy.html",
    "context": {
      "title": "Axceltrees Consulting Private Limited | Finding the Perfect Job Only Got Easier",
      "first_heading": ""
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "Axceltrees Consulting Private Limited | About Us",
      "first_heading": "AboutUs"
    }
  },
  {
    "path": "apply-now.html",
    "context": {
      "title": "Axceltrees Consulting Private Limited | Apply Now",
      "first_heading": "ApplyNow"
    }
  },
  {
    "path": "apply-resume.html",
    "context": {
      "title": "Axceltrees Consulting Private Limited | Apply Now",
      "first_heading": "ApplyResume"
    }
  },
  {
    "path": "clients.html",
    "context": {
      "title": "Axceltrees Consulting Private Limited | Clients",
      "first_heading": "Some of Our ValuedClients"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "Axceltrees Consulting Private Limited | Contact Us",
      "first_heading": "ContactUs"
    }
  },
  {
    "path": "css/4ba1f7eeea678c518b19a8a229705620.css",
    "context": {
      "path": "css/4ba1f7eeea678c518b19a8a229705620.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/7e610f95a2d26c26bc901487cdcd9a1c.css",
    "context": {
      "path": "css/7e610f95a2d26c26bc901487cdcd9a1c.css"
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
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "current-openings.html",
    "context": {
      "title": "Axceltrees Consulting Private Limited | Current Openings",
      "first_heading": "JobOpenings"
    }
  },
  {
    "path": "imgs/04cd26a7e71848a5ebf8e88a2669b63b.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/070ed646558da3da19a707394dc69bd7.webp",
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
    "path": "imgs/09494708796a6cd79f1a7c78aafb230f.webp",
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
    "path": "imgs/154862472992a4663ecf351678c46711.webp",
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
    "path": "imgs/19377ee0a9f33c81d4ceb399397bc65e.webp",
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
    "path": "imgs/1abb81b8849e5fd1024b7795f65a1a21.webp",
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
    "path": "imgs/1c02aaf7c79df18ce4b0e738887a9aec.webp",
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
    "path": "imgs/20b26ec637afc801c8372efe4eee3b03.webp",
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
    "path": "imgs/22d3c55d7a04b1a5c625424da7ce4009.webp",
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
    "path": "imgs/239356a53d0fa07bb8e3c315c2974a5d.webp",
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
    "path": "imgs/27e777f6312d5ac4c499abae54db3e03.webp",
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
        },
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
    "path": "imgs/2de9b93a3c6e9f86c9759fa9905bd3cb.webp",
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
    "path": "imgs/305e5eedf0fdef46289053bebd02766d.webp",
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
    "path": "imgs/367d6b6a1de009455ae538208b82d7d0.webp",
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
    "path": "imgs/371cd9c4752fd50d6a72cd0cba994035.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/38177a6b30d456b6eb5a3e851f660255.webp",
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
    "path": "imgs/3e39582987706d41db721482687f8a62.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/3e3c4e37e3ef6279950ee74ebc663334.webp",
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
    "path": "imgs/4199fbafedd05089baa5c9ea460c1dd1.webp",
    "context": {
      "refs": [
        {
          "alt": "Who we are",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4bf392c4c0b57a1e9fda554fd3fb94b3.webp",
    "context": {
      "refs": [
        {
          "alt": "m",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5507e24ff2a669abd50667cbdcfd9523.webp",
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
    "path": "imgs/5580cf274b7113c63b709b58acfbbb74.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
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
    "path": "imgs/5d99add62e22870ec8926243c2e765f3.webp",
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
    "path": "imgs/5ee1e23c9fe23ba9d690e1133b8c07a3.webp",
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
    "path": "imgs/5f2e93d5393bc33a1db5abc816241466.webp",
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
    "path": "imgs/6012b9755c9a091114b0fb83368af466.webp",
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
    "path": "imgs/6546751b074e89e23e55d4a787e40a05.webp",
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
    "path": "imgs/6749bdb84cb13fa89bb15ff9f0abbec0.webp",
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
    "path": "imgs/6af1f8a88757f25e276ecdadcaaee9c2.webp",
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
    "path": "imgs/6c6c62cd0ac10045a3fae30186ebe77d.webp",
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
    "path": "imgs/7301afaa5b3a0507b7c413e2ef1a551b.webp",
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
    "path": "imgs/742bfed4c3cdc83b3b43d53bcf5f8f6b.webp",
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
    "path": "imgs/744bb94757361f6bfc99d1c02533bcd0.webp",
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
    "path": "imgs/778ce088b476a3490d58caa02448e0e9.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/79942dc7cbce4efe35183443de0e8e3a.webp",
    "context": {
      "refs": [
        {
          "alt": "Shankar Ganesh",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7a59cb4aaf89ec727287130a5328fd5a.webp",
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
    "path": "imgs/7a9738d78d30f7afa8b23f57975fb6af.webp",
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
    "path": "imgs/7d3e1fe3718f9dbb4eb719a481151572.webp",
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
    "path": "imgs/7e525478890b692b12d66ee5a3528f75.webp",
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
    "path": "imgs/7ecac4fdd2cefa6f543b0a1588deb965.webp",
    "context": {
      "refs": [
        {
          "alt": "Malini M",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/84af3cb8f7fefddc28e22b63d6ed0d88.webp",
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
    "path": "imgs/86270784ff9671d14018cd18dadfc2de.webp",
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
    "path": "imgs/89bc825e2ac3e2325239aa6c91e22197.webp",
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
    "path": "imgs/8bcf2d78e66682f1940255acb714bd96.webp",
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
    "path": "imgs/92d414ecb0da902249c4d124a1527e56.webp",
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
    "path": "imgs/96a80aa7d0c8c42de9265503923c46a0.webp",
    "context": {
      "refs": [
        {
          "alt": "Senthil Prabhu",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/98d048157833e846710898487cf450dc.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/9aba657ba0f027ffa3fad77f2e30459b.webp",
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
    "path": "imgs/9b0659d2f2ddc6e34fd303ed3fc1fa50.webp",
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
    "path": "imgs/a003bec498553dbd62f001869455c766.webp",
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
    "path": "imgs/a1a02fcebdf373f05f2e4abeab1dab73.webp",
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
    "path": "imgs/a39162bd7fa5c8bcc8570b79ad54cb76.webp",
    "context": {
      "refs": [
        {
          "alt": "Untitled314x400px1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a490f104164a21f043b30ed302f2b591.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/a4dbb39f4544f6cfdb182f9ee2d92d42.webp",
    "context": {
      "refs": [
        {
          "alt": "IMG202204141757122",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0c8907a207ef4c973650a96841e50f0.webp",
    "context": {
      "refs": [
        {
          "alt": "Lavanya A",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0dc1228f2c289cb6d03084943206cf0.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b12cabdce2e8074d4193e0c4be85bc57.webp",
    "context": {
      "refs": [
        {
          "alt": "Why us",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b28f1d75ab82313c66f09f50360a009b.webp",
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
    "path": "imgs/b563ff1beea39d1d8144f614cccfe7fc.webp",
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
    "path": "imgs/b5721aca08135b6e061e17fae4016faa.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/b96a9f845a4b36780384ea135d10534b.webp",
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
    "path": "imgs/b9832ce1e3dabce86326d05cacb89f43.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/bc26b60905a3cde8bd01d4872187a47a.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/be7b3ee99b12fa939c35a0e1c9b6c367.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/c1ec2177520de19f711646ff95f865e6.svg",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/ca09686cc324ea688ab674d5ed3ecfa6.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20220414at52527PM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca70cf88de72ec12cd8b8b1d5fcba198.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/cc70cb7f99df780c5552991d88563e06.webp",
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
    "path": "imgs/d2efbe316fde22a828724bf18932d290.webp",
    "context": {
      "refs": [
        {
          "alt": "s",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d491f2bdf62783ea17bf9d13812df811.webp",
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
    "path": "imgs/d562a25dfba3042b9c6eeb8737442baf.webp",
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
    "path": "imgs/d6b92de0d6351ce86070baff2dd7e1b6.webp",
    "context": {
      "refs": [
        {
          "alt": "vinodanew",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d70c2c5275ac19601c69aaf789c403c4.webp",
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
    "path": "imgs/d9df8ee710ee282fc2042a46a26809e9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
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
    "path": "imgs/e047cd945011fb707d13a1d34f774a96.webp",
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
    "path": "imgs/e668af8bcce3062674f0e0241939f4db.webp",
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
    "path": "imgs/e6d7a27a3d085244aac375ebab280678.webp",
    "context": {
      "refs": [
        {
          "alt": "kavitha",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e97f19afacb7e4caef6880cc3012fc5e.webp",
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
    "path": "imgs/eaca3e6a6fdf4420cfa81d466235dfe9.webp",
    "context": {
      "refs": [
        {
          "alt": "S N Sampath Chandra",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ee8e83991fc749aa815da778539eaf28.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/f4ef8c669a86a474cca204537e8998ab.webp",
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
    "path": "imgs/f563760e5676173d928b1bb2a62b4102.webp",
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
    "path": "imgs/f6b7051c4b32b43d49dd79735028066a.webp",
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
    "path": "imgs/f81476f4a023e1c53744a22f9f9d3281.webp",
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
    "path": "imgs/fde2806fcfe98dc24f844681d8b91c8b.webp",
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
    "path": "imgs/fe21c28f66ec8157cfd9f6c88e39631e.webp",
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
    "path": "index.html",
    "context": {
      "title": "Axceltrees Consulting Private Limited | Finding the Perfect Job Only Got Easier",
      "first_heading": "Finding the Perfect Job Only Got Easier!"
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
    "path": "js/9ee3d668722ae3803ab34e5eb37f86a2.js",
    "context": {
      "path": "js/9ee3d668722ae3803ab34e5eb37f86a2.js"
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