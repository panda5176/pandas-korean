원문: [Getting started](https://pandas.pydata.org/docs/getting_started/index.html)

# 시작하기

## 설치

**콘다(conda)로 작업하시나요?**

판다스(pandas)는 [아나콘다(Anaconda)](https://docs.continuum.io/anaconda/) 배포판의 일부이며 아나콘다나 미니콘다(Miniconda)로 설치할 수 있습니다.

```sh
conda install pandas
```

**pip를 선호하시나요?**

판다스는 [파이파이(PyPI)](https://pypi.org/project/pandas)에서 pip를 통해 설치할 수 있습니다.

```sh
pip install pandas
```

**깊이 있는 설명서요?**

특정 버전을 설치하세요? 소스(source)에서부터 설치하세요? 고급 설치 페이지를 확인하세요.

> [더 배우기](install)

## 판다스 소개

### 판다스는 어떤 종류의 데이터를 다루나요?

스프레드시트(spreadsheets)나 데이터베이스(databases)와 같은 표 데이터(tabular data)로 작업할 때, 판다스가 여러분들을 위해 적합한 도구입니다. 판다스는 여러분이 데이터를 탐색하고, 정리하고, 처리하도록 도울 것입니다. 판다스에서, 데이터 표는 [`DataFrame`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html#pandas.DataFrame)이라고 부릅니다.

![](https://pandas.pydata.org/docs/_images/01_table_dataframe.svg)

> [소개 튜토리얼로](intro_tutorials/01_table_oriented)

> [사용자 안내로](../user_guide/dsintro)

### 표 데이터를 어떻게 읽고 쓰나요?

판다스는 많은 파일 형식 및 데이터 소스와의 통합을 간편하게 지원합니다(csv, excel, sql, json, parquet, ...). 이러한 각 데이터 소스로부터 데이터를 가져오는 것은 접두사 `read_*`가 있는 함수(function)로 제공합니다. 마찬가지로, `to_*` 메서드(methods)는 데이터를 저장하는 데 사용합니다.

![](https://pandas.pydata.org/docs/_images/02_io_readwrite.svg)

> [소개 튜토리얼로](intro_tutorials/02_read_write)

> [사용자 안내로](../user_guide/io)

### 어떻게 표의 일부만 선택하나요?

특정 행이나 열만 선택하거나 필터링(filtering)하세요? 조건에 따라 데이터를 필터링하세요? 판다스에서는 원하시는 데이터를 슬라이싱(slicing), 선택, 추출하는 메서드들을 사용 가능합니다.

![](https://pandas.pydata.org/docs/_images/03_subset_columns_rows.svg)

> [소개 튜토리얼로](intro_tutorials/03_subset_data)

> [사용자 안내로](../user_guide/indexing)

### 판다스에서는 어떻게 플롯을 만드나요?

판다슨느 맷플롯립(Matplotlib)의 힘을 이용해 간편하게 여러분의 데이터를 플로팅(plotting)하는 법을 제공합니다. 여러분은 여러분의 데이터에 해당하는 플롯 유형(산점도, 막대, 상자 그림, ...)을 고르실 수 있습니다.

![](https://pandas.pydata.org/docs/_images/04_plot_overview.svg)

> [소개 튜토리얼로](intro_tutorials/04_plotting)

> [사용자 안내로](../user_guide/visualization)

### 지금 있는 열에서 어떻게 새로운 열을 만드나요?

계산을 하기 위해 여러분 데이터의 모든 행을 반복해서 돌 필요가 없습니다. 열에 대한 데이터 조작은 요소별로(elementwise) 작동합니다. 다른 열에 존재하는 데이터에 기반해 [`DataFrame`](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html#pandas.DataFrame)에 열을 추가하는 것은 간단합니다.

![](https://pandas.pydata.org/docs/_images/05_newcolumn_2.svg)

> [소개 튜토리얼로](intro_tutorials/05_add_columns)

> [사용자 안내로](../user_guide/dsintro#열-선택-추가-삭제)

### 요약 통계량을 어떻게 계산하나요?

기초 통계량(basic statistics, 평균(mean), 중간값(median), 최솟값(min), 최댓값(max), 수(counts), ...)는 쉽게 계산 가능합니다. 이러한 집계(aggregations)나 사용자 정의 집계는 전체 데이터 세트나 데이터의 슬라이딩 윈도우(sliding window)에도 적용할 수 있고, 또는 범주(categories)로 묶을 수도 있습니다. 후자는 분할-적용-병합(split-apply-combine) 접근으로도 알려져 있습니다.

![](https://pandas.pydata.org/docs/_images/06_groupby.svg)

> [소개 튜토리얼로](intro_tutorials/06_calculate_statistics)

> [사용자 안내로](../user_guide/groupby)

### 표의 배열을 어떻게 재배열하나요?

다양한 방법으로 데이터 표의 구조를 바꾸세요. 여러분은 데이터 표를 넓은(wide) 형식에서 긴/깔끔한(long/tidy) 형식으로 [`melt()`](https://pandas.pydata.org/docs/reference/api/pandas.melt.html#pandas.melt)할 수도 있고, 긴 형식에서 넓은 형식으로 [`pivot()`](https://pandas.pydata.org/docs/reference/api/pandas.pivot.html#pandas.pivot)할 수도 있습니다. 내장된 집계로, 피벗 테이블(pivot table)을 단일 명령으로 생성합니다.

![](https://pandas.pydata.org/docs/_images/07_melt.svg)

> [소개 튜토리얼로](intro_tutorials/07_reshape_table_layout)

> [사용자 안내로](../user_guide/reshaping)

### 어떻게 여러 표에서 데이터를 결합하나요?

데이터베이스와 비슷한 조인/병합(join/merge) 연산이 여러 표의 데이터를 위해 제공되므로, 열 방향(column wise)과 행 방향(row wise)으로 여러 표를 결합할 수 있습니다.

![](https://pandas.pydata.org/docs/_images/08_concat_row.svg)

> [소개 튜토리얼로](intro_tutorials/08_combine_dataframes)

> [사용자 안내로](../user_guide/merging)

### 시계열 데이터를 어떻게 다루나요?

판다스에는 시계열(time series)를 위한 훌륭한 지원이 있으며, 날짜, 시간, 시간 인덱스(time-indexed) 데이터와 작업하기 위한 광범위한 도구 세트를 가지고 있습니다.

> [소개 튜토리얼로](intro_tutorials/09_timeseries)

> [사용자 안내로](../user_guide/timeseries)

### 텍스트 데이터를 어떻게 조작하나요?

데이터 세트는 수치(numerical) 데이터만 담지는 않습니다. 판다스는 텍스트(textual) 데티러를 정리하고 그로부터 유용한 정보를 추출하기 위한 넓은 범위의 함수를 제공합니다.

> [소개 튜토리얼로](intro_tutorials/10_text_data)

> [사용자 안내로](../user_guide/text)

## 어디서 오셨는지...

표 데이터를 조작하는 다른 소프트웨어에 친숙하신가요? 여러분이 이미 알고있는 소프트웨어와 비교하면서 판다스의 같은 연산을 배우세요.

### R

R 프로그래밍 언어는 `data.frame` 자료 구조(data structure)와, 판다스와 비슷하게 편리한 데이터 처리 기능을 위해 `data.frame`을 사용하고 확장하는, tidyverse같은 여러 패키지(packages)를 제공합니다.

> [더 배우기](comparison/comparison_with_r)

### SQL

`SELECT`, `GROUP BY`, `JOIN` 등에 이미 익숙하신가요? 대부분의 이러한 SQL 연산은 판다스에도 같은 것이 있습니다.

> [더 배우기](comparison/comparison_with_sql)

### STATA

STATA 통계 소프트웨어 제품군에 포함된 `data set`은 판다스 `DataFrame`에 해당합니다. STATA에서 알려진 많은 연산은 판다스에도 같은 것이 있습니다.

> [더 배우기](comparison/comparison_with_stata)

### Excel

엑셀(Excel)이나 다른 스프레드시트(spreadsheet) 프로그램 사용자들은 많은 개념을 판다스로 이전할 수 있음을 알게 될 것입니다.

> [더 배우기](comparison/comparison_with_spreadsheets)

### SAS

SAS 통계 소프트웨어 제품군도 판다스 `DataFrame`에 해당하는 `data set`을 제공합니다. 또한 SAS의 벡터화된(vectorized) 연산, 필터링, 문자열(string) 처리 연산, 그리고 더 많은 것들이 판다스에 비슷한 함수가 있습니다.

> [더 배우기](comparison/comparison_with_sas)

## 튜토리얼

판다스 기능에 대한 빠른 개요는, [판다스까지 10분](../user_guide/10min)을 보세요.

또는 판다스와 함께 데이터를 조작하기 위한 간결한 안내를 위해 판다스 [컨닝 페이퍼](https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf)를 참고할 수도 있습니다.

커뮤니티에서는 온라인으로 가능한 넓은 범위의 튜토리얼을 생산합니다. 일부 자료는 커뮤니티가 기여한 [커뮤니티 튜토리얼](tutorials)에 등록되어 있습니다.
