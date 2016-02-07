# Introduction #

The algorithm uses an array of size 1 million to lazily cache the cycle lengths as they are computed.


# Details #

An array of size million is initialized with values -1. When the cycle length of an integer k is needed, it checks if the cycle length for the k value is stored in the cache and returns said value if it is. If not, then the value is computed recursively, either by calling get\_len with k/2 or 1.5K+0.5 depending on even or odd with base case k=1. When the value is computed, it is added to the cache if the k i less than or equal to 1 million.