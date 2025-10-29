# 输入拓展

```c++
template <typename T>
std::istream& operator>>(std::istream &in, std::vector<T> &v)
{
    for (T &t : v)
    {
        in >> t;
    }
    return in;
}
```

# += 运算符

```c++
template<typename T, typename K>
void operator+=(std::vector<T> &v, const K &k)
{
    v.push_back(static_cast<T>(k));
}
```

# 前缀 ++ 运算符

```c++
template<typename T>
void operator++(std::vector<T> &v)
{
    v.emplace_back();
    for (size_t i = v.size() - 1; i > 0; --i)
    {
        std::swap(v[i], v[i - 1]);
    }
}
```

