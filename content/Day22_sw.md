# fomu

`st.form` huunda fomu inayounganisha vipengele pamoja na kitufe cha "Wasilisha".

Kwa kawaida, wakati wowote mtumiaji anapoingiliana na wijeti, programu ya Streamlit inarejeshwa.

Fomu ni chombo kinachoweka pamoja vipengele vingine na wijeti, na ina kitufe cha Wasilisha. Hapa, mtumiaji anaweza kuingiliana na wijeti moja au zaidi kwa mara nyingi apendavyo bila kusababisha marudio. Hatimaye, kitufe cha Kuwasilisha cha fomu kinapobonyezwa, thamani zote za wijeti ndani ya fomu zitatumwa kwa Kufululiza katika kundi moja.

Kuongeza vipengee kwenye kitu cha fomu, unaweza kutumia nukuu ya `na` (inayopendelewa) au unaweza kuitumia kama nukuu ya kitu kwa kupiga tu njia moja kwa moja kwenye fomu (kwa kwanza kuikabidhi kwa kutofautisha na kisha kutumia njia za Uboreshaji kwenye. hiyo). Tazama kwenye programu ya mfano.

Fomu zina vikwazo vichache:
- Kila fomu lazima iwe na `st.form_submit_button`.
- `st.button` na `st.download_button` haziwezi kuongezwa kwenye fomu.
- Fomu zinaweza kuonekana popote katika programu yako (upau wa kando, safuwima, n.k), lakini haziwezi kupachikwa ndani ya fomu zingine.

Kwa maelezo zaidi kuhusu fomu, angalia [chapisho la blogu](https://blog.streamlit.io/introducing-submit-button-and-forms/).

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/dataprofessor/st.form/)

##Msimbo
Hivi ndivyo jinsi ya kutumia `st.form`:
``` chatu
import streamt kama st

st.title('st.form')

# Mfano kamili wa kutumia na nukuu
st.header('1. Mfano wa kutumia `na` nukuu')
st.subheader('Mashine ya kahawa')

na st.form('fomu_yangu'):
    st.subheader('**Agiza kahawa yako**')
    
    # Ingiza vilivyoandikwa
    coffee_bean_val = st.selectbox('Maharagwe ya kahawa', ['Arabica', 'Robusta'])
    coffee_roast_val = st.selectbox('Kahawa choma', ['Nuru', 'Kati', 'Giza'])
    brewing_val = st.selectbox('Njia ya kutengeneza pombe', ['Aeropress', 'Drip', 'French press', 'Moka pot', 'Siphon'])
    serving_type_val = st.selectbox('Muundo wa kuhudumia', ['Moto', 'Iced', 'Frappe'])
    milk_val = st.select_slider('Uzito wa maziwa', ['Hakuna', 'Chini', 'Wastani', 'Juu'])
    owncup_val = st.checkbox('Leta kikombe chako')
    
    # Kila fomu lazima iwe na kitufe cha kuwasilisha
    imewasilishwa = st.form_submit_button('Wasilisha')

ikiwa imewasilishwa:
    st.markdown(f'''
        ☕ Umeagiza:
        - Maharage ya kahawa: `{coffee_bean_val}`
        - Kuchoma kahawa: `{kahawa_roast_val}`
        - Utengenezaji: `{brewing_val}`
        - Aina ya huduma: `{serving_type_val}`
        - Maziwa: `{maziwa_val}`
        - Lete kikombe chako: `{ownup_val}`
        ''')
kwingine:
    st.write('☝️ Weka agizo lako!')


# Mfano mfupi wa kutumia nukuu ya kitu
st.header('2. Mfano wa nukuu ya kitu')

form = st.form('my_form_2')
selected_val = form.slider('Chagua thamani')
form.form_submit_button('Wasilisha')

st.write('Thamani iliyochaguliwa: ', iliyochaguliwa_val)
```

## Maelezo ya mstari kwa mstari
Jambo la kwanza kabisa la kufanya wakati wa kuunda programu ya Kuhuisha ni kuanza kwa kuleta maktaba ya `streamlit` kama `st` kama hivyo:
``` chatu
import streamt kama st
```

