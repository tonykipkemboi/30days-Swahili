# Sanaa ya Kuunda Programu za Streamlit

Siku ya 30 ya leo ya changamoto ya *#Siku30ZaKufululiza*. Hongera kwa kufikia hatua hii katika changamoto.

Katika mafunzo haya, tutaweka maarifa yetu mapya kutoka kwa changamoto hii ya kujifunza ili kuunda programu za Streamlit ili kutatua tatizo la ulimwengu halisi.

## Tatizo la ulimwengu halisi

Kama mtayarishaji wa maudhui, kuwa na ufikiaji wa vijipicha kutoka kwa video za YouTube ni nyenzo muhimu kwa ukuzaji wa kijamii na kuunda maudhui.

Hebu tujue jinsi tutakavyotatua tatizo hili na kuunda programu ya Streamlit.

##Suluhisho

Leo, tutaunda `yt-img-app`, ambayo ni programu ya Streamlit ambayo inaweza kutoa picha za vijipicha kutoka kwa video za YouTube.

Kwa kifupi, hizi hapa ni hatua 3 rahisi ambazo tunataka programu ya Streamlit ifanye:

1. Kubali URL ya YouTube kama ingizo kutoka kwa watumiaji
2. Tekeleza uchakataji wa maandishi wa URL ili kutoa kitambulisho cha kipekee cha video ya YouTube
3. Tumia Kitambulisho cha video cha YouTube kama ingizo la utendaji maalum unaorejesha na kuonyesha picha ya kijipicha kutoka kwa video za YouTube.

##Maelekezo

Ili kuanza kutumia programu ya Streamlit, nakili na ubandike URL ya YouTube kwenye kisanduku cha maandishi.

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/yt-img-app/)

##Msimbo
Hivi ndivyo jinsi ya kuunda programu ya `yt-img-app` Streamlit:
``` Python
import streamlit as st

st.title('🖼️ yt-img-app')
st.header('YouTube Thumbnail Image Extractor App')

with st.expander('About this app'):
  st.write('This app retrieves the thumbnail image from a YouTube video.')
  
# Image settings
st.sidebar.header('Settings')
img_dict = {'Max': 'maxresdefault', 'High': 'hqdefault', 'Medium': 'mqdefault', 'Standard': 'sddefault'}
selected_img_quality = st.sidebar.selectbox('Select image quality', ['Max', 'High', 'Medium', 'Standard'])
img_quality = img_dict[selected_img_quality]

yt_url = st.text_input('Paste YouTube URL', 'https://youtu.be/JwSS70SZdyM')

def get_ytid(input_url):
  if 'youtu.be' in input_url:
    ytid = input_url.split('/')[-1]
  if 'youtube.com' in input_url:
    ytid = input_url.split('=')[-1]
  return ytid
    
# Display YouTube thumbnail image
if yt_url != '':
  ytid = get_ytid(yt_url) # yt or yt_url

  yt_img = f'http://img.youtube.com/vi/{ytid}/{img_quality}.jpg'
  st.image(yt_img)
  st.write('YouTube video thumbnail image URL: ', yt_img)
else:
  st.write('☝️ Enter URL to continue ...')
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Streamlit ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` Python
import streamlit as st
```

Kisha, tunaonyesha kichwa cha programu na kichwa kinachoandamana:
``` Python
st.title('🖼️ yt-img-app')
st.header('YouTube Thumbnail Image Extractor App')
```
Tukiwa tunafanya hivyo, tunaweza pia kutupa kisanduku cha Kuhusu kinachoweza kupanuka.
``` Python
with st.expander('About this app'):
  st.write('This app retrieves the thumbnail image from a YouTube video.')
```
Hapa, tunaunda kisanduku cha uteuzi kwa kukubali ingizo la mtumiaji kwenye ubora wa picha ya kutumia.
```python
# Image settings
st.sidebar.header('Settings')
img_dict = {'Max': 'maxresdefault', 'High': 'hqdefault', 'Medium': 'mqdefault', 'Standard': 'sddefault'}
selected_img_quality = st.sidebar.selectbox('Select image quality', ['Max', 'High', 'Medium', 'Standard'])
img_quality = img_dict[selected_img_quality]
```

Kisanduku cha maandishi cha ingizo kinaonyeshwa ili kukubali ingizo la mtumiaji kwenye URL ya video ya YouTube ili kutumia kutoa picha kutoka.
``` Python
yt_url = st.text_input('Paste YouTube URL', 'https://youtu.be/JwSS70SZdyM')
```

Chaguo maalum la kufanya usindikaji wa maandishi wa URL ya ingizo.
``` Python
def get_ytid(input_url):
  if 'youtu.be' in input_url:
    ytid = input_url.split('/')[-1]
  if 'youtube.com' in input_url:
    ytid = input_url.split('=')[-1]
  return ytid
```

Hatimaye, tunatumia udhibiti wa mtiririko ili kubaini ikiwa tuonyeshe kikumbusho cha kuingiza URL (yaani kama katika taarifa `nyingine`) au kuonyesha kijipicha cha YouTube (yaani kama katika taarifa ya `kama`).
``` Python
# Display YouTube thumbnail image
if yt_url != '':
  ytid = get_ytid(yt_url) # yt or yt_url

  yt_img = f'http://img.youtube.com/vi/{ytid}/{img_quality}.jpg'
  st.image(yt_img)
  st.write('YouTube video thumbnail image URL: ', yt_img)
else:
  st.write('☝️ Enter URL to continue ...')
```

## Muhtasari

Kwa muhtasari, tumeona kwamba katika uundaji wa programu yoyote ya Streamlit, kwa kawaida tunaanza kwa kutambua na kufafanua tatizo kwanza. Ifuatayo, tunatengeneza suluhisho la kukabiliana na tatizo kwa kulivunja katika hatua za punjepunje, ambazo tunatekeleza katika programu ya Streamlit.

Hapa, tunapaswa pia kubainisha ni data au taarifa gani tunayohitaji kama ingizo kutoka kwa watumiaji, mbinu na mbinu ya kutumia katika kuchakata ingizo la mtumiaji ili kutoa matokeo ya mwisho tunayotaka.

Natumai ulifurahia mafunzo haya, furahia Streamlit-ing!
