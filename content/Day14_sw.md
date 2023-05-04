# Vipengee vya Kuboresha

Vipengee ni moduli za Python za wahusika wengine zinazopanua kile kinachowezekana kwa Streamlit [[1](https://docs.streamlit.io/library/components)].

## Je, ni vipengele vipi vya Uboreshaji vinavyopatikana?

Kuna dazeni kadhaa za vipengele vya Uboreshaji vilivyoangaziwa kwenye tovuti ya Streamlit [[2](https://streamlit.io/components)].

Fanilo (Mtayarishi Mwema) aliratibu orodha ya ajabu ya vipengele vya Uboreshaji kwenye chapisho la wiki [[3](https://discuss.streamlit.io/t/streamlit-components-community-tracker/4634)] ambayo huorodhesha takriban 85 vipengele hadi Aprili 2022.

## Jinsi ya kutumia?

Vipengee vya kuhuisha viko tu usakinishaji wa bomba.

Katika somo hili, hebu tuanze kutumia kipengele cha `streamlit_pandas_profiling` [[4](https://share.streamlit.io/okld/streamlit-gallery/main?p=pandas-profiling)].

#### Sakinisha kijenzi

```bashi
bomba kusakinisha streamlit_pandas_profiling
```

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/streamlit-components/)

##Msimbo
Hivi ndivyo jinsi ya kuunda programu ya Kuhuisha kwa kutumia kijenzi:
``` chatu
import streamt kama st
ingiza panda kama pd
kuagiza pandas_profiling
kutoka kwa streamlit_pandas_profiling leta st_profile_report

st.header('`streamlit_pandas_profiling`')

df = pd.read_csv('https://raw.githubusercontent.com/dataprofessor/data/master/penguins_cleaned.csv')

pr = df.profile_report()
st_profile_report(pr)
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` pamoja na maktaba zingine zinazotumiwa katika programu kama hivyo:
``` chatu
import streamt kama st
ingiza panda kama pd
kuagiza pandas_profiling
kutoka kwa streamlit_pandas_profiling leta st_profile_report
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:
``` chatu
st.header('`streamlit_pandas_profiling`')
```

Kisha, tunapakia katika hifadhidata ya Penguins kwa kutumia `read_csv` amri ya `pandas`.
``` chatu
df = pd.read_csv('https://raw.githubusercontent.com/dataprofessor/data/master/penguins_cleaned.csv')
```

Hatimaye, ripoti ya wasifu wa pandas inatolewa kupitia amri ya `profile_report()` na kuonyeshwa kwa kutumia `st_profile_report`:
``` chatu
pr = df.profile_report()
st_profile_report(pr)
```

## Kutengeneza Vipengele vyako mwenyewe

Ikiwa ungependa kutengeneza kijenzi chako mwenyewe, tafadhali angalia nyenzo zifuatazo:
- [Unda Kijenzi](https://docs.streamlit.io/library/components/create)
- [Chapisha Kipengele](https://docs.streamlit.io/library/components/publish)
- [API ya vipengele](https://docs.streamlit.io/library/components/components-api)
- [Chapisho la blogu kwenye Vipengele](https://blog.streamlit.io/introducing-streamlit-components/)

Vinginevyo, ikiwa ungependa kujifunza kwa kutumia video, mhandisi wetu Tim Conkling ameweka pamoja mafunzo ya ajabu:
- [Jinsi ya kuunda sehemu ya Kuhuisha | Sehemu ya 1: Mipangilio na Usanifu](https://youtu.be/BuD3gILJW-Q)
- [Jinsi ya kuunda sehemu ya Kuhuisha | Sehemu ya 2: Sehemu ya 2: Tengeneza Wijeti ya Kitelezi](https://youtu.be/QjccJl_7Jco)

## Usomaji zaidi kuhusu Vipengele
1. [Vipengee vya Kuhuisha - Hati za API](https://docs.streamlit.io/library/components)
2. [Vipengele Vilivyoangaziwa vya Kuhuisha](https://streamlit.io/components)
3. [Vipengele vya Kuhuisha - Kifuatiliaji cha Jumuiya](https://discuss.streamlit.io/t/streamlit-components-community-tracker/4634)
4. [`streamlit_pandas_profiling`](https://share.streamlit.io/okld/streamlit-gallery/main?p=pandas-profiling)
