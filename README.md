# autocorrect-ko-vim

번역할 때 자주 틀리는 단어를 Abolish에 넣습니다.
넣긴 합니다만 cjk 문제인지 교정될 때와 안될 때가 있어서 일단은 틀린 단어를
하이라이팅하게 해두었습니다.

이 프로젝트는 [panozzaj/vim-autocorrect](https://github.com/panozzaj/vim-autocorrect)를
참고해 만들었습니다.

## 사용법

```viml
autocmd BufEnter *.md call AutoCorrectKo()
```

## 기여하기

1. `yaml` 형식에 맞게 `words.yml`에 단어를 추가하고, 콘솔에서 rake build를
   실행합니다.
2. 커밋해서 pr을 보냅니다.

## To Do

1. 한역을 하는 경우와 안하는 경우를 구별해 사용하도록 하기
