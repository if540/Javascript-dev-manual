# 附件、如何在 Javascript 裡產生 *.d.ts 檔?

雖然 TypeScript 會自動判斷可辨識的類型，理想還是要搭配 JSdoc 來完整描

script

```shell
tsc -p tsconfig.build.types.json
```

tsconfig.build.types.json

```json
{
    "compilerOptions": {
        "target": "esnext",
        "module": "esnext",
        "moduleResolution": "node",
        "lib": ["es2017", "dom"],
        "allowJs": true,
        "checkJs": true,
        "strict": false,
        "noImplicitThis": true,
        "alwaysStrict": true,
        // "types": ["mocha"],
        "esModuleInterop": true,
        "noEmit": false,
        "declaration": true,
        "emitDeclarationOnly": true,
        "outDir": "",
        // "outFile": "main.d.ts"
    },
    "include": ["src/moduleName.js"]
}
```

學習文章:

- [Generating TypeScript Definition Files from JavaScript](https://dev.to/open-wc/generating-typescript-definition-files-from-javascript-5bp2)
- [宣告檔案](https://willh.gitbook.io/typescript-tutorial/basics/declaration-files#jiang-xuan-gao-dang-an-he-yuan-shi-ma-fang-zai-yi-qi)
