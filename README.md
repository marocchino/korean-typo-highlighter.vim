# autocorrect-ko-vim

자주 틀리는 단어를 자동 교정해 줍니다.

이 프로젝트는 [panozzaj/vim-autocorrect](https://github.com/panozzaj/vim-autocorrect)를
참고해 만들었습니다.


## 사용법

```viml
autocmd BufEnter *.md call AutoCorrectKo()
```

## 기여하기

1. `yaml`형식에 맞게 `words.yml`에 단어를 추가하고, 콘솔에서 rake build를
   실행합니다.
2. 커밋해서 pr을 보냅니다.

## TODO

1. 한역을 하는 경우와 안하는 경우를 구별해 사용하도록 하기
