1. [High] Reentrancy in Refund (mutex lock modifier incomplete)
2. [Low] [Medium] [High] withdraw() can be called by host before deadline (not even maliciously), which sweeps the contract and makes refunds() impossible (no state is updated). Also if withdraw would be called before deadline and users would still be signing up, the whole accounting system is messed up which can cause interesting behaviour if users were to use the refund() after others deposited. I would suggest rating the severity of the issue depending how far the consequences were thought through.
3. [High] Withdraw function for host does not send eth. After Deadline ETH would be locked in the contract.
3. [Medium] Refund is not setting participation to false -> people are still attending and could even be host
4. [Medium] Receive function is not setting participation status
5. [Medium] Should a user be the host, the user should not be able to switch participant to false, obviously the host must attend.
6. [Low] inconsistency in docs in deposit. It is mentioned a user can sign up for any other user, which is not possible within the implementation
7. [Low] Deadline can arbitrarily be set by the host against the assumption (within setDeadline() bool deadlineSet should be set to true)