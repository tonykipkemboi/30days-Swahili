# st.file_uploader

`st.file_uploader` huonyesha wijeti ya kipakiaji faili [[1](https://docs.streamlit.io/library/api-reference/widgets/st.file_uploader)].

Kwa chaguo-msingi, faili zilizopakiwa hupunguzwa hadi 200MB. Unaweza kusanidi hii kwa kutumia chaguo la usanidi la server.maxUploadSize. Kwa maelezo zaidi kuhusu jinsi ya kuweka chaguo za usanidi, angalia [[2](https://docs.streamlit.io/library/advanced-features/configuration#set-configuration-options)].

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.file_uploader/)

##Msimbo
Hivi ndivyo jinsi ya kutumia `st.file_uploader`:
``` chatu
import streamt kama st
ingiza panda kama pd

st.title('st.file_uploader')

st.subheader('Ingiza CSV')
uploaded_file = st.file_uploader("Chagua faili")

ikiwa uploaded_file sio Hakuna:
  df = pd.read_csv(faili_lililopakiwa)
  st.subheader('DataFrame')
  st.write(df)
  st.subheader('Takwimu za Maelezo')
  st.write(df.describe())
kwingine:
  st.info('☝️ Pakia faili ya CSV')
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` na maktaba mengine ya sharti kama vile:
``` chatu
import streamt kama st
ingiza panda kama pd
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:
``` chatu
st.title('st.file_uploader')
```

Kisha, tutatumia `st.file_uploader` ili kuonyesha wijeti ya kipakiaji faili kwa ajili ya kukubali faili ya ingizo ya mtumiaji:
``` chatu
st.subheader('Ingiza CSV')
uploaded_file = st.file_uploader("Chagua faili")
```

Hatimaye, tunafafanua kauli za masharti kwa ajili ya kuonyesha mwanzoni ujumbe wa kukaribisha unaowaalika watumiaji kupakia faili zao (kama inavyotekelezwa katika hali ya `vingine`). Baada ya kupakia faili, taarifa za `if` huwashwa na faili ya CSV inasomwa na maktaba ya `pandas` na kuonyeshwa kupitia amri ya `st.write`.
``` chatu
ikiwa uploaded_file sio Hakuna:
  df = pd.read_csv(faili_lililopakiwa)
  st.subheader('DataFrame')
  st.write(df)
  st.subheader('Takwimu za Maelezo')
  st.write(df.describe())
kwingine:
  st.info('☝️ Pakia faili ya CSV')
```

## Kusoma zaidi
1. [`st.file_uploader`](https://docs.streamlit.io/library/api-reference/widgets/st.file_uploader)
2. [Weka chaguo za usanidi](https://docs.streamlit.io/library/advanced-features/configuration#set-configuration-options)
