# Unda dashibodi inayoweza kukokotwa na inayoweza kurejeshwa tena na Vipengee vya Uboreshaji

Streamlit Elements ni kipengele cha wahusika wengine kilichoundwa na [okld](https://github.com/okld) ambacho hukupa zana za kutunga programu nzuri na dashibodi zenye wijeti za UI Nyenzo, kihariri cha Monaco (Msimbo wa Studio inayoonekana), chati za Nivo. , na zaidi.

## Jinsi ya kutumia?

### Ufungaji

Hatua ya kwanza ni kusakinisha Vipengee vya Kuhuisha katika mazingira yako:

```bashi
pip install streamlit-elements==0.1.*
```

Inapendekezwa kubandika toleo kwenye `0.1.*`, kwani matoleo yajayo yanaweza kuleta mabadiliko yanayokiuka katika API.

### Matumizi

Unaweza kurejelea [Vipengee vya Kuhuisha README](https://github.com/okld/streamlit-elements#getting-started) kwa mwongozo wa kina wa matumizi.

## Tunajenga nini?

Lengo la changamoto ya leo ni kuunda dashibodi inayojumuisha kadi tatu za UI Nyenzo:

- Kadi ya kwanza iliyo na kihariri cha msimbo wa Monaco ili kuingiza data fulani;
- Kadi ya pili ya kuonyesha data hiyo katika chati ya Nivo Bump;
- Kadi ya tatu ya kuonyesha URL ya video ya YouTube iliyofafanuliwa kwa `st.text_input`.

Unaweza kutumia data inayotokana na onyesho la Nivo Bump hapo, kwenye kichupo cha 'data': https://nivo.rocks/bump/.

## Programu ya onyesho

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://share.streamlit.io/okld/streamlit-elements-demo/main)

## Msimbo wenye maelezo ya mstari kwa mstari

``` chatu
# Kwanza, tutahitaji uagizaji ufuatao kwa programu yetu.

kuagiza json
import streamt kama st
kutoka kwa Njia ya uingizaji ya pathlib

# Kuhusu Vipengee vya Uboreshaji, tutahitaji vitu hivi vyote.
# Vitu vyote vinavyopatikana na matumizi yameorodheshwa hapo: https://github.com/okld/streamlit-elements#getting-started

kutoka kwa vipengele vya kuleta vipengee vya streamlit, dashibodi, mui, kihariri, midia, uvivu, usawazishaji, nivo

# Badilisha mpangilio wa ukurasa ili kufanya dashibodi kuchukua ukurasa mzima.

st.set_page_config(layout="wide")

na st.sidebar:
    st.title("🗓️ #30DaysOfStreamlit")
    st.header("Siku ya 27 - Vipengee vya Kusambaza")
    st.write("Jenga dashibodi inayoweza kukokotwa na inayoweza kurejeshwa kwa kutumia Vipengee vya Uboreshaji.")
    st.write("---")

    # Bainisha URL ya kicheza media.
    media_url = st.text_input("URL ya Vyombo vya habari", thamani="https://www.youtube.com/watch?v=vIQQR_yq-8I")

# Anzisha data chaguo-msingi ya mhariri wa nambari na chati.
#
# Kwa somo hili, tutahitaji data ya chati ya Nivo Bump.
# Unaweza kupata data nasibu hapo, kwenye kichupo cha 'data': https://nivo.rocks/bump/
#
# Kama utakavyoona hapa chini, kipengele hiki cha hali ya kikao kitasasishwa wakati wetu
Mabadiliko # ya kihariri cha msimbo, na itasomwa na chati ya Nivo Bump ili kuchora data.

ikiwa "data" haiko katika st.session_state:
    st.session_state.data = Njia("data.json").read_text()

# Bainisha mpangilio chaguo-msingi wa dashibodi.
# Gridi ya Dashibodi ina safu wima 12 kwa chaguomsingi.
#
# Kwa habari zaidi juu ya vigezo vinavyopatikana:
# https://github.com/react-grid-layout/react-grid-layout#grid-item-props

mpangilio = [
    Kipengee # cha mhariri kimewekwa katika viwianishi x=0 na y=0, na huchukua safu wima 6/12 na kina urefu wa 3.
    dashibodi.Kipengee("mhariri", 0, 0, 6, 3),
    Kipengee # cha chati kimewekwa katika viwianishi x=6 na y=0, na huchukua safu wima 6/12 na kina urefu wa 3.
    dashibodi.Kipengee("chati", 6, 0, 6, 3),
    Kipengee # cha maudhui kimewekwa katika viwianishi x=0 na y=3, na huchukua safu wima 6/12 na kina urefu wa 4.
    dashibodi.Kipengee("media", 0, 2, 12, 4),
]

# Unda fremu ya kuonyesha vitu.

na vipengele("demo"):

    # Unda dashibodi mpya na mpangilio ulioainishwa hapo juu.
    #
    # draggableHandle ni kiteuzi cha hoja cha CSS ili kufafanua sehemu inayoweza kukokotwa ya kila kipengee cha dashibodi.
    # Hapa, vipengele vilivyo na jina la darasa la 'kuburutwa' vitavutwa.
    #
    # Kwa habari zaidi juu ya vigezo vinavyopatikana vya gridi ya dashibodi:
    # https://github.com/react-grid-layout/react-grid-layout#grid-layout-props
    # https://github.com/react-grid-layout/react-grid-layout#responsive-grid-layout-props

    na dashibodi.Gridi(mpangilio, draggableHandle=".draggable"):

        # Kadi ya kwanza, mhariri wa nambari.
        #
        # Tunatumia kigezo cha 'ufunguo' kutambua kipengee sahihi cha dashibodi.
        #
        # Ili kufanya yaliyomo kwenye kadi yajaze kiotomatiki urefu unaopatikana, tutatumia CSS flexbox.
        # sx ni kigezo kinachopatikana na kila wijeti ya Nyenzo ya UI ili kufafanua sifa za CSS.
        #
        # Kwa habari zaidi kuhusu Kadi, flexbox na sx:
        # https://mui.com/components/cards/
        # https://mui.com/system/flexbox/
        # https://mui.com/system/the-sx-prop/

        with mui.Card(key="editor", sx={"display": "flex", "flexDirection": "column"}):

            # Ili kufanya kichwa hiki kiburuzwe, tunahitaji tu kuweka jina lake la darasa kuwa 'kuburutwa',
            # kama ilivyofafanuliwa hapo juu kwenye dashibodi.Grid's DraggableHandle.

            mui.CardHeader(title="Mhariri", className="draggable")

            # Tunataka kufanya maudhui ya kadi kuchukua urefu wote unaopatikana kwa kuweka thamani ya CSS inayobadilika kuwa 1.
            # Pia tunataka maudhui ya kadi kupungua wakati kadi inapunguzwa kwa kuweka minHeight hadi 0.

            with mui.CardContent(sx={"flex": 1, "minHeight": 0}):

                # Hapa kuna mhariri wetu wa nambari ya Monaco.
                #
                # Kwanza, tunaweka thamani chaguo-msingi kuwa st.session_state.data ambayo tulianzisha hapo juu.
                # Pili, tunafafanua lugha ya kutumia, JSON hapa.
                #
                # Kisha, tunataka kurejesha mabadiliko yaliyofanywa kwa maudhui ya kihariri.
                # Kwa kuangalia hati za Monaco, kuna mali ya onChange ambayo inachukua utendakazi.
                # Chaguo hili la kukokotoa linaitwa kila wakati mabadiliko yanapofanywa, na thamani ya maudhui iliyosasishwa hupitishwa
                # kigezo cha kwanza (cf. onChange: https://github.com/suren-atoyan/monaco-react#props)
                #
                Vipengee # vya Uboreshaji hutoa kazi maalum ya kusawazisha (). Chaguo hili la kukokotoa hutengeneza kiitikio ambacho kitafanya
                # sambaza kiotomatiki vigezo vyake kwa vipengee vya hali ya kikao cha Sawazisha.
                #
                #Mifano
                # --------
                # Unda simu inayorudisha mbele parameta yake ya kwanza kwa kitu cha hali ya kikao kinachoitwa "data":
                # >>> mhariri.Monaco(onChange=sync("data"))
                # >>> chapisha(st.session_state.data)
                #
                # Unda simu inayorudisha mbele parameta yake ya pili kwa kitu cha hali ya kikao kinachoitwa "ev":
                # >>> mhariri.Monaco(onChange=sync(None, "ev"))
                # >>> chapisha(st.session_state.ev)
                #
                # Unda simu inayorudisha mbele vigezo vyake vyote kwa hali ya kikao:
                # >>> mhariri.Monaco(onChange=sync("data", "ev"))
                # >>> chapisha(st.session_state.data)
                # >>> chapisha(st.session_state.ev)
                #
                # Sasa, kuna suala: onChange inaitwa kila wakati mabadiliko yanafanywa, ambayo inamaanisha kila wakati
                # ukiandika herufi moja, programu yako yote ya Kufululiza itaendeshwa tena.
                #
                # Ili kuepusha suala hili, unaweza kuwaambia Vipengee vya Uboreshaji kusubiri tukio lingine kutokea
                # (kama kubofya kitufe) kutuma data iliyosasishwa, kwa kufunga simu yako ya nyuma na lazy().
                #
                # Kwa habari zaidi juu ya vigezo vinavyopatikana vya Monaco:
                # https://github.com/suren-atoyan/monaco-react
                # https://microsoft.github.io/monaco-editor/api/interfaces/monaco.editor.IstandaloneEditorConstructionOptions.html

                mhariri.Monaco(
                    defaultValue=st.session_state.data,
                    lugha="json",
                    onChange=wavivu(sync("data"))
                )

            na mui.CardActions:

                Mhariri wa # Monaco ana uvivu wa kupiga simu kwa onChange, ambayo inamaanisha kuwa hata ukibadilika
                # Maudhui ya Monaco, Streamlit haitaarifiwa moja kwa moja, kwa hivyo haitapakiwa upya kila wakati.
                # Kwa hivyo tunahitaji tukio lingine lisilo la uvivu ili kuanzisha sasisho.
                #
                # Suluhisho ni kuunda kitufe ambacho hupiga simu kwa kubofya.
                # Upigaji simu wetu hauitaji kufanya chochote haswa. Unaweza kuunda tupu
                # Python kazi, au tumia sync() bila hoja.
                #
                # Sasa, kila wakati utabofya kitufe hicho, onClick callback itafutwa, lakini kila nyingine
                # simu za uvivu zilizobadilika wakati huo huo pia zitaitwa.

                mui.Button("Tekeleza mabadiliko", onClick=sync())

        # Kadi ya pili, chati ya Nivo Bump.
        # Tutatumia usanidi wa kisanduku chenye kubadilika kama kadi ya kwanza kurekebisha kiotomatiki urefu wa maudhui.

        with mui.Card(key="chart", sx={"display": "flex", "flexDirection": "column"}):

            # Ili kufanya kichwa hiki kiburuzwe, tunahitaji tu kuweka jina lake la darasa kuwa 'kuburutwa',
            # kama ilivyofafanuliwa hapo juu kwenye dashibodi.Grid's DraggableHandle.

            mui.CardHeader(title="Chati", className="draggable")

            # Kama ilivyo hapo juu, tunataka kufanya maudhui yetu kukua na kupungua mtumiaji anapobadilisha ukubwa wa kadi,
            # kwa kuweka flex hadi 1 na minHeight hadi 0.

            with mui.CardContent(sx={"flex": 1, "minHeight": 0}):

                # Hapa ndipo tutachora chati yetu ya Bump.
                #
                # Kwa zoezi hili, tunaweza tu kurekebisha mfano wa Nivo na kuifanya ifanye kazi na Vipengee vya Kuboresha.
                Mfano # wa Nivo unapatikana kwenye kichupo cha 'code' hapo: https://nivo.rocks/bump/
                #
                # Data inachukua kamusi kama kigezo, kwa hivyo tunahitaji kubadilisha data yetu ya JSON kutoka kwa kamba hadi
                # kamusi ya Python kwanza, na `json.loads()`.
                #
                # Kwa habari zaidi kuhusu chati zingine zinazopatikana za Nivo:
                # https://nivo.rocks/

                nivo.Bump(
                    data=json.loads(st.session_state.data),
                    color={ "scheme": "spectral" },
                    Upana wa mstari=3,
                    activeLineWidth=6,
                    inactiveLineWidth=3,
                    inactiveOpacity=0.15,
                    pointSize=10,
                    activePointSize=16,
                    inactivePointSize=0,
                    pointColor={ "mandhari": "msingi" },
                    pointBorderWidth=3,
                    activePointBorderWidth=3,
                    pointBorderColor={ "kutoka": "serie.color" },
                    axisTop={
                        "Ukubwa wa tiki": 5,
                        "TickPadding": 5,
                        "TickRotation": 0,
                        "legend": "",
                        "legendPosition": "katikati",
                        "legendOffset": -36
                    },
                    axisBottom={
                        "Ukubwa wa tiki": 5,
                        "TickPadding": 5,
                        "TickRotation": 0,
                        "legend": "",
                        "legendPosition": "katikati",
                        "legendOffset": 32
                    },
                    axisLeft={
                        "Ukubwa wa tiki": 5,
                        "TickPadding": 5,
                        "TickRotation": 0,
                        "legend": "cheo",
                        "legendPosition": "katikati",
                        "legendOffset": -40
                    },
                    margin={ "juu": 40, "kulia": 100, "chini": 40, "kushoto": 60 },
                    axisRight=Hakuna,
                )

        # Kipengele cha tatu cha dashibodi, kicheza Media.

        with mui.Card(key="media", sx={"display": "flex", "flexDirection": "column"}):
            mui.CardHeader(title="Media Player", className="draggable")
            with mui.CardContent(sx={"flex": 1, "minHeight": 0}):

                # Kipengele hiki kinatumia ReactPlayer, inasaidia wachezaji wengine wengi zaidi
                # kuliko YouTube. Unaweza kuiangalia hapo: https://github.com/cookpete/react-player#props

                media.Player(url=media_url, width="100%", height="100%", controls=Kweli)

```

## Swali lolote?

Jisikie huru kuuliza swali lolote kuhusu Vipengee vya Kuhuisha au changamoto hii hapo: [Sasisha Mada ya Vipengee](https://discuss.streamlit.io/t/streamlit-elements-build-draggable-and-resizable-dashboards-with-material- chati-za-ui-nivo-na-zaidi/24616)
