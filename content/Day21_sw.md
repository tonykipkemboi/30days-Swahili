#maendeleo

`st.progress` huonyesha upau wa maendeleo ambao husasishwa kielelezo jinsi marudio yanavyoendelea.

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.progress/)

##Msimbo
Hivi ndivyo jinsi ya kutumia `st.progress`:
``` chatu
import streamt kama st
muda wa kuagiza

st.title('st.progress')

na st.expander('Kuhusu programu hii'):
     st.write('Sasa unaweza kuonyesha maendeleo ya hesabu zako katika programu ya Kuhuisha kwa amri ya `st.progress`.')

my_bar = st.progress(0)

kwa percent_complete katika masafa(100):
     wakati.usingizi(0.05)
     my_bar.progress(asilimia_kamili + 1)

st.balloons()
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` pamoja na maktaba ya `time` kama hivyo:
``` chatu
import streamt kama st
muda wa kuagiza
```

Ifuatayo, tunaunda maandishi ya kichwa cha programu:
``` chatu
st.title('st.progress')
```

**Sanduku la Kuhusu** limeundwa kwa kutumia `st.expander` na maelezo yanaonyeshwa kupitia `st.write`:
``` chatu
na st.expander('Kuhusu programu hii'):
     st.write('Sasa unaweza kuonyesha maendeleo ya hesabu zako katika programu ya Kuhuisha kwa amri ya `st.progress`.')
```

Hatimaye, tunafafanua upau wa maendeleo na kuuthibitisha kwa thamani ya kuanzia ya `0`. Kisha, kitanzi cha `for` kitarudia kutoka `0` hadi `100` ifikiwe. Katika kila marudio, tunatumia `time.sleep(0.05)` ili kuruhusu programu kusubiri `0.05` kabla ya kuongeza thamani ya `1` kwenye upau wa maendeleo `my_bar` na kwa kufanya hivyo onyesho la picha la upau huongezeka. kwa kila marudio.
``` chatu
my_bar = st.progress(0)

kwa percent_complete katika masafa(100):
     wakati.usingizi(0.05)
     my_bar.progress(asilimia_kamili + 1)

st.balloons()
```

## Kusoma zaidi
- [`st.progress`](https://docs.streamlit.io/library/api-reference/status/st.progress)
