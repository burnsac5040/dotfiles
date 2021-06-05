# python-sspipe --
{:data-section="shell"}
{:data-date="May 21, 2021"}
{:data-extra="Um Pages"}

## SYNOPSIS
Piping in Python

## OPTIONS
Simple function call
`"hello world!" \                                                 | p(print)`                                                                                            | `X = "hello world!"`<br>`print(X)` |                                                                           |                                                         |                                                                                                                                                                |                                                                                                                        |
| Function call<br>with extra args                                  | `"hello" \                                                                                           | p(print, "world", end='!')`        | `X = "hello"`<br>`print(X, "world", end='!')`                             |                                                         |                                                                                                                                                                |                                                                                                                        |
| Explicitly positioning<br>piped argument<br>with `px` placeholder | `"world" \                                                                                           | p(print, "hello", px, "!")`        | `X = "world"`<br>`print("hello", X, "!")`                                 |                                                         |                                                                                                                                                                |                                                                                                                        |
| Chaining pipes                                                    | `5 \                                                                                                 | px + 2 \                           | px ** 5 + px \                                                            | p(print)`                                               | `X = 5`<br>`X = X + 2`<br>`X = X ** 5 + X`<br>`print(X)`                                                                                                       |                                                                                                                        |
| Tailored behavior<br>for builtin `map`<br>and `filter`            | `(`<br>`  range(5)`<br>`  \                                                                          | p(filter, px % 2 == 0)`<br>`  \    | p(map, px + 10)`<br>`  \                                                  | p(list) \                                               | p(print)`<br>`)`                                                                                                                                               | `X = range(5)`<br>`X = filter((lambda x:x%2==0),X)`<br>`X = map((lambda x: x + 10), X)`<br>`X = list(X)`<br>`print(X)` |
| NumPy expressions                                                 | `range(10) \                                                                                         | np.sin(px)+1 \                     | p(plt.plot)`                                                              | `X = range(10)`<br>`X = np.sin(X) + 1`<br>`plt.plot(X)` |                                                                                                                                                                |                                                                                                                        |
| Pandas support                                                    | `people_df \                                                                                         | px.loc[px.age > 10, 'name']`       | `X = people_df`<br>`X.loc[X.age > 10, 'name']`                            |                                                         |                                                                                                                                                                |                                                                                                                        |
| Assignment                                                        | `people_df['name'] \                                                                                 | = px.str.upper()`                  | `X = people_df['name']`<br>`X = X.str.upper()`<br>`people_df['name'] = X` |                                                         |                                                                                                                                                                |                                                                                                                        |
| Pipe as variable                                                  | `to_upper = px.strip().upper()`<br>`to_underscore = px.replace(' ', '_')`<br>`normalize = to_upper \ | to_underscore`<br>`"  ab cde " \   | normalize \                                                               | p(print)`                                               | `_f1 = lambda x: x.strip().upper()`<br>`_f2 = lambda x: x.replace(' ','_')`<br>`_f3 = lambda x: _f2(_f1(x))`<br>`X = " ab cde "`<br>`X = _f3(X)`<br>`print(X)` |                                                                                                                        |
| Builtin<br>Data Structures                                        | `2 \                                                                                                 | p({px-1: p([px, p((px+1, 4))])})`  | `X = 2`<br>`X = {X-1: [X, (X+1, 4)]}`                                     |                                                         |                                                                                                                                                                |                                                                                                                        |