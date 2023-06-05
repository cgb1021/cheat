```
const parse = (time: number): string => {
  if (!time || time < 0) {
    return '0:0'
  }
  const hour = Math.floor(time / 3600)
  const minite = Math.floor((time - hour * 3600) / 60)
  const second = time % 60
  const str = `${minite}:${second}`
  if (hour) {
    return `${hour}:` + str
  }
  return str
}
```
