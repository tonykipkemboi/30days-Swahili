# st.line_chati

`st.line_chart` inaonyesha chati ya mstari.

Hii ni sintaksia-sukari karibu na `st.altair_chart`. Tofauti kuu ni kwamba amri hii hutumia safu wima na fahirisi za data ili kubaini vipimo vya chati. Kama matokeo hii ni rahisi kutumia kwa hali nyingi za "panga tu hii", huku ikiwa haiwezi kubinafsishwa.

Iwapo `st.line_chart` haikisii vipimo vya data kwa usahihi, jaribu kubainisha chati unayotaka kwa kutumia st.altair_chart.

## Tunajenga nini?

Programu rahisi ya kuonyesha chati ya mstari.

Mtiririko wa programu:
1. Unda `Pandas` DataFrame kutoka kwa nambari zinazozalishwa bila mpangilio kupitia `NumPy`.
2. Unda na uonyeshe chati ya mstari kupitia amri ya `st.line_chart()`.

## Programu ya onyesho

[![Sasisha Programu](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.line_chart/)

##Msimbo
Hivi ndivyo jinsi ya kutumia [`st.line_chart`](https://docs.streamlit.io/library/api-reference/charts/st.line_chart):
``` chatu
import streamt kama st
ingiza panda kama pd
ingiza numpy kama np

st.header('Chati ya mstari')

chart_data = pd.DataFrame(
     np.random.randn(20, 3),
     safu=['a', 'b', 'c'])

st.line_chart(data_chati)

```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` pamoja na maktaba zingine kama hivyo:
``` chatu
import streamt kama st
ingiza panda kama pd
ingiza numpy kama np
```

Ifuatayo, tunaunda maandishi ya kichwa kwa programu:
``` chatu
st.header('Chati ya mstari')
```

Kisha, tunaunda DataFrame ya nambari zinazozalishwa kwa nasibu ambayo ina safu wima 3.
``` chatu
chart_data = pd.DataFrame(
     np.random.randn(20, 3),
     safu=['a', 'b', 'c'])
```

Hatimaye, chati ya mstari huundwa kwa kutumia `st.line_chart()` na DataFrame iliyohifadhiwa katika kigezo cha `chart_data` kama data ya ingizo:
``` chatu
st.line_chart(data_chati)
```

## Kusoma zaidi
Soma zaidi kuhusu amri ifuatayo ya Kuhuisha ambayo [`st.line_chart`](https://docs.streamlit.io/library/api-reference/charts/st.line_chart) imetokana na:
- [`st.altair_chart`](https://docs.streamlit.io/library/api-reference/charts/st.altair_chart)
