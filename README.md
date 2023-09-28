# mister-worldwide
Consumes a single word. Produces a gif of that word translating between many languages.
![Alt text](output.gif)

Basic 

```
python3 mr-worldwide.py --size "256,256" --text hello! --font_path fonts/arial.ttf --font_color "256,32,32" --background_color "256,256,256" --languages all --delay 300
```

Intermediate Examples
```
TEXT ARRAY:

python3 mr-worldwide.py --size "1024,256" --text_array "你好, Hola, Hello, नमस्ते, السلام عليكم, হ্যালো, Olá, Привет, こんにちは, ਸਤ ਸ੍ਰੀ ਅਕਾਲ, Hallo, Halo, 呵呵, హలో, Xin chào, नमस्कार, 안녕하세요, Bonjour, வணக்கம், Merhaba, اسلام و علیکم, 哈囉, สวัสดี, નમસ્તે, Pronto" --font_path fonts/arial.ttf --font_color "0,0,0" --font_size=32 --background_color "256,256,256" --languages all --delay 300
```

```
SINUSOIDAL:

python3 mr-worldwide.py --size "256,256" --text hello! --font_path fonts/arial.ttf --font_color "256,32,32" --background_color "256,256,256" --languages all --delay sine:"500,100" 

```




``` TODO
--round_robin true #true or false
--background_images #list of image paths, stretched to fit box size, must equal number of languages
--smart_color_picker (from background, highest maximal contrast, <3)
```

**round-robin-sinosoidal**
Start at A_0, emphasizing for interval-ms time, then cycle through all other options until A_1 for interval-ms time, then A_2, and so on.
Come to think of it, it's a misnomer : it's more a piecewise saw-tooth function.
