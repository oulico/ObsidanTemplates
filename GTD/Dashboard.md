
# [[Capture]] 
```tasks 
description does not include @work 
description does not include @home 
filter by function task.file.filename === "Capture.md"
not done
```
---

## [[Work]]

```tasks 
description includes @work 
description does not include @later
filter by function task.file.filename !== "Logs.md"
filter by function task.file.filename !== "Old.md"
sort by due
not done 
```
---

## [[GTD/Home]]
```tasks 
description includes @home 
not done 
```
---

## Scheduled Tasks - Today
```tasks 
scheduled today
not done 
```
---

## Due Tasks - This Week
```tasks 
not done
due AFTER yesterday
due BEFORE tomorrow
```
---

## Work Done

> 매주 금요일 완료된 일감을 확인하고 Logs로 보냅니다.

```tasks
filter by function task.file.filename !== "Logs.md"
filter by function task.file.filename !== "Old.md"
filter by function task.file.folder !== "GTD/Projects/Trashbin"
description does not include @home
done after this sunday
group by done
```
---

## My Status

### 미라클 모닝 현황
> 일찍일어나는 날이 연속될 경우 기록이 누적되어 그래프에 표현됩니다.

```dataviewjs

const earlyRisePages = dv.pages('#DailyReflection') .sort(page => page.file.cday, 'asc');

var labels = [],
	streakCount = 0,
	streaks = [];	

earlyRisePages.forEach(note => {
	labels.push(note.title.slice(9,));

	if (note.earlyRise === true) {
	streakCount += 1;
	} else {
	streakCount = 0;
	}
	streaks.push(streakCount);
});

const chartData = {
	type: 'line',
	data: {
		labels: labels,
		datasets: [{
			label: '미라클 모닝 누적 그래프',
			data: streaks,
			borderWidth: 1,
			fill: true,
			tension: 0.3
		}]	
	},
	options: {
		scales: {
			y: {
				beginAtZero: true,
				ticks: {
				stepSize: 1
				}
			}
		}
	}	
};

window.renderChart(chartData, this.container)

```

### 현재 읽는 책
> 현재 읽는 책과 진행률

```dataview 
TABLE without id file.link AS "Title", 
	("![](" + cover + ")") as Cover, 
	("![progress + " + (round((currentPage/totalPage)*100)) + " %](https://progress-bar.dev/" +(round((currentPage/totalPage)*100)) + "/)") AS Progress,
	publish as "Year", 
	"by " + author as Author 
FROM #BookSummary 
WHERE readingStatus = "reading" 
SORT Progress desc
```

### 현재 진행중인 프로젝트

> 현재 GTD로 관리중인 프로젝트의 목록입니다.
```dataviewjs
dv.table(["프로젝트명", "진행률", "수정일"],
  dv.pages('"GTD/Projects"')
    .map(page => {
      const tasks = page.file.tasks || [];
      const totalTasks = tasks.length;
      const completedTasks = tasks.filter(task => task.checked).length;
      const doneRate = totalTasks > 0 ? Math.round((completedTasks / totalTasks) * 100) : 100;

      return [
        page.file.link,
        `![progress + ${doneRate} %](https://progress-bar.dev/${doneRate}/)`,
        page.file.mday
      ];
    })
);


```

