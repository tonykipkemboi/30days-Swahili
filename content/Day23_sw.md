# st.experimental_get_query params

`st.experimental_get_query_params` inaruhusu urejeshaji wa vigezo vya hoja moja kwa moja kutoka kwa URL ya kivinjari cha mtumiaji.

## Programu ya onyesho

1. Kiungo kifuatacho hupakia programu ya onyesho bila vigezo vya kuuliza (angalia ujumbe wa hitilafu):

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.experimental_get_query_params/)

2. Kiungo kifuatacho hupakia programu ya onyesho na vigezo vya hoja (hakuna ujumbe wa hitilafu hapa):

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](http://share.streamlit.io/dataprofessor/st.experimental_get_query_params/?firstname=Jack&surname=Beanstalk)

##Msimbo
Hivi ndivyo jinsi ya kutumia `st.experimental_get_query_params`:
``` chatu
import streamt kama st

st.title('st.experimental_get_query_params')

na st.expander('Kuhusu programu hii'):
  st.write("`st.experimental_get_query_params` huruhusu urejeshaji wa vigezo vya hoja moja kwa moja kutoka kwa URL ya kivinjari cha mtumiaji.")

# 1. Maagizo
st.header('1. Maagizo')
st.markdown('''
Katika upau wa URL hapo juu wa kivinjari chako cha wavuti, weka yafuatayo:
`?jina la kwanza=Jack&surname=Beanstalk`
baada ya URL msingi `http://share.streamlit.io/dataprofessor/st.experimental_get_query_params/`
kwamba inakuwa
`http://share.streamlit.io/dataprofessor/st.experimental_get_query_params/?firstname=Jack&surname=Beanstalk`
''')


# 2. Yaliyomo katika st.experimental_get_query_params
st.header('2. Yaliyomo katika st.experimental_get_query_params')
st.write(st.experimental_get_query_params())


# 3. Kurejesha na kuonyesha habari kutoka kwa URL
st.header('3. Kurejesha na kuonyesha taarifa kutoka kwa URL')

firstname = st.experimental_get_query_params()['firstname'][0]
jina la ukoo = st.experimental_get_query_params()['surname'][0]

st.write(f'Hello **{firstname} {surname}**, habari yako?')
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
```

Ifuatayo, tutaipa programu jina:
``` chatu
st.title('st.experimental_get_query_params')
```

Wacha pia tuongeze kisanduku kunjuzi cha Kuhusu:
``` chatu
na st.expander('Kuhusu programu hii'):
  st.write("`st.experimental_get_query_params` huruhusu urejeshaji wa vigezo vya hoja moja kwa moja kutoka kwa URL ya kivinjari cha mtumiaji.")
```

Kisha, tutatoa maagizo kwa wanaotembelea programu kuhusu jinsi wanavyoweza kupitisha vigezo vya hoja moja kwa moja kwenye URL:
``` chatu
# 1. Maagizo
st.header('1. Maagizo')
st.markdown('''
Katika upau wa URL hapo juu wa kivinjari chako cha wavuti, weka yafuatayo:
`?jina=Jack&surname=Beanstalk`
baada ya URL msingi `http://share.streamlit.io/dataprofessor/st.experimental_get_query_params/`
kwamba inakuwa
`http://share.streamlit.io/dataprofessor/st.experimental_get_query_params/?firstname=Jack&surname=Beanstalk`
''')
```

Baadaye, tutaonyesha maudhui ya amri ya `st.experimental_get_query_params`.
``` chatu
# 2. Yaliyomo katika st.experimental_get_query_params
st.header('2. Yaliyomo katika st.experimental_get_query_params')
st.write(st.experimental_get_query_params())
```

Hatimaye, tutachagua na kuonyesha taarifa teule kutoka kwa kigezo cha hoja cha URL:
``` chatu
# 3. Kurejesha na kuonyesha habari kutoka kwa URL
st.header('3. Kurejesha na kuonyesha taarifa kutoka kwa URL')

firstname = st.experimental_get_query_params()['firstname'][0]
jina la ukoo = st.experimental_get_query_params()['surname'][0]

st.write(f'Hello **{firstname} {surname}**, habari yako?')
```

## Kusoma zaidi
- [`st.experimental_get_query_params`](https://docs.streamlit.io/library/api-reference/utilities/st.experimental_get_query_params)
