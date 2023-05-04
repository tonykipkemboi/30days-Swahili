# Jinsi ya kutumia API kwa kujenga programu ya Bored API

Programu ya API iliyochoshwa inapendekeza mambo ya kufurahisha kwako kufanya wakati umechoka!

Kitaalam, inaonyesha pia matumizi ya API kutoka ndani ya programu ya Kuhuisha.

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/bored-api-app/)

##Msimbo
Hivi ndivyo jinsi ya kutekeleza programu ya Bored-API:
``` chatu
import streamt kama st
maombi ya kuagiza

st.title('🏀 Programu ya API iliyochoshwa')

st.sidebar.header('Ingizo')
selected_type = st.sidebar.selectbox('Chagua aina ya shughuli', ["elimu", "burudani", "kijamii", "diy", "hisani", "kupika", "kupumzika", "muziki", "kazi zenye shughuli nyingi "])

suggested_activity_url = f'http://www.boredapi.com/api/activity?type={selected_type}'
json_data = requests.get(suggested_activity_url)
suggested_activity = json_data.json()

c1, c2 = safu wima(2)
na c1:
  na st.expander('Kuhusu programu hii'):
    st.write('Je, umechoshwa? **Programu ya API ya Kuchoshwa** hutoa mapendekezo kuhusu shughuli ambazo unaweza kufanya ukiwa na kuchoka. Programu hii inaendeshwa na API ya Kuchoshwa.')
na c2:
  na st.expander('data ya JSON'):
    st.write(suggested_shughuli)
    
st.header('Shughuli inayopendekezwa')
st.info(shughuli_iliyopendekezwa['shughuli'])

col1, col2, col3 = safu wima(3)
na col1:
  st.metric(lebo='Idadi ya Washiriki', thamani=shughuli_iliyopendekezwa['washiriki'], delta='')
na col2:
  st.metric(label='Aina ya Shughuli', value=suggested_activity['type'].capitalize(), delta='')
na col3:
  st.metric(lebo='Bei', thamani=shughuli_iliyopendekezwa['bei'], delta='')
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` na `requests` maktaba kama hivyo:
``` chatu
import streamt kama st
maombi ya kuagiza
```

Kichwa cha programu kinaonyeshwa kupitia `st.title`:
``` chatu
st.title('🏀 Programu ya API iliyochoshwa')
```

Kisha, tutakubali ingizo la mtumiaji kwenye **aina ya shughuli** kwa kutumia amri ya `st.selectbox`:
``` chatu
st.sidebar.header('Ingizo')
selected_type = st.sidebar.selectbox('Chagua aina ya shughuli', ["elimu", "burudani", "kijamii", "diy", "hisani", "kupika", "kupumzika", "muziki", "kazi zenye shughuli nyingi "])
```

Shughuli iliyochaguliwa iliyotajwa hapo juu kisha huongezwa kwa URL kupitia kamba ya f, ambayo inatumiwa kupata data inayotokana na JSON:
``` chatu
suggested_activity_url = f'http://www.boredapi.com/api/activity?type={selected_type}'
json_data = requests.get(suggested_activity_url)
suggested_activity = json_data.json()
```

Hapa, tutaonyesha maelezo kuhusu programu na data ya JSON kupitia amri ya `st.expander`.
``` chatu
c1, c2 = safu wima(2)
na c1:
  na st.expander('Kuhusu programu hii'):
    st.write('Je, umechoshwa? **Programu ya API ya Kuchoshwa** hutoa mapendekezo kuhusu shughuli unazoweza kufanya. Programu hii inaendeshwa na API ya Kuchoshwa.')
na c2:
  na st.expander('data ya JSON'):
    st.write(suggested_shughuli)
```

Kisha tutaonyesha shughuli iliyopendekezwa kama vile:
``` chatu
st.header('Shughuli inayopendekezwa')
st.info(shughuli_iliyopendekezwa['shughuli'])
```

Hatimaye, tutaonyesha pia maelezo yanayoambatana ya shughuli iliyopendekezwa kama vile `Idadi ya Washiriki`, `Aina ya Shughuli` na `Bei`.
``` chatu
col1, col2, col3 = safu wima(3)
na col1:
  st.metric(lebo='Idadi ya Washiriki', thamani=shughuli_iliyopendekezwa['washiriki'], delta='')
na col2:
  st.metric(label='Aina ya Shughuli', value=suggested_activity['type'].capitalize(), delta='')
na col3:
  st.metric(lebo='Bei', thamani=shughuli_iliyopendekezwa['bei'], delta='')
```

## Kusoma zaidi
- [API ya Kuchoshwa](http://www.boredapi.com/)
