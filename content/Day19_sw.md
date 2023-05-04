# Jinsi ya kupanga programu yako ya Uboreshaji

Katika somo hili, tutatumia amri zifuatazo kupanga programu yetu ya Kuhuisha:
- `st.set_page_config(layout="wide")` - Huonyesha yaliyomo kwenye programu katika hali pana (vinginevyo kwa chaguo-msingi, yaliyomo yamewekwa kwenye kisanduku cha upana usiobadilika.
- `st.sidebar` - Huweka wijeti au maonyesho ya maandishi/picha kwenye upau wa kando.
- `st.expander` - Huweka maonyesho ya maandishi/picha ndani ya kisanduku cha kontena kinachoweza kukunjwa.
- `st.columns` - Huunda nafasi ya jedwali (au safu wima) ambamo yaliyomo yanaweza kuwekwa ndani.

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/streamlit-layout/)

##Msimbo
Hivi ndivyo jinsi ya kubinafsisha mpangilio wa programu yako ya Kuhuisha:
``` chatu
import streamt kama st

st.set_page_config(layout="wide")

st.title('Jinsi ya kupanga programu yako ya Kuhuisha')

na st.expander('Kuhusu programu hii'):
  st.write('Programu hii inaonyesha njia mbalimbali za jinsi unavyoweza kupanga programu yako ya Kuhuisha.')
  st.image('https://streamlit.io/images/brand/streamlit-logo-secondary-colormark-darktext.png', width=250)

st.sidebar.header('Ingizo')
user_name = st.sidebar.text_input('Jina lako ni nani?')
user_emoji = st.sidebar.selectbox('Chagua emoji', ['', '😄', '😆', '😊', '😍', '😴', '😕', '😱'])
user_food = st.sidebar.selectbox('Chakula gani unachokipenda zaidi ni nini?', ['', 'Tom Yum Kung', 'Burrito', 'Lasagna', 'Hamburger', 'Pizza'])

st.header('Pato')

col1, col2, col3 = safu wima(3)

na col1:
  kama user_name != '':
    st.write(f'👋 Hujambo {user_name}!')
  kwingine:
    st.write('👈 Tafadhali weka **jina** lako!')

na col2:
  ikiwa mtumiaji_emoji != '':
    st.write(f'{user_emoji} ndio **emoji**!')
  kwingine:
    st.write('👈 Tafadhali chagua **emoji**!')

na col3:
  ikiwa user_food != '':
    st.write(f'🍴 **{user_food}** ndicho **chakula** chako unachokipenda!')
  kwingine:
    st.write('👈 Tafadhali chagua **chakula** chako unachopenda!')
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
```

Tutaanza kwa kufafanua kwanza mpangilio wa ukurasa utakaoonyeshwa katika hali `pana`, ambayo inaruhusu maudhui ya ukurasa kupanuka hadi upana wa kivinjari.
``` chatu
st.set_page_config(layout="wide")
```

Kisha, tutaipa programu ya Streamlit jina.
``` chatu
st.title('Jinsi ya kupanga programu yako ya Kuhuisha')
```

Kisanduku kinachoweza kupanuliwa kiitwacho `Kuhusu programu hii` kimewekwa chini ya kichwa cha programu. Baada ya upanuzi, tutaona maelezo ya ziada ndani.
``` chatu
na st.expander('Kuhusu programu hii'):
  st.write('Programu hii inaonyesha njia mbalimbali za jinsi unavyoweza kupanga programu yako ya Kuhuisha.')
  st.image('https://streamlit.io/images/brand/streamlit-logo-secondary-colormark-darktext.png', width=250)
```

Wijeti za ingizo za kukubali ingizo la mtumiaji huwekwa kwenye upau wa kando kama ilivyobainishwa kwa kutumia amri ya `st.sidebar` kabla ya amri za Kufululiza `ingizo_maandishi` na `kisanduku cha kuchagua`. Nambari za ingizo zilizowekwa au zilizochaguliwa na mtumiaji hukabidhiwa na kuhifadhiwa katika vigeu vya `jina_la_mtumiaji`, `mtumiaji_emoji` na `chakula_cha mtumiaji`.
``` chatu
st.sidebar.header('Ingizo')
user_name = st.sidebar.text_input('Jina lako ni nani?')
user_emoji = st.sidebar.selectbox('Chagua emoji', ['', '😄', '😆', '😊', '😍', '😴', '😕', '😱'])
user_food = st.sidebar.selectbox('Chakula gani unachokipenda zaidi ni nini?', ['', 'Tom Yum Kung', 'Burrito', 'Lasagna', 'Hamburger', 'Pizza'])
```

Hatimaye, tutaunda safu wima 3 kwa kutumia amri ya `st.columns` ambayo inalingana na `col1`, `col2` na `col3`. Kisha, tunagawa yaliyomo kwa kila safu kwa kuunda vizuizi vya msimbo mahususi kwa kuanzia na taarifa ya `na`. Chini ya hili, tunaunda taarifa za masharti zinazoonyesha maandishi mbadala 1 kati ya 2 kulingana na ikiwa mtumiaji ametoa data yake ya ingizo (iliyobainishwa kwenye utepe) au la. Kwa chaguo-msingi, ukurasa unaonyesha maandishi chini ya taarifa `nyingine`. Baada ya kutoa ingizo la mtumiaji, maelezo yanayolingana ambayo mtumiaji hutoa kwa programu yanaonyeshwa chini ya maandishi ya kichwa cha `Pato`.
``` chatu
st.header('Pato')

col1, col2, col3 = safu wima(3)

na col1:
  kama user_name != '':
    st.write(f'👋 Hujambo {user_name}!')
  kwingine:
    st.write('👈 Tafadhali weka **jina** lako!')

na col2:
  ikiwa mtumiaji_emoji != '':
    st.write(f'{user_emoji} ndio **emoji**!')
  kwingine:
    st.write('👈 Tafadhali chagua **emoji**!')

na col3:
  ikiwa user_food != '':
    st.write(f'🍴 **{user_food}** ndicho **chakula** chako unachokipenda!')
  kwingine:
    st.write('👈 Tafadhali chagua **chakula** chako unachopenda!')
```
Inastahili pia kutambua kwamba mifuatano ya `f` ilitumiwa kuchanganya maandishi yaliyowekwa kwenye mikebe ya awali pamoja na thamani zilizotolewa na mtumiaji.

## Kusoma zaidi
- [Miundo na Vyombo](https://docs.streamlit.io/library/api-reference/layout)
