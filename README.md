  ### sinnara2021/story
  =============
  # 👩🏻 신나라샘의 챗봇 제작 스토리방
  -------------
   ### 챗봇삽입 default 페이지 만드는 경로
  _layouts/default.html
![image](https://user-images.githubusercontent.com/79739569/132869335-d9c5560a-0ad6-445f-ad58-91427fcf1372.png)

   ### 챗봇삽입 소스코드
   '''
   <!DOCTYPE html>
<html lang="{{ site.lang | default: "en-US" }}">
  <head>
    
    
챗봇삽입

    
<style>
  df-messenger {
   --df-messenger-bot-message: #D6F7FC;
   --df-messenger-chat-background-color: #EFF6F6;
   --df-messenger-input-box-color: #EFF1F1;
   --df-messenger-font-color: black;
   --df-messenger-user-message: #FBF7B9;
  }
</style>
    
    {% if site.google_analytics %}
      <script async src="https://www.googletagmanager.com/gtag/js?id={{ site.google_analytics }}"></script>
      <script>
        window.dataLayer = window.dataLayer || [];
        function gtag(){dataLayer.push(arguments);}
        gtag('js', new Date());
        gtag('config', '{{ site.google_analytics }}');
      </script>
    {% endif %}
    <meta charset="UTF-8">

{% seo %}
    <link rel="preconnect" href="https://fonts.gstatic.com">
    <link rel="preload" href="https://fonts.googleapis.com/css?family=Open+Sans:400,700&display=swap" as="style" type="text/css" crossorigin>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="theme-color" content="#157878">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <link rel="stylesheet" href="{{ '/assets/css/style.css?v=' | append: site.github.build_revision | relative_url }}">
  </head>
  <body>
    <a id="skip-to-content" href="#content">Skip to the content.</a>

    <header class="page-header" role="banner">
      <h1 class="project-name">{{ page.title | default: site.title | default: site.github.repository_name }}</h1>
      <h2 class="project-tagline">{{ page.description | default: site.description | default: site.github.project_tagline }}</h2>
      {% if site.github.is_project_page %}
        <a href="{{ site.github.repository_url }}" class="btn">View on GitHub</a>
      {% endif %}
      {% if site.show_downloads %}
        <a href="{{ site.github.zip_url }}" class="btn">Download .zip</a>
        <a href="{{ site.github.tar_url }}" class="btn">Download .tar.gz</a>
      {% endif %}
    </header>

    <main id="content" class="main-content" role="main">
      {{ content }}

      <footer class="site-footer">
        {% if site.github.is_project_page %}
          <span class="site-footer-owner"><a href="{{ site.github.repository_url }}">{{ site.github.repository_name }}</a> is maintained by <a href="{{ site.github.owner_url }}">{{ site.github.owner_name }}</a>.</span>
        {% endif %}
        <span class="site-footer-credits">This page was generated by <a href="https://pages.github.com">GitHub Pages</a>.</span>
      </footer>
    </main>
  </body>
</html>
'''

  ### 여러가지 응답 만들기
  '''
  Responses
  
  Custom Payload
  
  1. Description type :  
  Intents 이름: richDes   
  Training phrases : 리치설명
  

  {
    "richContent": [
     [
       {
         "title": "전등 리스트",
         "type": "description",
         "text": [
           "안방전등",
            "거실전등"
          ]
        }
     ]
    ]
  }

2. Info type
Intents 이름:  richInfo  
Training phrases : 리치정보


{
  "richContent": [
    [
      {
        "type": "info",
        "title": "제목",
        "subtitle": "부제목",
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
Intents 이름:  richImage 
Training phrases : 리치그림


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
Intents 이름:  richButton 
Training phrases : 리치버튼


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
Intents 이름:  richSuggestion  
Training phrases : 리치선택

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
Intents 이름:  richList 
Training phrases : 리치리스트

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

### 마크다운 문법 알아보기

https://www.dropbox.com/s/mzp9tq4qtfjdlif/20141021_markdown_use_tip.md?dl=0





