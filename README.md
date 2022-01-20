# Python-Visualization
data visualization of dataset using seaborn 
---
jupyter:
  colab:
    name: Untitled0.ipynb
  kernelspec:
    display_name: Python 3
    name: python3
  language_info:
    name: python
  nbformat: 4
  nbformat_minor: 0
---

::: {.cell .code id="3NcUyXbShsts"}
``` {.python}
    
```
:::

::: {.cell .code execution_count="1" colab="{\"base_uri\":\"https://localhost:8080/\"}" id="hFmYT1eEmR0a" outputId="233a146a-c27a-41b6-c0c2-80a4f4f5fae7"}
``` {.python}
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt

iris=sns.load_dataset("iris")
iris.head(10)
iris.describe()
iris.info()
sns.jointplot(x="sepal_length" , y="sepal_width",data=iris)

```

::: {.output .stream .stdout}
    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 150 entries, 0 to 149
    Data columns (total 5 columns):
     #   Column        Non-Null Count  Dtype  
    ---  ------        --------------  -----  
     0   sepal_length  150 non-null    float64
     1   sepal_width   150 non-null    float64
     2   petal_length  150 non-null    float64
     3   petal_width   150 non-null    float64
     4   species       150 non-null    object 
    dtypes: float64(4), object(1)
    memory usage: 6.0+ KB
:::

::: {.output .execute_result execution_count="1"}
    <seaborn.axisgrid.JointGrid at 0x7f682aa2ac90>
:::

::: {.output .display_data}
![](vertopal_84c16ec5a3904955bf2f8e5594c952f5/b1637685f7292621d4228c0733d34096a8bfb97f.png)
:::
:::

::: {.cell .code execution_count="14" colab="{\"height\":743,\"base_uri\":\"https://localhost:8080/\"}" id="mCevhIa7nKa6" outputId="6f6340b3-5e39-4b91-a7ad-e1d49938c923"}
``` {.python}
sns.pairplot(iris)

```

::: {.output .execute_result execution_count="14"}
    <seaborn.axisgrid.PairGrid at 0x7f6303681950>
:::

::: {.output .display_data}
![](vertopal_84c16ec5a3904955bf2f8e5594c952f5/d59a5054ac46b1d0b8d1f30422d675a4f9be2168.png)
:::
:::

::: {.cell .code execution_count="16" colab="{\"height\":283,\"base_uri\":\"https://localhost:8080/\"}" id="xwaYGTzS2tB1" outputId="064e7e94-6dfb-4a74-a14d-ac4b1ec241ae"}
``` {.python}
sns.boxplot(data=iris)
```

::: {.output .execute_result execution_count="16"}
    <matplotlib.axes._subplots.AxesSubplot at 0x7f6303614ed0>
:::

::: {.output .display_data}
![](vertopal_84c16ec5a3904955bf2f8e5594c952f5/134717b1c8ba6b3993a650e27eda4bdb21e278e2.png)
:::
:::

::: {.cell .code execution_count="18" colab="{\"height\":283,\"base_uri\":\"https://localhost:8080/\"}" id="Rnp-hMnv3K86" outputId="7fefe519-6232-4557-cafd-fdf89e89dfc0"}
``` {.python}
sns.violinplot(data=iris)
```

::: {.output .execute_result execution_count="18"}
    <matplotlib.axes._subplots.AxesSubplot at 0x7f62fe5f67d0>
:::

::: {.output .display_data}
![](vertopal_84c16ec5a3904955bf2f8e5594c952f5/5290502efe0a1aab6f79d7142eec90cb30ea96e6.png)
:::
:::

::: {.cell .code execution_count="20" colab="{\"height\":442,\"base_uri\":\"https://localhost:8080/\"}" id="Men55_Yx3cFx" outputId="62971c34-5191-4033-fc2f-3c018a388e74"}
``` {.python}
sns.swarmplot(data=iris)
```

