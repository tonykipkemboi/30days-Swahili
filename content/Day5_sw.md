# st.andika

`st.write` inaruhusu kuandika maandishi na hoja kwa programu ya Kuhuisha.

Mbali na kuweza kuonyesha maandishi, yafuatayo yanaweza pia kuonyeshwa kupitia amri ya `st.write()`:

- Prints masharti; inafanya kazi kama `st.markdown()`
- Inaonyesha Python `dict`
- Maonyesho ya `pandas` DataFrame inaweza kuonyeshwa kama jedwali
- Viwanja/grafu/takwimu kutoka kwa `matplotlib`, `plotly`, `altair`, `graphviz`, `bokeh`
- Na zaidi (ona [st.write on API docs](https://docs.streamlit.io/library/api-reference/write-magic/st.write))

## Tunajenga nini?

Programu rahisi inayoonyesha njia mbalimbali za jinsi ya kutumia amri ya `st.write()` kwa kuonyesha maandishi, nambari, DataFrame na viwanja.

## Programu ya onyesho

Programu ya Kuhuisha iliyotumika inapaswa kuonekana kama ile iliyoonyeshwa kwenye kiungo kilicho hapa chini:

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.write/)

## Msimbo

Hivi ndivyo jinsi ya kutumia st.write:

```bash
ingiza numpy kama np
leta madhabahu kama al
ingiza panda kama pd
import streamt kama st

st.header('st.write')

# Mfano 1

st.write('Hujambo, *Dunia!* :sunglasses:')

# Mfano wa 2

st.write(1234)

# Mfano wa 3

df = pd.DataFrame({
     'safu wima ya kwanza': [1, 2, 3, 4],
     'safu wima ya pili': [10, 20, 30, 40]
     })
st.write(df)

# Mfano wa 4

st.write('Chini ni DataFrame:', df, 'Juu ni mfumo wa data.')

# Mfano wa 5

df2 = pd.DataFrame(
     np.random.randn(200, 3),
     safu=['a', 'b', 'c'])
c = alt.Chati(df2).mark_circle().encode().
     x='a', y='b', size='c', color='c', tooltip=['a', 'b', 'c'])
st.write(c)
```

## Maelezo ya mstari kwa mstari

Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:

```bash
import streamt kama st
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:

```bash
st.header('st.write')
```

**Mfano 1**
Kesi yake ya msingi ya utumiaji ni kuonyesha maandishi na maandishi yaliyoumbizwa na Markdown:

```bash
st.write('Hujambo, *Dunia!* :miwani ya jua:')
```

**Mfano wa 2**
Kama ilivyotajwa hapo juu, inaweza pia kutumika kuonyesha fomati zingine za data kama vile nambari:

```bash
st.write(1234)
```

**Mfano wa 3**
DataFrames pia inaweza kuonyeshwa kama ifuatavyo:

```bash
df = pd.DataFrame({
     'safu wima ya kwanza': [1, 2, 3, 4],
     'safu wima ya pili': [10, 20, 30, 40]
     })
st.write(df)
```

**Mfano wa 4**
Unaweza kupitisha kwa hoja nyingi:

```bash
st.write('Chini ni DataFrame:', df, 'Juu ni mfumo wa data.')
```

**Mfano 5**
Mwishowe, unaweza pia kuonyesha viwanja vile vile kwa kuipitisha kwa kutofautisha kama ifuatavyo:

```bash
df2 = pd.DataFrame(
     np.random.randn(200, 3),
     safu=['a', 'b', 'c'])
c = alt.Chati(df2).mark_circle().encode().
     x='a', y='b', size='c', color='c', tooltip=['a', 'b', 'c'])
st.write(c)
```

## Programu ya onyesho

Programu ya Kuhuisha iliyotumika inapaswa kuonekana kama ile iliyoonyeshwa kwenye kiungo kilicho hapa chini:

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.write/)

## Hatua zinazofuata

Kwa kuwa sasa umeunda programu ya Kuhuisha ndani ya nchi, ni wakati wa kuipeleka kwenye [Streamlit Community Cloud](https://streamlit.io/cloud) kama itakavyoelezwa hivi karibuni katika shindano lijalo.

Kwa sababu hii ni wiki ya kwanza ya changamoto yako, tunatoa msimbo kamili (kama inavyoonyeshwa kwenye kisanduku cha msimbo hapo juu) na suluhisho (programu ya onyesho) ndani ya ukurasa huu wa tovuti.

Kusonga mbele katika changamoto zinazofuata, inashauriwa kuwa kwanza ujaribu kutekeleza programu ya Kuhuisha wewe mwenyewe.

Usijali ikiwa utakwama, unaweza kutazama suluhisho kila wakati.

## Kusoma zaidi

Kando na [`st.write`](https://docs.streamlit.io/library/api-reference/write-magic/st.write), unaweza kuchunguza njia zingine za kuonyesha maandishi:

- [`st.markdown`](https://docs.streamlit.io/library/api-reference/text/st.markdown)
- [`st.header`](https://docs.streamlit.io/library/api-reference/text/st.header)
- [`st.subheader`](https://docs.streamlit.io/library/api-reference/text/st.subheader)
- [`st.caption`](https://docs.streamlit.io/library/api-reference/text/st.caption)
- [`st.text`](https://docs.streamlit.io/library/api-reference/text/st.text)
- [`st.latex`](https://docs.streamlit.io/library/api-reference/text/st.latex)
- [`st.code`](https://docs.streamlit.io/library/api-reference/text/st.code)
