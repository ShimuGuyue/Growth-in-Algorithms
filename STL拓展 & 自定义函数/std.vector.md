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



