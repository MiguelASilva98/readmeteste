There are four types of agents that we can use in Identity. We have **AdminAgent**, **RegulatorAgent**, **ProviderAgent**, and **ConsumerAgent**.

**Regulator Agent** - This agent should be started with the below parameters

    aca-py start --inbound-transport http 0.0.0.0 8022 --outbound-transport http --endpoint http://0.0.0.0:8022 --label RegulatorAgent --seed Agent000000000000000000000000000 --admin 0.0.0.0 8023 --admin-insecure-mode --auto-ping-connection --auto-accept-invites --auto-accept-requests --auto-respond-credential-offer --auto-respond-credential-proposal --auto-respond-credential-request--auto-store-credential --auto-verify-presentation --wallet-key secret --wallet-name VerifierAgent --wallet-type indy --genesis-url http://172.0.0.0:9000/genesis

For more info about RegulatorAgent:  [https://github.com/MiguelASilva98/readmeteste/wiki/Agent-Startup-and-Settings#regulator-agent-issuer](https://github.com/MiguelASilva98/readmeteste/wiki/Agent-Startup-and-Settings#regulator-agent-issuer)
