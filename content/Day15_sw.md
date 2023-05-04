# st.latex

`st.latex` huonyesha vielezi vya hisabati vilivyoumbizwa kama LaTeX.

## Tunajenga nini?

Programu rahisi inayoonyesha mlingano wa hisabati kwa kutumia sintaksia ya LaTeX kupitia amri ya `st.latex`.

## Programu ya onyesho
[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.latex/)

##Msimbo
Hivi ndivyo jinsi ya kutumia `st.latex`:
``` chatu
import streamt kama st

st.header('st.latex')

st.latex(r'''
     a + ar + a r^2 + a r^3 + \cdots + a r^{n-1} =
     \jumla_{k=0}^{n-1} ar^k =
     a \kushoto(\frac{1-r^{n}}{1-r}\kulia)
     ''')
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:
``` chatu
st.header('st.latex')
```

Kisha, tunaonyesha mlingano wa hisabati kupitia `st.latex`:
``` chatu
st.latex(r'''
     a + ar + a r^2 + a r^3 + \cdots + a r^{n-1} =
     \jumla_{k=0}^{n-1} ar^k =
     a \kushoto(\frac{1-r^{n}}{1-r}\kulia)
     ''')
```

##Marejeleo
- Soma zaidi kuhusu [`st.latex`](https://docs.streamlit.io/library/api-reference/text/st.latex) katika Hati ya API ya Kuhuisha.
