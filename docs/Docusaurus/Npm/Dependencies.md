---

sidebar_label: 'Dependencies vs  peerDependencies'
sidebar_position: 2

---

# Dependencies vs  peerDependencies

what is npm install xxxx --legacy-peer-deps?

## dependencies

```gherkin=
.
├── helloWorld
│   └── node_modules
│       ├── packageA
│       ├── plugin1
│       │   └── nodule_modules
│       │       └── packageA
│       └── plugin2
│       │   └── nodule_modules
│       │       └── packageA

```

從上面的依賴圖可以看出，helloWorld本身已經安裝了一次packageA，但因為因為在 plugin1和plugin2中的dependencies也聲明了packageA，所以最後packageA 會被安裝三次，有兩次安裝是冗餘的。

## peerDependency

而peerDependency就可以避免類似的核心依賴函式庫被重複下載的問題。如果在plugin1 和plugin2 的package.json中使用peerDependency來宣告核心依賴函式庫，例如：

```gherkin=
.
├── helloWorld
│   └── node_modules
│       ├── packageA
│       ├── plugin1
│       └── plugin2
```

### --legacy-peer-deps

--legacy-peer-deps標誌是在v7中引入的，目的是繞過peerDependency自動安裝；它告訴NPM 忽略項目中引入的各個modules之間的相同modules但不同版本的問題並繼續安裝，保證各個引入的依賴之間對自身所使用的不同版本modules共存。

【前端开发技巧】npm install xxxx --legacy-peer-deps到底做了些什么？ 稀土掘金
https://juejin.cn/post/6971268824288985118
