# kitufe

`st.button` huruhusu onyesho la wijeti ya kitufe.

## Tunajenga nini?

Programu rahisi inayofanya kazi huchapisha kwa masharti ujumbe mbadala kulingana na kama kitufe kilibonyezwa au la.

Mtiririko wa programu:

1. Kwa chaguo-msingi, programu huchapisha `Kwaheri`
2. Baada ya kubofya kitufe, programu huonyesha ujumbe mbadala `Kwa nini hujambo`

## Programu ya onyesho

Programu ya Kuhuisha iliyotumika inapaswa kuonekana kama ile iliyoonyeshwa kwenye kiungo kilicho hapa chini:

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.button/)

## Msimbo

Hapa kuna nambari ya kutekeleza programu iliyotajwa hapo juu:

```bash
import streamlit as st

st.header('st.button')

if st.button('Sema hujambo'):
     st.write('Kwa nini hujambo')
else:
     st.write('Kwaheri')
```

## Maelezo ya mstari kwa mstari

Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:

```bash
import streamt kama st
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:

```bash
st.header('st.button')
```

Ifuatayo, tutatumia kauli za masharti `if` na `engine` kwa kuchapisha ujumbe mbadala.

```bash
if st.button('Sema hujambo'):
     st.write('Kwa nini hujambo')
else:
     st.write('Kwaheri')
```

Kama tunavyoweza kuona kwenye kisanduku cha msimbo kilicho hapo juu, amri ya `st.button()` inakubali hoja ya ingizo ya `lebo` ya `Sema hello`, ambayo ni maandishi ambayo kitufe kinaonyesha.

Amri ya `st.write` hutumika kuchapisha ujumbe wa maandishi wa ama `Kwa nini hujambo` au `Kwaheri` kutegemeana na kama kitufe kilibofya au la, ambacho kinatekelezwa kupitia:

```bash
st.write('Kwa nini hujambo')
```

na

```bash
st.write('Kwaheri')
```

Ni muhimu kutambua kwamba taarifa za `st.write` zimewekwa chini ya masharti ya `if` na `engine` ili kutekeleza mchakato uliotajwa hapo juu wa uonyeshaji mbadala wa ujumbe.

## Hatua zinazofuata

Kwa kuwa sasa umeunda programu ya Kuhuisha ndani ya nchi, ni wakati wa kuipeleka kwenye [Streamlit Community Cloud](https://streamlit.io/cloud) kama itakavyoelezwa hivi karibuni katika shindano lijalo.

Kwa sababu hii ni wiki ya kwanza ya changamoto yako, tunatoa msimbo kamili (kama inavyoonyeshwa kwenye kisanduku cha msimbo hapo juu) na suluhisho (programu ya onyesho) ndani ya ukurasa huu wa tovuti.

Kusonga mbele katika changamoto zinazofuata, inashauriwa kuwa kwanza ujaribu kutekeleza programu ya Kuhuisha wewe mwenyewe.

Usijali ikiwa utakwama, unaweza kutazama suluhisho kila wakati.

## Marejeleo

Soma kuhusu [`st.button`](https://docs.streamlit.io/library/api-reference/widgets/st.button) katika Hati ya API ya Kuhuisha.
