# Kubinafsisha mada ya programu za Kuboresha

Tunaweza kubinafsisha mandhari kwa kurekebisha vigezo katika `config.toml`, ambayo ni faili ya usanidi iliyohifadhiwa katika folda sawa na programu katika folda `.streamlit`.

## Tunajenga nini?

Programu rahisi inayoonyesha matokeo ya ubinafsishaji wa mada yetu. Hili linawezekana kwa kubinafsisha msimbo wa HTML wa HEX ndani ya [`.streamlit/config.toml`](https://github.com/dataprofessor/streamlit-custom-theme/blob/master/.streamlit/config.toml) faili.

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/streamlit-custom-theme/)

##Msimbo
Huu hapa ni msimbo wa faili ya [`streamlit_app.py`](https://github.com/dataprofessor/streamlit-custom-theme/blob/master/streamlit_app.py):
``` chatu
import streamt kama st

st.title('Kubinafsisha mandhari ya Programu za Kuhuisha')

st.write('Yaliyomo katika faili ya `.streamlit/config.toml` ya programu hii')

st.code("""
[mandhari]
primaryColor="#F39C12"
backgroundColor="#2E86C1"
secondaryBackgroundColor="#AED6F1"
textColor="#FFFFFF"
font="monospace"
""")

nambari = st.sidebar.slider('Chagua nambari:', 0, 10, 5)
st.write('Nambari iliyochaguliwa kutoka kwa wijeti ya kitelezi ni:', nambari)
```

Huu hapa ni msimbo wa faili ya [`.streamlit/config.toml`](https://github.com/dataprofessor/streamlit-custom-theme/blob/master/.streamlit/config.toml):
``` chatu
[mandhari]
primaryColor="#F39C12"
backgroundColor="#2E86C1"
secondaryBackgroundColor="#AED6F1"
textColor="#FFFFFF"
font="monospace"
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:
``` chatu
st.title('Theming with config.toml')
```

Kisha, tutaonyesha yaliyomo kwenye faili ya `.streamlit/config.toml` ambayo tutaonyesha kwanza dokezo hili kupitia `st.write` ikifuatiwa na msimbo halisi kupitia `st.code`:
``` chatu
st.write('Yaliyomo katika faili ya ./streamlit/config.toml ya programu hii')

st.code("""
[mandhari]
primaryColor="#F39C12"
backgroundColor="#2E86C1"
secondaryBackgroundColor="#AED6F1"
textColor="#FFFFFF"
font="monospace"
""")
```

Hatimaye, tunaunda wijeti ya kitelezi kwenye utepe ikifuatiwa na kuonyesha nambari iliyochaguliwa:
``` chatu
nambari = st.sidebar.slider('Chagua nambari:', 0, 10, 5)
st.write('Nambari iliyochaguliwa kutoka kwa wijeti ya kitelezi ni:', nambari)
```

Hebu sasa tuangalie rangi maalum ambazo tumetumia katika programu hii, ambazo zimebainishwa katika faili ya `.streamlit/config.toml`:
- `primaryColor="#F39C12"` - Hii inaweka rangi ya msingi kuwa chungwa. Angalia rangi za machungwa kwenye wijeti ya kitelezi.
- `backgroundColor="#2E86C1"` - Hii inaweka rangi ya usuli kuwa samawati. Kumbuka paneli kuu ina rangi ya mandharinyuma ya samawati.
- `secondaryBackgroundColor="#AED6F1"` - Hii huweka rangi ya usuli ya pili hadi kijivu iliyokolea. Angalia rangi ya mandharinyuma ya kijivu ya utepe na rangi ya usuli ya kisanduku cha msimbo kwenye paneli kuu.
- `textColor="#FFFFFF"` - Rangi ya maandishi imewekwa kuwa nyeupe.
- `font="monospace"` - Hii inaweka fonti kuwa nafasi moja.


## Kusoma zaidi
- [Mandhari](https://docs.streamlit.io/library/advanced-features/theming)
- [Nambari za Rangi za HTML](https://htmlcolorcodes.com/) ni zana nzuri ya kuchagua rangi zinazokuvutia.
