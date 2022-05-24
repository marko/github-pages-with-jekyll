---
title: Flutter vertical spacing
date: 2022-05-24
---

```dart
/// Inserts a [SizedBox] of height [gap] between each [Widget] in [children]
List<Widget> verticalSpacing(double gap, Iterable<Widget> children) {
  return children
      .expand((item) sync* {
        yield SizedBox(height: gap);
        yield item;
      })
      .skip(1)
      .toList();
}
```

