---
title: [用 Python 理財：打造小資族選股策略] 簡介與環境架設
published: true
---
## 簡介

### 目標

1. 學習選股技巧
2. 用程式減少看盤時間
3. 利用量化投資，穩定獲利

### 何謂量化投資?

擬定投資策略(這裡通常指的是選取某種指標),並將其寫成程式,讓其可以自動的依照你的策略去進行買賣,進而達成獲利的一種投資方式.我們可以從該定義看出,要做量化投資需要以下的能力:
1. 金融知識:例如可用來觀察公司的財報,以用來擬定投資策略
2. 統計知識:例如可用來分析歷史數據,整理出某種投資指標
3. 程式能力:有辦法將投資策略轉化成自動化程式

### 自行打造股票分析軟體

1. 讓python自動抓取股票的股價、月報、財報
2. 學習財務數據背後所代表的含意
3. 利用python製作多種指標，做為選股買賣的依據
4. 結合多種指標，建構一個可以長期獲利的策略

## 環境架設

### 安裝`virtualenv` (在linux環境)

預設已經先安裝好`python3`了,接下來安裝`pip3`:

```
sudo apt-get install python3-pip
```

就可以利用`pip3`來安裝`virtualenv`:

```
pip3 install virtualenv
```

使用`virtualenv`的好處是在不同的虛擬環境中,可以使用不同版本的python套件,而不會發生衝突.

**使用方法**

1. 創建虛擬環境

```
virtualenv -p /usr/bin/python3 firstEnv
```

2. 啟動虛擬環境

```
source firstEnv/bin/activate
```

使用`pip3 list`可以查詢有哪些安裝的套件

3. 關閉虛擬環境

```
deactivate
```

### 安裝jupyter notebook

```
pip3 install jupyter
```

如果出現`command not found`,那是因為`jupyter-notebook`指令放在`~/.local/bin`目錄中,所以需要將其加入到環境變數,方法為在`~/.bashrc`檔案中加入一行:

```
export PATH="$PATH:~/.local/bin"
```

接著

```
source ~/.bashrc
```

**使用方法**

```
jupyter-notebook
```

然後在瀏覽器URL的地方輸入`http://localhost:8888/`,就可以看到`jupyter notebook`的使用環境.


