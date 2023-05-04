kisanduku # cha kuchagua

`st.selectbox` inaruhusu onyesho la wijeti iliyochaguliwa.

## Tunajenga nini?

Programu rahisi inayomuuliza mtumiaji rangi anayoipenda zaidi ni ipi.

Mtiririko wa programu:
1. Mtumiaji anachagua rangi
2. Programu huchapisha rangi iliyochaguliwa

## Programu ya onyesho
Programu ya Kuhuisha iliyotumika inapaswa kuonekana kama ile iliyoonyeshwa kwenye kiungo kilicho hapa chini:

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.selectbox/)

##Msimbo
Hapa kuna nambari ya kutekeleza programu iliyotajwa hapo juu:
``` chatu
import streamt kama st

st.header('st.selectbox')

chaguo = st.selectbox(
     'Ni rangi gani unayoipenda zaidi?',
     ('Bluu', 'Nyekundu', 'Kijani'))

st.write('Rangi unayoipenda ni ', chaguo)
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:
``` chatu
st.header('st.selectbox')
```

Ifuatayo, tutaunda kigezo kiitwacho `chaguo` ambacho kitakubali ingizo la mtumiaji kwa njia ya wijeti ya ingizo ya **chagua** kupitia amri ya `st.selectbox()`.

``` chatu
chaguo = st.selectbox(
     'Ni rangi gani unayoipenda zaidi?',
     ('Bluu', 'Nyekundu', 'Kijani'))
```
Kama tunavyoona kwenye kisanduku cha msimbo hapo juu, amri ya `st.selectbox()` inakubali hoja 2 za ingizo:
1. Maandishi yanayoenda juu ya wijeti iliyochaguliwa, yaani, `'Ni rangi gani unayoipenda zaidi?'`
2. Thamani zinazowezekana za kuchagua kutoka `('Bluu', 'Nyekundu', 'Kijani')`

Hatimaye, tutachapisha rangi iliyochaguliwa kama ifuatavyo:
``` chatu
st.write('Rangi unayoipenda ni ', chaguo)
```

## Hatua zinazofuata
Kwa kuwa sasa umeunda programu ya Kuhuisha ndani ya nchi, ni wakati wa kuipeleka kwenye [Streamlit Community Cloud](https://streamlit.io/cloud).

##Marejeleo
Zaidi kuhusu [`st.selectbox`](https://docs.streamlit.io/library/api-reference/widgets/st.selectbox)
