## 拼音搜索

```js
import PinyinMatch from 'pinyin-match'
export default (data, keyWord, props) => {
  props = Array.isArray(props) ? props : [props]
  return keyWord ? data.filter(v => props.some(prop => PinyinMatch.match(v[prop], keyWord))) : data
}
```