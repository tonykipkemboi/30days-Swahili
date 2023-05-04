Kisanduku # cha kuteua

`st.checkbox` huonyesha wijeti ya kisanduku cha kuteua.

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.checkbox/)

##Msimbo
Hivi ndivyo jinsi ya kutumia `st.checkbox`:
``` chatu
import streamt kama st

st.header('st.checkbox')

st.write ('Ungependa kuagiza nini?')

aiskrimu = st.checkbox('Ice cream')
kahawa = st.checkbox('Kahawa')
cola = st.checkbox('Cola')

ikiwa icecream:
     st.write("Nzuri! Hapa kuna zingine 🍦")
    
ikiwa kahawa:
     st.write("Sawa, hapa kuna kahawa ☕")

ikiwa cola:
     st.write("Haya njoo 🥤")
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:
``` chatu
st.header('st.checkbox')
```

Kisha, tutauliza swali kupitia `st.write':
``` chatu
st.write ('Ungependa kuagiza nini?')
```

Kisha tutatoa baadhi ya vipengee vya menyu vya kuweka tiki:
``` chatu
aiskrimu = st.checkbox('Ice cream')
kahawa = st.checkbox('Kahawa')
cola = st.checkbox('Cola')
```

Hatimaye, tutachapisha maandishi maalum kulingana na kisanduku cha kuteua kilichowekwa tiki:
``` chatu
ikiwa icecream:
     st.write("Nzuri! Hapa kuna zingine 🍦")
    
ikiwa kahawa:
     st.write("Sawa, hapa kuna kahawa ☕")

ikiwa cola:
     st.write("Haya unakwenda 🥤")
```

## Kusoma zaidi
- [`st.checkbox`](https://docs.streamlit.io/library/api-reference/widgets/st.checkbox)
