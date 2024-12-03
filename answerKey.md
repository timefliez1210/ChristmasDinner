1. [high/medium] Should a user be the host, the user should not be able to switch participant to false, obviously the host must attend.
2. [high] Reentrancy in Refund (mutex lock modifier incomplete)
3. [low] inconsistency in docs in deposit. It is mentioned a user can sign up for any other user, which is not possible within the implementation
4. [Medium] Deadline can arbitrarily be set by the host against the assumption
5. [Medium] Refund is not setting participation to false -> people are still attending and could even be host