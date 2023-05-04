# Sanaa ya Kuunda Programu za Kuhuisha

Siku ya 30 ya leo ya changamoto ya *#Siku30ZaKufululiza*. Hongera kwa kufikia hatua hii katika changamoto.

Katika mafunzo haya, tutaweka maarifa yetu mapya kutoka kwa changamoto hii ya kujifunza ili kuunda programu za Kuhuisha ili kutatua tatizo la ulimwengu halisi.

## Tatizo la ulimwengu halisi

Kama mtayarishaji wa maudhui, kuwa na ufikiaji wa vijipicha kutoka kwa video za YouTube ni nyenzo muhimu kwa ukuzaji wa kijamii na kuunda maudhui.

Hebu tujue jinsi tutakavyotatua tatizo hili na kuunda programu ya Kuhuisha.

##Suluhisho

Leo, tutaunda `yt-img-app`, ambayo ni programu ya Kuhuisha ambayo inaweza kutoa picha za vijipicha kutoka kwa video za YouTube.

Kwa kifupi, hizi hapa ni hatua 3 rahisi ambazo tunataka programu ya Kuhuisha ifanye:

1. Kubali URL ya YouTube kama ingizo kutoka kwa watumiaji
2. Tekeleza uchakataji wa maandishi wa URL ili kutoa kitambulisho cha kipekee cha video ya YouTube
3. Tumia Kitambulisho cha video cha YouTube kama ingizo la utendaji maalum unaorejesha na kuonyesha picha ya kijipicha kutoka kwa video za YouTube.

##Maelekezo

Ili kuanza kutumia programu ya Kuhuisha, nakili na ubandike URL ya YouTube kwenye kisanduku cha maandishi.

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/yt-img-app/)

##Msimbo
Hivi ndivyo jinsi ya kuunda programu ya `yt-img-app` Kuhuisha:
``` chatu
import streamt kama st

st.title('🖼️ yt-img-programu')
st.header('Programu ya Kichujio cha Picha cha Kijipicha cha YouTube')

na st.expander('Kuhusu programu hii'):
  st.write('Programu hii hurejesha picha ya kijipicha kutoka kwa video ya YouTube.')
  
# Mipangilio ya picha
st.sidebar.header('Mipangilio')
img_dict = {'Max': 'maxresdefault', 'Juu': 'hqdefault', 'Medium': 'mqdefault', 'Standard': 'sddefault'}
selected_img_quality = st.sidebar.selectbox('Chagua ubora wa picha', ['Upeo', 'Juu', 'Wastani', 'Standard'])
img_quality = img_dict[selected_img_quality]

yt_url = st.text_input('Bandika URL ya YouTube', 'https://youtu.be/JwSS70SZdyM')

def get_ytid(input_url):
  ikiwa 'youtu.be' kwenye input_url:
    ytid = input_url.split('/')[-1]
  ikiwa 'youtube.com' katika input_url:
    ytid = input_url.split('=')[-1]
  kurudi ytid
    
# Onyesha kijipicha cha YouTube
ikiwa yt_url != '':
  ytid = get_ytid(yt_url) # yt au yt_url

  yt_img = f'http://img.youtube.com/vi/{ytid}/{img_quality}.jpg'
  picha ya st.(yt_img)
  st.write('URL ya kijipicha cha video ya YouTube: ', yt_img)
kwingine:
  st.write('☝️ Weka URL ili kuendelea ...')
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
```

Kisha, tunaonyesha kichwa cha programu na kichwa kinachoandamana:
``` chatu
st.title('🖼️ yt-img-programu')
st.header('Programu ya Kichujio cha Picha cha Kijipicha cha YouTube')
```
Tukiwa tunafanya hivyo, tunaweza pia kutupa kisanduku cha Kuhusu kinachoweza kupanuka.
``` chatu
na st.expander('Kuhusu programu hii'):
  st.write('Programu hii hurejesha picha ya kijipicha kutoka kwa video ya YouTube.')
 
Hapa, tunaunda kisanduku cha uteuzi kwa kukubali ingizo la mtumiaji kwenye ubora wa picha ya kutumia.
``` chatu
# Mipangilio ya picha
st.sidebar.header('Mipangilio')
img_dict = {'Max': 'maxresdefault', 'Juu': 'hqdefault', 'Medium': 'mqdefault', 'Standard': 'sddefault'}
selected_img_quality = st.sidebar.selectbox('Chagua ubora wa picha', ['Upeo', 'Juu', 'Wastani', 'Standard'])
img_quality = img_dict[selected_img_quality]
```

Kisanduku cha maandishi cha ingizo kinaonyeshwa ili kukubali ingizo la mtumiaji kwenye URL ya video ya YouTube ili kutumia kutoa picha kutoka.
``` chatu
yt_url = st.text_input('Bandika URL ya YouTube', 'https://youtu.be/JwSS70SZdyM')
```

Chaguo maalum la kufanya usindikaji wa maandishi wa URL ya ingizo.
``` chatu
def get_ytid(input_url):
  ikiwa 'youtu.be' kwenye input_url:
    ytid = input_url.split('/')[-1]
  ikiwa 'youtube.com' katika input_url:
    ytid = input_url.split('=')[-1]
  kurudi ytid
```

Hatimaye, tunatumia udhibiti wa mtiririko ili kubaini ikiwa tuonyeshe kikumbusho cha kuingiza URL (yaani kama katika taarifa `nyingine`) au kuonyesha kijipicha cha YouTube (yaani kama katika taarifa ya `kama`).
``` chatu
# Onyesha kijipicha cha YouTube
ikiwa yt_url != '':
  ytid = get_ytid(yt_url) # yt au yt_url

  yt_img = f'http://img.youtube.com/vi/{ytid}/{img_quality}.jpg'
  picha ya st.(yt_img)
  st.write('URL ya kijipicha cha video ya YouTube: ', yt_img)
kwingine:
  st.write('☝️ Weka URL ili kuendelea ...')
```

## Muhtasari

Kwa muhtasari, tumeona kwamba katika uundaji wa programu yoyote ya Kuhuisha, kwa kawaida tunaanza kwa kutambua na kufafanua tatizo kwanza. Ifuatayo, tunatengeneza suluhisho la kukabiliana na tatizo kwa kulivunja katika hatua za punjepunje, ambazo tunatekeleza katika programu ya Kuhuisha.

Hapa, tunapaswa pia kubainisha ni data au taarifa gani tunayohitaji kama ingizo kutoka kwa watumiaji, mbinu na mbinu ya kutumia katika kuchakata ingizo la mtumiaji ili kutoa matokeo ya mwisho tunayotaka.

Natumai ulifurahia mafunzo haya, Furaha ya Kufululiza!
