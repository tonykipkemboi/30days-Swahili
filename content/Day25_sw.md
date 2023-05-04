# jimbo_la_st

Tunafafanua ufikiaji wa programu ya Kuhuisha katika kichupo cha kivinjari kama kipindi. Kwa kila kichupo cha kivinjari kinachounganishwa na seva ya Kuhuisha, kipindi kipya kinaundwa. Uboreshaji huendesha upya hati yako kutoka juu hadi chini kila wakati unapotumia programu yako. Kila marudio hufanyika katika slate tupu: hakuna vigezo vinavyoshirikiwa kati ya kukimbia.

Hali ya Kipindi ni njia ya kushiriki vigeu kati ya marudio, kwa kila kipindi cha mtumiaji. Kando na uwezo wa kuhifadhi na kuendeleza hali, Streamlit pia hufichua uwezo wa kudhibiti hali kwa kutumia kipengele cha Kupiga Simu.

Katika somo hili, tutaonyesha matumizi ya Hali ya Kipindi na Simu tunapounda programu ya kubadilisha uzani.

`st.session_state` inaruhusu utekelezaji wa hali ya kipindi katika programu ya Kuhuisha.

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.session_state/)

##Msimbo
Hivi ndivyo jinsi ya kutumia `st.session_state`:
``` chatu
import streamt kama st

st.title('st.session_state')

def lbs_to_kg():
  st.session_state.kg = st.session_state.lbs/2.2046
def kg_to_lbs():
  st.session_state.lbs = st.session_state.kg*2.2046

st.header('Ingizo')
col1, spacer, col2 = st.columns([2,1,2])
na col1:
  pounds = st.number_input("Pauni:", ufunguo = "lbs", on_change = lbs_to_kg)
na col2:
  kilo = st.number_input("Kilogramu:", ufunguo = "kg", on_change = kg_to_lbs)

st.header('Pato')
st.write("st.session_state object:", st.session_state)
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
```

Kwanza, tutaanza kwa kuunda kichwa cha programu:
``` chatu
st.title('st.session_state')
```

Ifuatayo, tunafafanua utendakazi maalum kwa ubadilishaji wa uzito kutoka lbs hadi kilo na kinyume chake:
``` chatu
def lbs_to_kg():
  st.session_state.kg = st.session_state.lbs/2.2046
def kg_to_lbs():
  st.session_state.lbs = st.session_state.kg*2.2046
```

Hapa, tunatumia `st.number_input` kukubali ingizo za nambari za thamani za uzito:
``` chatu
st.header('Ingizo')
col1, spacer, col2 = st.columns([2,1,2])
na col1:
  pounds = st.number_input("Pauni:", ufunguo = "lbs", on_change = lbs_to_kg)
na col2:
  kilo = st.number_input("Kilogramu:", ufunguo = "kg", on_change = kg_to_lbs)
```
Vitendaji 2 maalum vilivyo hapo juu vitaitwa mara tu thamani ya nambari itakapowekwa kwenye kisanduku cha nambari iliyoundwa kwa kutumia amri ya `st.number_input`. Ona jinsi chaguo la `on_change` linavyobainisha vitendaji 2 maalum `lbs_to_kg` na `kg_to_lbs`).

Kwa kifupi, unapoingiza nambari kwenye kisanduku cha `st.number_input` nambari hiyo inabadilishwa kwa kutumia vipengele hivi maalum.

Hatimaye, thamani za uzito katika vitengo vya `kg` na `lbs` kama zilivyohifadhiwa katika hali ya kipindi kama `st.session_state.kg` na `st.session_state.lbs` zitachapishwa kupitia `st.write`:
``` chatu
st.header('Pato')
st.write("st.session_state object:", st.session_state)
```

## Kusoma zaidi
- [Hali ya Kikao](https://docs.streamlit.io/library/api-reference/session-state)
- [Ongeza hali kwa programu](https://docs.streamlit.io/library/advanced-features/session-state)
