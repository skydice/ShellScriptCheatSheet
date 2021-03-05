# 리눅스 쉘에서 데이터를 다룰 때 유용한 팁

### 폴더를 순회하기
```shell
for directory in */; do
    echo $directory
done
```

### 날짜로 된 폴더를 순회하기
```shell
DATE=`date -d 'yesterday' +"%Y-%m-%d"`
START_DATE=`date -d '30 days ago' +"%Y-%m-%d"`

while [ $START_DATE != $DATE ]; do
    if [ -d "Folder_$START_DATE" ]
    then
        do something
    fi
    START_DATE=$(date -I -d "$START_DATE + 1 day")
done
```
