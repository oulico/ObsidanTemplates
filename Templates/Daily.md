---
title: 데일리 노트 - {{date}}
date:
  - "{{date}}"
tags:
  - DailyReflection
  - SelfImprovement
  - MentalHealth
---

```toc
```
## 오늘의 작업

```dataviewjs
var dateformat = "YYYY-MM-DD HH:mm"; 
if (dv.current().dateformat) { dateformat = dv.current().dateformat; } 
dv.table(["파일명", "생성일", "수정일"], dv.pages() .where(p => p.file.cday.equals(dv.current().file.day) || p.file.mday.equals(dv.current().file.day)) .sort(p => p.file.mtime, 'asc') .map(p => [ p.file.link,  moment(p.file.ctime.toString()).format(dateformat),moment(p.file.mtime.toString()).format(dateformat), ]) );
```
## 오늘의 목표

{{오늘 달성하고자 하는 개인적이거나 직업적인 목표를 기록하세요.}}

## 감사 일기

- {{오늘 있었던 긍정적인 경험이나 감사한 일들을 나열하세요.}}

## 오늘의 성과

{{오늘 달성한 목표나 이룬 성과를 기록하세요.}}

## 오늘의 학습

{{오늘 배운 새로운 지식이나 기술, 읽은 책이나 기사 등에서 얻은 인사이트를 기록하세요.}}

## 감정 일기
> 사건 - 생각 - 기분 순으로 구분하여 기록하세요.

{{오늘 느낀 주요 감정들과 그 원인이 된 사건이나 생각을 기록하세요.}}

## 내일을 위한 계획

{{내일의 목표와 계획을 미리 기록하여 준비하세요.}}

## 추가 노트

{{오늘의 노트에 추가하고 싶은 기타 사항을 자유롭게 기록하세요.}}
