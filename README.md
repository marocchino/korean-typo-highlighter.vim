# KoreanTypoHighlighter

틀린 외래어를 하이라이팅 해줍니다.

이 프로젝트는 [panozzaj/vim-autocorrect](https://github.com/panozzaj/vim-autocorrect)를
참고해 만들었습니다.

## 사용법

`.vimrc`에 밑의 내용을 추가합니다.

```viml
autocmd BufEnter *.md call KoreanTypoHighlight()
```

## 기여하기

1. `yaml` 형식에 맞게 `words.yml`에 단어를 추가하고, 콘솔에서 rake build를
   실행합니다.
2. 커밋해서 pr을 보냅니다.

## To Do

1. 한역을 하는 경우와 안하는 경우를 구별해 사용하도록 하기
