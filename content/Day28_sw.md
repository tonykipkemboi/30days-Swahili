# umbo la kutiririsha

[`streamlit-shap`](https://github.com/snehankekre/streamlit-shap) ni kipengele cha Kuhuisha ambacho hutoa kanga ili kuonyesha viwanja vya [SHAP](https://github.com/slundberg/shap) katika [Tiririsha](https://streamlit.io/).

Maktaba hii imeundwa na wafanyikazi wetu wa ndani [Snehan Kekre](https://github.com/snehankekre) ambao pia hudumisha tovuti ya [Hati za Uboreshaji](https://docs.streamlit.io/).

Kwanza, sakinisha Streamlit (bila shaka!) kisha bomba kusakinisha `streamlit-shap` maktaba:
```bashi
pip install streamlit
pip install streamlit-shap
```

Pia kuna maktaba zingine za sharti za kusakinisha (k.m. `matplotlib`, `pandas`, `scikit-learn` na `xgboost`) ikiwa bado hujafanya hivyo.


## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/streamlit-shap/)

##Msimbo
Hivi ndivyo jinsi ya kutumia `streamlit-shap`:
``` chatu
import streamt kama st
kutoka kwa streamlit_shap leta st_shap
umbo la kuagiza
kutoka kwa sklearn.model_selection kuleta train_test_split
agiza xgboost
ingiza numpy kama np
ingiza panda kama pd

st.set_page_config(layout="wide")

@st.memo_ya_majaribio
def load_data():
    rudisha shap.datasets.adult()

@st.memo_ya_majaribio
def load_model(X, y):
    X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=7)
    d_train = xgboost.DMatrix(X_train, lebo=y_train)
    d_test = xgboost.DMatrix(X_test, lebo=y_test)
    vigezo = {
        "eta": 0.01,
        "objective": "binary:logistic",
        "mfano": 0.5,
        "base_score": np.mean(y_train),
        "eval_metric": "logloss",
        "n_kazi": -1,
    }
    model = xgboost.train(params, d_train, 10, evals = [(d_test, "test")], verbose_eval=100, early_stopping_rounds=20)
    mfano wa kurudi

st.title("`streamlit-shap` ya kuonyesha viwanja vya SHAP katika programu ya Kuhuisha")

na st.expander('Kuhusu programu'):
    st.markdown('''[`streamlit-shap`](https://github.com/snehankekre/streamlit-shap) ni kipengele cha Uboreshaji ambacho hutoa kanga ili kuonyesha [SHAP](https://github.com /slundberg/shap) inapanga katika [Streamlit](https://streamlit.io/).
                    Maktaba hii imeundwa na wafanyikazi wetu wa ndani [Snehan Kekre](https://github.com/snehankekre) ambao pia hudumisha tovuti ya [Hati za Uboreshaji](https://docs.streamlit.io/).
                ''')

st.header('Ingizo data')
X,y = load_data()
X_display,y_display = shap.datasets.adult(display=True)

na st.expander('Kuhusu data'):
    st.write('Data ya sensa ya watu wazima inatumika kama mfano wa mkusanyiko wa data.')
na st.expander('X'):
    st.dataframe(X)
na st.expander('y'):
    st.dataframe(y)

st.header('SHAP output')
 
# treni ya XGBoost mfano
model = load_model(X, y)

# hesabu thamani za SHAP
mfafanuzi = shap.Explainer(mfano, X)
shap_values = mfafanuzi(X)

na st.expander('Njama ya maporomoko ya maji'):
    st_shap(shap.plots.waterfall(shap_values[0]), urefu=300)
na st.expander('Nyuki plot'):
    st_shap(shap.plots.beeswarm(shap_values), urefu=300)

mfafanuzi = shap.TreeExplainer(mfano)
shap_values = explainer.shap_values(X)

na st.expander('Njama ya Nguvu'):
    st.subheader('Mfano wa kwanza wa data')
    st_shap(shap.force_plot(explainer.expected_value, shap_values[0,:], X_display.iloc[0,:]), urefu=200, upana=1000)
    st.subheader('mfano wa data elfu moja')
    st_shap(shap.force_plot(explainer.expected_value, shap_values[:1000,:], X_display.iloc[:1000,:]), urefu=400, upana=1000)
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
kutoka kwa streamlit_shap leta st_shap
umbo la kuagiza
kutoka kwa sklearn.model_selection kuleta train_test_split
agiza xgboost
ingiza numpy kama np
ingiza panda kama pd
```

Kisha, tutaweka mpangilio wa ukurasa kuwa mpana hivi kwamba yaliyomo katika programu ya Kuhuisha yanaweza kueneza upana wa ukurasa mzima.
``` chatu
st.set_page_config(layout="wide")
```

Kisha, tutapakia katika mkusanyiko wa data kutoka kwa maktaba ya `shap`:
``` chatu
@st.memo_ya_majaribio
def load_data():
    rudisha shap.datasets.adult()
```

Baadaye, tutabainisha chaguo za kukokotoa zinazoitwa `load_model` kwa ajili ya kuchukua katika jozi ya `X, y` ya matrix kama ingizo, kufanya mgawanyiko wa data ili kutoa mafunzo/kujaribu seti, kuunda `DMatrix` na kuunda muundo wa XGBoost.
``` chatu
@st.memo_ya_majaribio
def load_model(X, y):
    X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=7)
    d_train = xgboost.DMatrix(X_train, lebo=y_train)
    d_test = xgboost.DMatrix(X_test, lebo=y_test)
    vigezo = {
        "eta": 0.01,
        "objective": "binary:logistic",
        "mfano": 0.5,
        "base_score": np.mean(y_train),
        "eval_metric": "logloss",
        "n_kazi": -1,
    }
    model = xgboost.train(params, d_train, 10, evals = [(d_test, "test")], verbose_eval=100, early_stopping_rounds=20)
    mfano wa kurudi
```

Kichwa cha programu ya Kuhuisha huonyeshwa:
``` chatu
st.title("`streamlit-shap` ya kuonyesha viwanja vya SHAP katika programu ya Kuhuisha")
```

Kisanduku kuhusu kipanuzi kinatekelezwa ili kutoa maelezo ya programu:
``` chatu
na st.expander('Kuhusu programu'):
    st.markdown('''[`streamlit-shap`](https://github.com/snehankekre/streamlit-shap) ni kipengele cha Uboreshaji ambacho hutoa kanga ili kuonyesha [SHAP](https://github.com /slundberg/shap) inapanga katika [Streamlit](https://streamlit.io/).
                    Maktaba hii imeundwa na wafanyikazi wetu wa ndani [Snehan Kekre](https://github.com/snehankekre) ambao pia hudumisha tovuti ya [Hati za Uboreshaji](https://docs.streamlit.io/).
                ''')
```

Hapa, tutaonyesha maandishi ya kichwa pamoja na kisanduku cha kipanuzi cha vigeuzo vya `X` na `y` vya data ya Ingizo:
``` chatu
st.header('Ingizo data')
X,y = load_data()
X_display,y_display = shap.datasets.adult(display=True)

na st.expander('Kuhusu data'):
    st.write('Data ya sensa ya watu wazima inatumika kama mfano wa mkusanyiko wa data.')
na st.expander('X'):
    st.dataframe(X)
na st.expander('y'):
    st.dataframe(y)
```

Hapa, tutaonyesha maandishi ya kichwa kwa matokeo yajayo ya SHAP:
``` chatu
st.header('SHAP output')
```

Kielelezo cha XGBoost basi kinaundwa kwa kutumia kitendakazi cha `load_model` ambacho kilitekelezwa hapo juu. Hatimaye,
``` chatu
# treni ya XGBoost mfano
X,y = load_data()
X_display,y_display = shap.datasets.adult(display=True)

model = load_model(X, y)
```

Hapa, tutakokotoa thamani za SHAP, ambazo hutumika kuunda viwanja vya Maporomoko ya Maji na Nyuki.
``` chatu
# hesabu thamani za SHAP
mfafanuzi = shap.Explainer(mfano, X)
shap_values = mfafanuzi(X)

na st.expander('Njama ya maporomoko ya maji'):
    st_shap(shap.plots.waterfall(shap_values[0]), urefu=300)
na st.expander('Nyuki plot'):
    st_shap(shap.plots.beeswarm(shap_values), urefu=300)
```

Hatimaye, algoriti za Tree SHAP hutumika kueleza matokeo ya miundo ya miti iliyounganishwa kupitia amri ya `shap.TreeExplainer` na kuonyeshwa kupitia amri ya `shap.force_plot`:
``` chatu
mfafanuzi = shap.TreeExplainer(mfano)
shap_values = explainer.shap_values(X)

na st.expander('Njama ya Nguvu'):
    st.subheader('Mfano wa kwanza wa data')
    st_shap(shap.force_plot(explainer.expected_value, shap_values[0,:], X_display.iloc[0,:]), urefu=200, upana=1000)
    st.subheader('mfano wa data elfu moja')
    st_shap(shap.force_plot(explainer.expected_value, shap_values[:1000,:], X_display.iloc[:1000,:]), urefu=400, upana=1000)
```

## Kusoma zaidi
- [`streamlit-shap`](https://github.com/snehankekre/streamlit-shap)
- [SHAP](https://github.com/slundberg/shap)