::: {.output .stream .stderr}
    /usr/local/lib/python3.7/dist-packages/seaborn/categorical.py:1296: UserWarning: 7.3% of the points cannot be placed; you may want to decrease the size of the markers or use stripplot.
      warnings.warn(msg, UserWarning)
    /usr/local/lib/python3.7/dist-packages/seaborn/categorical.py:1296: UserWarning: 32.7% of the points cannot be placed; you may want to decrease the size of the markers or use stripplot.
      warnings.warn(msg, UserWarning)
    /usr/local/lib/python3.7/dist-packages/seaborn/categorical.py:1296: UserWarning: 9.3% of the points cannot be placed; you may want to decrease the size of the markers or use stripplot.
      warnings.warn(msg, UserWarning)
    /usr/local/lib/python3.7/dist-packages/seaborn/categorical.py:1296: UserWarning: 26.0% of the points cannot be placed; you may want to decrease the size of the markers or use stripplot.
      warnings.warn(msg, UserWarning)
:::

::: {.output .execute_result execution_count="20"}
    <matplotlib.axes._subplots.AxesSubplot at 0x7f62fe4a8710>
:::

::: {.output .display_data}
![](vertopal_84c16ec5a3904955bf2f8e5594c952f5/a12a5a7d41ff79f0f3dbb992076a27cd37e4049e.png)
:::
:::

::: {.cell .code execution_count="22" colab="{\"height\":283,\"base_uri\":\"https://localhost:8080/\"}" id="OmcorSWz31GU" outputId="6b0d5764-cea7-4f99-d3d1-839872d93f57"}
``` {.python}
sns.barplot(data=iris)
```

::: {.output .execute_result execution_count="22"}
    <matplotlib.axes._subplots.AxesSubplot at 0x7f62fe380c50>
:::

::: {.output .display_data}
![](vertopal_84c16ec5a3904955bf2f8e5594c952f5/79d31ae6ce7edfadc61b8f7040c948550266ab71.png)
:::
:::

::: {.cell .code execution_count="24" colab="{\"height\":283,\"base_uri\":\"https://localhost:8080/\"}" id="vg5xXAl74Fmu" outputId="dd1f8fcb-a855-4c0e-d07c-2385d112ec14"}
``` {.python}
sns.countplot(data=iris)
```

::: {.output .execute_result execution_count="24"}
    <matplotlib.axes._subplots.AxesSubplot at 0x7f62fe2e2790>
:::

::: {.output .display_data}
![](vertopal_84c16ec5a3904955bf2f8e5594c952f5/de5bdcef009d8553c748e306a1af18d242683b6e.png)
:::
:::

::: {.cell .code execution_count="27" colab="{\"height\":283,\"base_uri\":\"https://localhost:8080/\"}" id="l9H5EmTy5w4z" outputId="41460cc8-5c07-466c-f360-97e3d1dfae04"}
``` {.python}
sns.kdeplot(data=iris)
```

::: {.output .execute_result execution_count="27"}
    <matplotlib.axes._subplots.AxesSubplot at 0x7f62fe1eeb50>
:::

::: {.output .display_data}
![](vertopal_84c16ec5a3904955bf2f8e5594c952f5/569489ba0d05c0446f015cfae4ea3d8786b2ba65.png)
:::
:::

::: {.cell .code execution_count="33" colab="{\"height\":297,\"base_uri\":\"https://localhost:8080/\"}" id="1R64yRqy6m0x" outputId="7e76a2f4-cc52-44ce-f65b-e1d0ba742f61"}
``` {.python}
sns.kdeplot(iris["sepal_length"])
```

::: {.output .execute_result execution_count="33"}
    <matplotlib.axes._subplots.AxesSubplot at 0x7f62f9983250>
:::

::: {.output .display_data}
![](vertopal_84c16ec5a3904955bf2f8e5594c952f5/ca57485a3148ee31b6c7210af1775a770c1ef9d0.png)
:::
:::