Hii inafuatwa na kuunda maandishi ya kichwa cha programu:
``` chatu
st.title('st.form')
```

### Mfano wa kwanza
Hebu tuanze na mfano wa kwanza, hapa tutatumia amri ya `st.form` kupitia nukuu ya `na`. Ndani ya fomu, tutaanza kwa kuandika kichwa kidogo `Agiza kahawa yako` kisha tuunde wijeti kadhaa za ingizo (`st.selectbox`, `st.select_slider` na `st.checkbox`) ili kukusanya taarifa kuhusu agizo la kahawa. Hatimaye, kitufe cha kuwasilisha kinaundwa kupitia amri ya `st.form_submit_button`, ambayo ikibofya itatuma ingizo zote za mtumiaji kama kundi moja la maelezo kwa programu ili kuchakatwa.
``` chatu
# Mfano kamili wa kutumia na nukuu
st.header('1. Mfano wa kutumia `na` nukuu')
st.subheader('Mashine ya kahawa')

na st.form('fomu_yangu'):
    st.subheader('**Agiza kahawa yako**')

    # Ingiza vilivyoandikwa
    coffee_bean_val = st.selectbox('Maharagwe ya kahawa', ['Arabica', 'Robusta'])
    coffee_roast_val = st.selectbox('Kahawa choma', ['Nuru', 'Kati', 'Giza'])
    brewing_val = st.selectbox('Njia ya kutengeneza pombe', ['Aeropress', 'Drip', 'French press', 'Moka pot', 'Siphon'])
    serving_type_val = st.selectbox('Muundo wa kuhudumia', ['Moto', 'Iced', 'Frappe'])
    milk_val = st.select_slider('Uzito wa maziwa', ['Hakuna', 'Chini', 'Wastani', 'Juu'])
    owncup_val = st.checkbox('Leta kikombe chako')
    
    # Kila fomu lazima iwe na kitufe cha kuwasilisha.
    imewasilishwa = st.form_submit_button('Wasilisha')
```

Kisha, tutaongeza mantiki ya kitakachotokea baada ya kubofya kitufe cha kuwasilisha. Kwa chaguomsingi, wakati wowote programu ya Kufululiza inapopakiwa taarifa `nyingine` itaendeshwa na tunaona ujumbe `☝️ Weka agizo lako!`. Ilhali unapobofya kitufe cha kuwasilisha, ingizo zote zinazotolewa na mtumiaji kupitia wijeti mbalimbali huhifadhiwa katika vigeu kadhaa (k.m. `coffee_bean_val`, `coffee_roast_val`, n.k.) na kuchapishwa kupitia amri ya `st.markdown` kwa usaidizi wa f. -kamba.
``` chatu
ikiwa imewasilishwa:
    st.markdown(f'''
        ☕ Umeagiza:
        - Maharage ya kahawa: `{coffee_bean_val}`
        - Kuchoma kahawa: `{kahawa_roast_val}`
        - Utengenezaji: `{brewing_val}`
        - Aina ya huduma: `{serving_type_val}`
        - Maziwa: `{maziwa_val}`
        - Lete kikombe chako: `{ownup_val}`
        ''')
kwingine:
    st.write('☝️ Weka agizo lako!')
```


### Mfano wa pili
Hebu sasa tuendelee na mfano wa pili wa kutumia `st.form` kama nukuu ya kitu. Hapa, amri ya `st.form` imepewa kigezo cha `fomu`. Baadaye, amri mbalimbali za Kufululiza kama vile `kitelezi` au `form_submit_button` hutumika kwenye kigezo cha `fomu`.
``` chatu
# Mfano mfupi wa kutumia nukuu ya kitu
st.header('2. Mfano wa nukuu ya kitu')

form = st.form('my_form_2')
selected_val = form.slider('Chagua thamani')
form.form_submit_button('Wasilisha')

st.write('Thamani iliyochaguliwa: ', iliyochaguliwa_val)
```

## Kusoma zaidi
- [`st.form`](https://docs.streamlit.io/library/api-reference/control-flow/st.form)
- [Tunatanguliza kitufe cha Wasilisha na Fomu](https://blog.streamlit.io/introducing-submit-button-and-forms/)
