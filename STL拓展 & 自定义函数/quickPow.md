# 快速幂

```c++
int64_t quickPow(int64_t base, int64_t n, const int64_t mod = INT64_MAX)
{
    int64_t ans = 1;
    base %= mod;
    while (n)
    {
        if (n & 1LL)
            ans = ans * base % mod;
        base = base * base % mod;
        n >>= 1;
    }
    return ans;
}
```

