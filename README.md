# 1. Index or insert position of element in sorted array.


```javascript
const index = (arr: number[], target: number): number => {
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] === target) return i;
    if (arr[i] > target) return i;
  }
  return arr.length;
};

console.log(index([1, 3, 5, 6], 2));
```

# 2. Search string in list follow pattern.

```javascript
// 2:
// 2.1:
const search1 = (list: string[], pattern: string): string[] => {
  return list.filter((item) => item.startsWith(pattern));
};

// 2.2:
const same = (str: string, pattern: string): boolean => {
  for (let i = 0; i < pattern.length; i++) {
    if (str[i] !== pattern[i]) return false;
  }

  return true;
};

const search2 = (list: string[], pattern: string): string[] => {
  const result: string[] = [];
  for (let i = 0; i < list.length; i++) {
    if (same(list[i], pattern)) {
      result.push(list[i]);
    }
  }

  return result;
};

const list = [
  'tranvando',
  'nguyenvando',
  'nguyentienhung',
  'nguyentienlinh',
  'tranvanba',
  'phamngulao',
];
const pattern = 'nguyen';

console.log(search1(list, pattern));
console.log(search2(list, pattern));
```
 
 
