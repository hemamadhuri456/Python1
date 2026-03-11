class Solution:
    def strongPasswordChecker(self, password: str) -> int:
        n = len(password)
        need = int(not any(c.islower() for c in password)) + int(not any(c.isupper() for c in password)) + int(not any(c.isdigit() for c in password))
        if n < 6:
            cnt, idx = 0, 0
            while idx < n:
                j = idx
                while j < n and password[j] == password[idx]:
                    j += 1
                cnt += (j - idx) // 3
                idx = j
            return max(6 - n, need, cnt)
        runs = []
        idx = 0
        while idx < n:
            j = idx
            while j < n and password[j] == password[idx]:
                j += 1
            if j - idx >= 3:
                runs.append(j - idx)
            idx = j
        cnt = sum(v // 3 for v in runs)
        if n <= 20:
            return max(need, cnt)
        delCnt = n - 20
        mod = [0, 0, 0]
        for v in runs:
            mod[v % 3] += 1
        del1 = min(mod[0], delCnt)
        delCnt -= del1
        cnt -= del1
        del2 = min(mod[1], delCnt // 2)
        delCnt -= del2 * 2
        cnt -= del2 + delCnt // 3
        return (n - 20) + max(need, cnt)
