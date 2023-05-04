# st.cache

`st.cache` hukuruhusu kuboresha utendakazi wa programu yako ya Kuhuisha.

Uboreshaji hutoa utaratibu wa kuakibisha unaoruhusu programu yako kuendelea kufanya kazi hata inapopakia data kutoka kwenye wavuti, kudhibiti seti kubwa za data au kufanya hesabu za gharama kubwa. Hii inafanywa na kipamba `@st.cache`.

Unapoweka alama ya kukokotoa na mpambaji wa @st.cache, inaambia Streamlit kwamba wakati wowote utendakazi unapoitwa inahitaji kuangalia vitu vichache:

1. Vigezo vya ingizo ambavyo uliita chaguo za kukokotoa navyo
2. Thamani ya kigezo chochote cha nje kinachotumika katika chaguo za kukokotoa
3. Mwili wa kazi
4. Mwili wa kitendakazi chochote kinachotumika ndani ya kitendakazi kilichohifadhiwa

Ikiwa hii ni mara ya kwanza kwa Streamlit kuona vipengele hivi vinne vilivyo na thamani hizi halisi na katika mseto huu kamili na mpangilio, huendesha chaguo la kukokotoa na kuhifadhi matokeo katika kache ya ndani. Kisha, wakati ujao kazi iliyohifadhiwa inaitwa, ikiwa hakuna vipengele hivi vilivyobadilika, Streamlit itaruka tu kutekeleza kazi kabisa na, badala yake, itarejesha pato lililohifadhiwa hapo awali kwenye cache.

Njia ambayo Streamlit hufuatilia mabadiliko katika vipengele hivi ni kupitia hashing. Fikiria kache kama hifadhi ya thamani ya ufunguo wa kumbukumbu, ambapo ufunguo ni heshi ya yote yaliyo hapo juu na thamani ni kitu halisi cha pato kinachopitishwa na rejeleo.

Hatimaye, `@st.cache` inasaidia hoja ili kusanidi tabia ya kache. Unaweza kupata habari zaidi juu ya hizo katika marejeleo yetu ya API.

## Jinsi ya kutumia?

Unaweza tu kuongeza kipamba `st.cache` kwenye mstari uliotangulia wa chaguo maalum cha kukokotoa ambacho umefafanua katika programu yako ya Kuhuisha. Tazama mfano hapa chini.

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.cache/)

##Msimbo
Hivi ndivyo jinsi ya kutumia `st.cache`:
``` chatu
import streamt kama st
ingiza numpy kama np
ingiza panda kama pd
kutoka wakati wa kuagiza

st.title('st.cache')

# Kutumia akiba
a0 = wakati ()
st.subheader('Kutumia st.cache')

@st.cache(suppress_st_warning=Kweli)
def load_data_a():
  df = pd.DataFrame(
    np.rand.rand(2000000, 5),
    safu=['a', 'b', 'c', 'd', 'e']
  )
  kurudi df

st.write(load_data_a())
a1 = wakati ()
st.info(a1-a0)


# Kutotumia kashe
b0 = wakati ()
st.subheader('Si kutumia st.cache')

def load_data_b():
  df = pd.DataFrame(
    np.rand.rand(2000000, 5),
    safu=['a', 'b', 'c', 'd', 'e']
  )
  kurudi df

st.write(load_data_b())
b1 = wakati ()
st.info(b1-b0)
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` pamoja na maktaba zingine zinazotumiwa katika programu kama hivyo:
``` chatu
import streamt kama st
ingiza numpy kama np
ingiza panda kama pd
kutoka wakati wa kuagiza
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:
``` chatu
st.title('Sasisha Akiba')
```

Ifuatayo, tutafafanua vitendaji 2 maalum vya kutengeneza DataFrame kubwa ambapo ya kwanza hutumia kipamba `st.cache` huku ya pili haitumii:
``` chatu
@st.cache(suppress_st_warning=Kweli)
def load_data_a():
  df = pd.DataFrame(
    np.rand.rand(1000000, 5),
    safu=['a', 'b', 'c', 'd', 'e']
  )
  kurudi df

def load_data_b():
  df = pd.DataFrame(
    np.rand.rand(1000000, 5),
    safu=['a', 'b', 'c', 'd', 'e']
  )
  kurudi df
```

Hatimaye, tunaendesha kitendakazi maalum huku pia tukiweka muda wa kukimbia kwa kutumia `time()` amri.
``` chatu
# Kutumia akiba
a0 = wakati ()
st.subheader('Kutumia st.cache')

# Tunaweka kitendakazi cha load_data_a hapa

st.write(load_data_a())
a1 = wakati ()
st.info(a1-a0)

# Kutotumia kashe
b0 = wakati ()
st.subheader('Si kutumia st.cache')

# Tunaweka kitendakazi cha load_data_b hapa

st.write(load_data_b())
b1 = wakati ()
st.info(b1-b0)
```

Angalia jinsi kukimbia kwa mara ya kwanza kunaweza kutoa takriban muda sawa wa kukimbia. Pakia upya programu na utambue jinsi muda wa uendeshaji unavyobadilika unapotumia kipamba `st.cache`. Je, umeona ongezeko lolote la kasi?

## Kusoma zaidi
- [`st.cache` API Documentation](https://docs.streamlit.io/library/api-reference/performance/st.cache)
- [Boresha utendakazi kwa `st.cache`](https://docs.streamlit.io/library/advanced-features/caching)
- [Majaribio ya awali ya akiba](https://docs.streamlit.io/library/advanced-features/experimental-cache-primitives)
- [`st.experimental_memo`](https://docs.streamlit.io/library/api-reference/performance/st.experimental_memo)
- [`st.experimental_singleton`](https://docs.streamlit.io/library/api-reference/performance/st.experimental_singleton)
