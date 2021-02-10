* 용량
  - 고용량 파일 탐색: `find ./ -type d -size +256k` <- 용량 알아서 조절하기
  - 현위치 폴더 별 용량 확인: `du -hs * | sort -rh | head -20`
- 휴지통 비우기: `cd ~/.local/share/Trash/files; rm -rf *`

* 개수
  - 현재 폴더 이하 파일개수 세기: `find . -type f | wc -l`
  - 현 위치에서 폴더 별 파일개수 확인: 아래 코드 확인

```
for x in `find . -maxdepth 2 -mindepth 2 -type d -print`  
do
echo $x, `find $x -type f|wc -l`;
done
```
