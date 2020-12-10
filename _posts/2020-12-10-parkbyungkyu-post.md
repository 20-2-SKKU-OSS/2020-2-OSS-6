---
layout: post
title: 박병규- 제목 키워드 검색기능 추가
date: 2020-12-10 16:00:00 +0900
category: Process
---

## 1. 키워드를 입력받아 제목에서 찾는 기능

이 코드의 원래 기능은 크롤링을 할 때 기간, 카테고리를 정하면 기사를 모두 크롤링 하는 것,
15번 이슈를 통해 사용자가 키워드를 입력하면 제목에 해당 키워드가 포함된 기사들만 .csv 파일에 저장하도록 하는 기능 추가
    
```python
def get_keyword(self):
    keyword = 'initvalue'
    ynkeyword = input("기사 제목 키워드 찾기 기능을 사용하시겠습니까? (y/n) :")
    if ynkeyword == "n" or ynkeyword == "N":
        return keyword
    elif ynkeyword == "y" or ynkeyword == "Y":
        keyword = input("원하는 키워드를 입력해주세요 :")
        return keyword
    else:
        print("invalid input")
        return keyword
```

## 2. 키워드가 포함된 기사만 엑셀 파일에 쓰는 기능

```python
    if self.keyword == 'initvalue':
        wcsv = writer.get_writer_csv()
        wcsv.writerow([news_date, category_name, text_company, text_headline, text_sentence, content_url])
    else:
        headline_to_words = text_headline.split()
        if headline_to_words.index(self.keyword) >= 0:
            wcsv = writer.get_writer_csv()
            wcsv.writerow([news_date, category_name, text_company, text_headline, text_sentence, content_url])
```

## 2. 프로젝트 read.me 수정
![readmescreen](../assets/img/readmechange.JPG)
