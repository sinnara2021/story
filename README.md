  ### sinnara2021/story
  =============
  # ๐ฉ๐ป ์ ๋๋ผ์์ ์ฑ๋ด ์ ์ ์คํ ๋ฆฌ๋ฐฉ
  
  https://user-images.githubusercontent.com/79739569/132930276-0eaae252-dcd3-40b2-bbb3-f4e614c4bc3e.jpg
  -------------
   ### ์ฑ๋ด์ฝ์ default ํ์ด์ง ๋ง๋๋ ๊ฒฝ๋ก
  _layouts/default.html
![image](https://user-images.githubusercontent.com/79739569/132869335-d9c5560a-0ad6-445f-ad58-91427fcf1372.png)
<hr/>

   ### ์ฑ๋ด์ฝ์ ์์ค์ฝ๋
  ์ฑ๋ด ์ฝ์ ์์ค ์ฝ๋๋ default.html ํ์ด์ง ์ด์ด๋ณด๊ธฐ!
  <hr/>

  ### ์ฌ๋ฌ๊ฐ์ง ์๋ต ๋ง๋ค๊ธฐ
  '''
  Responses
  
  Custom Payload
  
  1. Description type :  
  Intents ์ด๋ฆ: richDes   
  Training phrases : ๋ฆฌ์น์ค๋ช
  

  {
    "richContent": [
     [
       {
         "title": "์ ๋ฑ ๋ฆฌ์คํธ",
         "type": "description",
         "text": [
           "์๋ฐฉ์ ๋ฑ",
            "๊ฑฐ์ค์ ๋ฑ"
          ]
        }
     ]
    ]
  }

2. Info type
Intents ์ด๋ฆ:  richInfo  
Training phrases : ๋ฆฌ์น์ ๋ณด


{
  "richContent": [
    [
      {
        "type": "info",
        "title": "์ ๋ชฉ",
        "subtitle": "๋ถ์ ๋ชฉ",
        "image": {
          "src": {
            "rawUrl": "http://117.16.177.40/image/i2r_small.png"
          }
        },
        "actionLink":"https://i2r.link"
      }
    ]
  ]
}

3. Image type
Intents ์ด๋ฆ:  richImage 
Training phrases : ๋ฆฌ์น๊ทธ๋ฆผ


{
  "richContent": [
    [
      {
        "type": "image",
        "accessibilityText":"MBD Image",
        "rawUrl": "http://117.16.177.40/image/sunset.jpg"
      }
    ]
  ]
}

4. Button type
Intents ์ด๋ฆ:  richButton 
Training phrases : ๋ฆฌ์น๋ฒํผ


{
  "richContent": [
    [
      {
        "link":"https://sinnara2021.github.io/chatbot/",
        "text": "Go to Idea to Real",
        "icon": {
          "type":"link",
          "color":"#FF9800"
        },
        "type": "button"
      }
    ]
  ]
}

5. Suggestion Chips
Intents ์ด๋ฆ:  richSuggestion  
Training phrases : ๋ฆฌ์น์ ํ

{
  "richContent": [
    [
      {
        "type":"chips",
        "options": [
          {
            "text":"yes"
          },
          {
            "text":"no"
          }
        ]
      }
    ]
  ]
}

6. List Response Type
Intents ์ด๋ฆ:  richList 
Training phrases : ๋ฆฌ์น๋ฆฌ์คํธ

{
  "richContent": [
    [
      {
        "title":"List item 1 title",
        "subtitle":"List Item 1 subtitle",
        "type":"list",
        "event": {
          "parameters":{},
          "name":"WELCOME",
          "languageCode":"en"
        }
      },
      {
        "type":"divider"
      },
      {
        "title":"List item 2 title",
        "subtitle":"List Item 2 subtitle",
        "type":"list",
        "event": {
          "parameters":{},
          "name":"PARALLEL",
          "languageCode":"en"
        }
      }
    ]
  ]
}



'''
<hr/>
### ๋งํฌ๋ค์ด ๋ฌธ๋ฒ ์์๋ณด๊ธฐ

https://www.dropbox.com/s/mzp9tq4qtfjdlif/20141021_markdown_use_tip.md?dl=0


# ์ ๋ชฉ 1
## ์ ๋ชฉ 2
### ์ ๋ชฉ 3
#### ์ ๋ชฉ 4
##### ์ ๋ชฉ 5
###### ์ ๋ชฉ 6
![image](https://user-images.githubusercontent.com/79739569/132870001-c4b88bfd-9b9e-4b67-bfed-043fea45a258.png)


![image](https://user-images.githubusercontent.com/79739569/132870090-11936485-fcde-42c5-a8d2-2264f2234c86.png)
์ดํ๋ฆญ์ฒด๋ *๋ณํ(asterisks)* ํน์ _์ธ๋๋ฐ(underscore)_๋ฅผ ์ฌ์ฉํ์ธ์. 
๋๊ป๊ฒ๋ **๋ณํ(asterisks)** ํน์ __์ธ๋๋ฐ(underscore)__๋ฅผ ์ฌ์ฉํ์ธ์.
**_์ดํ๋ฆญ์ฒด_์ ๋๊ป๊ฒ**๋ฅผ ๊ฐ์ด ์ฌ์ฉํ  ์ ์์ต๋๋ค. 
์ทจ์์ ์ ~~๋ฌผ๊ฒฐํ์(tilde)~~๋ฅผ ์ฌ์ฉํ์ธ์. 
<u>๋ฐ์ค</u>์ `<u></u>`๋ฅผ ์ฌ์ฉํ์ธ์.
![image](https://user-images.githubusercontent.com/79739569/132870103-7018344a-c460-4348-ab27-3a2087db44e2.png)


[์ํธ๊ณ ์ฑ๋ด์ ์ ๊นํํ์ด์ง](https://yunsugyoung.github.io/talk/) 
![Image](https://cdn.pixabay.com/photo/2017/06/10/07/21/chat-2389223__340.png)
![image](https://user-images.githubusercontent.com/79739569/132870129-bae6b843-b869-42d0-b655-bacd2650b6fb.png)


- - -
(Hyphens)
* * *
(Asterisks)
_ _ _
(Underscores)
![image](https://user-images.githubusercontent.com/79739569/132870150-e026b638-ff94-42c2-b9ea-d0dbd05318fb.png)

| ๊ฐ | ์๋ฏธ | ๊ธฐ๋ณธ๊ฐ |
|---|:---:|---:|
| `static` | ์ ํ(๊ธฐ์ค) ์์ / ๋ฐฐ์น ๋ถ๊ฐ๋ฅ | `static` |
| `relative` | ์์ ์์ ์ ๊ธฐ์ค์ผ๋ก ๋ฐฐ์น |  |
| `absolute` | ์์น ์ ๋ถ๋ชจ(์กฐ์)์์๋ฅผ ๊ธฐ์ค์ผ๋ก ๋ฐฐ์น |  |
| `fixed` | ๋ธ๋ผ์ฐ์  ์ฐฝ์ ๊ธฐ์ค์ผ๋ก ๋ฐฐ์น |  |
![image](https://user-images.githubusercontent.com/79739569/132870166-0c3659b6-3632-48ce-9fff-c72e8c25aeb8.png)

![image](https://user-images.githubusercontent.com/79739569/132870206-ac78a972-7076-4d3f-ab36-bdbf2f3f9fed.png)
