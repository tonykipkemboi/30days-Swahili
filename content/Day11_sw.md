# st.multiselect

`st.multiselect` inaonyesha wijeti iliyochaguliwa nyingi.

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.multiselect/)

##Msimbo
Hivi ndivyo jinsi ya kutumia `st.multiselect`:
``` chatu
import streamt kama st

st.header('st.multiselect')

chaguzi = st.multiselect(
     'Ni rangi gani unazopenda zaidi',
     ['Kijani', 'Njano', 'Nyekundu', 'Bluu'],
     ['Njano', 'Nyekundu'])

st.write('Umechagua:', chaguzi)
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:
``` chatu
st.header('st.multiselect')
```

Kisha, tutatumia wijeti ya `st.multiselect` kukubali ingizo ambapo watumiaji wataweza kuchagua rangi moja au zaidi ya chaguo hapo.

``` chatu
chaguzi = st.multiselect(
     'Ni rangi gani unazopenda zaidi',
     ['Kijani', 'Njano', 'Nyekundu', 'Bluu'],
     ['Njano', 'Nyekundu'])
```

Hatimaye, tutaandika rangi zilizochaguliwa:
``` chatu
st.write('Umechagua:', chaguzi)
```

## Kusoma zaidi
- [`st.multiselect`](https://docs.streamlit.io/library/api-reference/widgets/st.multiselect)
