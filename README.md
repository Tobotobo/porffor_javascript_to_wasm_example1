# porffor_javascript_to_wasm_example1

## 概要
以下の記事を見て「Porffor」を試してみた。  
→　所感(2024/8/27)  
　　公式に書かれている通りで、今のところ何も面白いことはできなかった。  
　　今後に期待🙆

Publickey  
JavaScript/TypeScriptからWebAssemblyやネイティブバイナリを生成するコンパイラ「Porffor」の開発が加速へ、開発者がフルタイムで取り組み  
https://www.publickey1.jp/blog/24/javascripttypescriptwebassemblyporffor.html  

Porffor  
https://porffor.dev/  
https://github.com/CanadaHonk/porffor  
Porffor は、JS コードを WebAssembly またはネイティブに事前にコンパイルする、ユニークな JS エンジン/コンパイラ/ランタイムです。  
現時点では制限があり、本格的な使用ではなく、研究を目的としています。  

## 詳細

### 環境
Windows10 Pro x64
```
> node --version
v21.4.0
> npm --version
10.2.4
```

### インストール
```
npm install -g porffor@latest
```
```
> porf --version
0.39.2+c58905509
```

### 実行
```
> porf hello.js
Hello Porffor!
```

### Wasm にコンパイル
```
porf wasm hello.js hello.wasm
```

### Native コンパイル
```
porf native hello.js hello.exe
```

エラーで生成できず...
```
> porf native hello.js hello.exe
       3ms  parsed
     178ms  generated wasm
     200ms  optimized
      65ms  assembled
         \  compiling Wasm to C...TypeError: Cannot read properties of undefined (reading 'constructor')
         /  compiling Wasm to C...
```