#siri

`st.secrets` hukuruhusu kuhifadhi maelezo ya siri kama vile vitufe vya API, nenosiri la hifadhidata au vitambulisho vingine.

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.secrets/)

##Msimbo
Hivi ndivyo jinsi ya kutumia `st.secrets`:
``` chatu
import streamt kama st

st.title('st.secrets')

st.write(st.secrets['ujumbe'])
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:
``` chatu
st.title('st.secrets')
```

Hatimaye, tutakuwa tunaonyesha siri zilizohifadhiwa:
``` chatu
st.write(st.secrets['ujumbe'])
```

Ikumbukwe kwamba, siri zinaweza kuhifadhiwa katika Wingu la Jumuiya ya Kuhuisha kama inavyoonyeshwa kwenye picha za skrini zilizoonyeshwa hapa chini.

Ikiwa zinafanya kazi ndani ya nchi, zinaweza kuhifadhiwa katika `.streamlit/secrets.toml`, lakini hakikisha kuwa unaepuka kupakia hii kwenye repo ya GitHub wakati wa kusambaza programu.

## Kusoma zaidi
- [Ongeza siri kwenye programu zako za Kufululiza](https://blog.streamlit.io/secrets-in-sharing-apps/)
- [Udhibiti wa siri](https://docs.streamlit.io/streamlit-cloud/get-started/deploy-an-app/connect-to-data-sources/secrets-management)
