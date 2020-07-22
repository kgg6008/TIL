# 이슈 발생 사항

## AutoModelForSequenceClassification import issue
- 이슈 일자 : 2020-07-22
- 실행코드
	``` python
	from transformers import AutoModelForSequenceClassification, AutoTokenizer
	model = AutoModelForSequenceClassification.from_pretrained('bert-base-cased')
	```
- error
	```bash
	---------------------------------------------------------------------------
	ImportError                               	Traceback (most recent call last)
	<ipython-input-9-478d30a810b9> in <module>
	----> 1 from transformers import AutoModelForSequenceClassification, AutoTokenizer
      2 model = AutoModelForSequenceClassification.from_pretrained('bert-base-cased')

	ImportError: cannot import name 'AutoModelForSequenceClassification' from 'transformers' (/Users/h/opt/anaconda3/lib/python3.7/site-packages/transformers/__init__.py)
	```
- 아래와 같이 실행하니 돌아감
- 이유는 모르겠음
	```python
	from transformers import TFAutoModelForSequenceClassification, AutoTokenizer
	model = TFAutoModelForSequenceClassification.from_pretrained('bert-base-cased')
	```
