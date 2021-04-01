
## 获取字典

```js
    getDictionary (data, key, value) {
      const result = {}
      data.forEach(v => {
        const realykey = v[key]
        result[realykey] = v[value]
      })
      return result
    }
```
## groupBy

```js
  groupBy (data, params) {
      const groups = {}
      data.forEach(v => {
        const group = JSON.stringify(v[params])
        groups[group] = groups[group] || []
        groups[group].push(v)
      })
      return groups
    }
```

## 数组去重

```js
  unique (arr) {
      return Array.from(new Set(arr))
}
```
