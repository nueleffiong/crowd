# crowd
crowdfunding website
In this updated version of the crowdfunding smart contract, we have implemented the following changes:

Added a FundingStage enum to keep track of the crowdfunding stages - Open, Successful, or Failed.

Introduced a Milestone struct to store information about each milestone, including the amount required to reach the milestone, the deadline, a flag indicating whether the milestone is reached, and a flag indicating whether the funds for the milestone have been released.

Modified the contribute function to transfer tokens from the contributor to the crowdfunding contract instead of Ether. The contribution amount is stored in the contributions mapping.

Introduced a checkMilestoneReached internal function to check if any milestone is reached whenever a contribution is made.

Modified the closeCrowdfunding function to change the crowdfunding stage to Successful if the goal amount is reached and to Failed otherwise.

Added a claimTokens function that allows contributors to claim tokens as rewards based on their contributions.

Added a calculateTokenReward internal function to calculate the token reward for each contributor based on their contribution and the total raised amount.

Added a withdrawContribution function that allows contributors to withdraw their contributions if the crowdfunding fails.

Introduced an addMilestone function that allows the project owner to add milestones to the crowdfunding campaign.

Added several utility functions (getContractBalance, getNumberOfMilestones, getMilestone) to retrieve contract information.

It is essential to note that this contract still requires proper testing and auditing before deploying it to the mainnet. Additionally, it's crucial to handle other aspects like access control, error handling, and security considerations before deploying the contract for production use.
