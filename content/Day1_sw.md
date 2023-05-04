# Kuweka mazingira ya maendeleo ya ndani

Kabla ya kuanza kuunda programu za Kuhuisha, itatubidi kwanza tuweke mazingira ya usanidi.

Wacha tuanze kwa kusanikisha na kuweka mazingira ya conda.

## **Sakinisha conda**

- Sakinisha `conda` kwa kwenda kwa <https://docs.conda.io/en/latest/miniconda.html> na uchague mfumo wako wa uendeshaji (Windows, Mac au Linux).
- Pakua na uendeshe kisakinishi ili kusakinisha `conda`.

## **Tengeneza mazingira mapya ya konda**

Sasa kwa kuwa umeweka conda, wacha tuunde mazingira ya conda ya kudhibiti utegemezi wote wa maktaba ya Python.

Ili kuunda mazingira mapya na Python 3.9, ingiza yafuatayo:

```bash
conda create -n stenv python=3.9
```

ambapo `create -n stenv` itaunda mazingira ya conda yenye jina `stenv` na `python=3.9` itasanidi mazingira ya conda na toleo la Python 3.9.

## **Wezesha mazingira ya conda**

Ili kutumia mazingira ya conda ambayo tulikuwa tumeunda ambayo yanaitwa `stenv`, ingiza yafuatayo kwenye safu ya amri:

```bash
conda kuamsha stenv
```

## **Sakinisha maktaba ya Kufululiza**

Sasa ni wakati wa kusakinisha maktaba ya `streamlit`:

```bash
pip install streamlit
```

## **Inazindua programu ya onyesho la Kuhuisha**

Ili kuzindua programu ya onyesho la Kuhuisha (Kielelezo 1) aina:

```bash
streamlit hello
```
