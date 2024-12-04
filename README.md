## Christmas Dinner

Which problems do we solve:

-   **Funding Security**: Organizing a social event is tough, people often say "we will attend" but take forever to pay their share, with our Christmas Dinner Contract we directly "force" the attendees to pay upon signup, so the host can plan properly knowing the total budget after deadline.
-   **Organization**: Through funding security hosts will have a way easier time to arrange the event which fits the given budget. No Backsies.


Roles and Actors:
- ```Host```: The person doing the organization of the event. Receiver of the funds by the end of ```deadline```. Privilegded Role, which can be handed over to any ```Participant``` by the current ```host```
- ```Participant```: Attendees of the event which provided some sort of funding. ```Participant``` can become new ```Host```, can continue sending money as Generous Donation, can sign up friends and can become ```Funder```.
- ```Funder```: Former Participants which left their funds in the contract as donation, but can not attend the event. ```Funder``` can become ```Participant``` again BEFORE deadline ends.



Key Assumptions:
- There is some trust between the host and attendees
- Only Whitelisted tokens and ether will be handled.



## Usage

### Build

```shell
$ forge install
```

```shell
$ forge build
```

### Test

```shell
$ forge test
```

```shell
$ forge coverage
```

