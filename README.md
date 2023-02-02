# modulo-on-factorial



int powr(int num,int n){

int res=1; while(n>0){ if(n%2==1){res=res*num; res%=mod;

} n=n>>1;

num=(num*num)%mod;

} return res;

}


// p is mod //
ll inverse(int a, int p){
    return powr(a, p-2);
}


factorial[0] = 1;
for (int i = 1; i <= 2e5; i++) {
    factorial[i] = factorial[i - 1] * i % mod;
}

int binomial_coefficient(int n, int k) {
    return factorial[n] * inverse(factorial[k] * factorial[n - k] % mod,mod) % mod;
}
