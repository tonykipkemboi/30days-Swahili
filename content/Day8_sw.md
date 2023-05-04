# kitelezi

`st.slider` inaruhusu onyesho la wijeti ya kuingiza kitelezi.

Aina zifuatazo za data zinatumika: int, kuelea, tarehe, saa na tarehe.

## Tunajenga nini?

Programu rahisi inayoonyesha njia mbalimbali za jinsi ya kukubali ingizo la mtumiaji kwa kurekebisha wijeti ya kitelezi.

Mtiririko wa programu:
1. Mtumiaji huchagua thamani kwa kurekebisha wijeti ya kitelezi
2. Programu huchapisha thamani iliyochaguliwa

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.slider/)


##Msimbo
Hivi ndivyo jinsi ya kutumia st.slider:

``` chatu
import streamt kama st
kutoka wakati wa kuagiza, wakati wa tarehe

st.header('st.slider')

#Mfano 1

st.subheader('Slider')

age = st.slider('Una umri gani?', 0, 130, 25)
st.write("Mimi nina", umri, 'umri wa miaka')

#Mfano wa 2

st.subheader('Kitelezi cha masafa')

thamani = st.slider(
     'Chagua anuwai ya maadili',
     0.0, 100.0, (25.0, 75.0))
st.write('Maadili:', maadili)

#Mfano wa 3

st.subheader('Kitelezi cha muda wa masafa')

miadi = st.slider(
     "Panga miadi yako:",
     thamani=(wakati(11, 30), muda(12, 45)))
st.write("Umeratibiwa:", miadi)

#Mfano wa 4

st.subheader('Kitelezi cha tarehe')

start_time = st.slider(
     "Unaanza lini?",
     thamani=tarehe(2020, 1, 1, 9, 30),
     umbizo = "MM/DD/YY - hh:mm")
st.write("Wakati wa kuanza:", saa_ya_kuanza)

```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
kutoka wakati wa kuagiza, wakati wa tarehe
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:
``` chatu
st.header('st.slider')
```

**Mfano 1**

Kitelezi:

``` chatu
st.subheader('Slider')

age = st.slider('Una umri gani?', 0, 130, 25)
st.write("Mimi nina", umri, 'umri wa miaka')
```

Kama tunavyoona, amri ya `st.slider()`
hutumika kukusanya maoni ya mtumiaji kuhusu umri wa watumiaji.

Hoja ya kwanza ya ingizo inaonyesha maandishi juu ya wijeti ya **kitelezi** ikiuliza `'Una umri gani?'`.

Nambari kamili tatu zifuatazo `0, 130, 25` inawakilisha thamani za chini zaidi, za juu zaidi na chaguo-msingi, mtawalia.

**Mfano wa 2**

Kitelezi cha safu:

``` chatu
st.subheader('Kitelezi cha masafa')

thamani = st.slider(
     'Chagua anuwai ya maadili',
     0.0, 100.0, (25.0, 75.0))
st.write('Maadili:', maadili)
```

Kitelezi cha masafa huruhusu uteuzi wa jozi ya thamani ya chini na ya juu.

Hoja ya kwanza ya ingizo inaonyesha maandishi juu kidogo ya kitelezi cha masafa** kikiuliza `'Chagua anuwai ya thamani'`.

Hoja tatu zifuatazo `0.0, 100.0, (25.0, 75.0)` zinawakilisha thamani za chini kabisa na za juu zaidi huku nakala ya mwisho inaashiria thamani chaguo-msingi za kutumia kama zile zilizochaguliwa za chini kabisa (25.0) na za juu (75.0).

**Mfano wa 3**

Kitelezi cha muda wa masafa:

``` chatu
st.subheader('Kitelezi cha muda wa masafa')

miadi = st.slider(
     "Panga miadi yako:",
     thamani=(wakati(11, 30), muda(12, 45)))
st.write("Umeratibiwa:", miadi)
```

Kitelezi cha muda wa masafa huruhusu uteuzi wa jozi ya thamani ya chini na ya juu ya wakati.

Hoja ya kwanza ya ingizo inaonyesha maandishi juu kidogo ya kitelezi cha **saa za masafa** kinachouliza `'Ratibu miadi yako:`.

Thamani chaguo-msingi za jozi za thamani ya chini na ya juu za muda zimewekwa kuwa 11:30 na 12:45, mtawalia.

**Mfano wa 4**

Kitelezi cha tarehe:

``` chatu
st.subheader('Kitelezi cha tarehe')

start_time = st.slider(
     "Unaanza lini?",
     thamani=tarehe(2020, 1, 1, 9, 30),
     umbizo = "MM/DD/YY - hh:mm")
st.write("Wakati wa kuanza:", saa_ya_kuanza)
```

Kitelezi cha tarehe huruhusu uteuzi wa tarehe.

Hoja ya kwanza ya ingizo inaonyesha maandishi juu kidogo ya wijeti ya **tarehe** inayouliza `'Unaanza lini?'`.

Thamani chaguomsingi ya muda iliwekwa kwa kutumia chaguo la `thamani` kuwa tarehe 1 Januari 2020 saa 9:30.

## Kusoma zaidi
Unaweza pia kuchunguza wijeti ifuatayo inayohusiana:
- [`st.select_slider`](https://docs.streamlit.io/library/api-reference/widgets/st.select_slider)
