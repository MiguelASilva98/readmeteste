# Agent Startup and Settings

There are four types of agents that we can use in Identity. We have **AdminAgent**, **RegulatorAgent**, **ProviderAgent**, and **ConsumerAgent**.

## Regulator Agent (Issuer) 

This agent should be started with the below parameters:

    aca-py start --inbound-transport http 0.0.0.0 8022 --outbound-transport http --endpoint http://0.0.0.0:8022 --label RegulatorAgent --seed Agent000000000000000000000000000 --admin 0.0.0.0 8023 --admin-insecure-mode --auto-ping-connection --auto-accept-invites --auto-accept-requests --auto-respond-credential-offer --auto-respond-credential-proposal --auto-respond-credential-request--auto-store-credential --wallet-key secret --wallet-name RegulatorAgent --wallet-type indy --genesis-url http://172.0.0.0:9000/genesis

For more info about RegulatorAgent:  https://github.com/MiguelASilva98/readmeteste/wiki/Agent-Startup-and-Settings#regulator-agent-issuer

## Holder Agent (Provider)

This agent should be started with the below parameters:

    aca-py start --inbound-transport http 0.0.0.0 8022 --outbound-transport http --endpoint http://0.0.0.0:8022 --label ProviderAgent--seed Agent000000000000000000000000000 --admin 0.0.0.0 8023 --admin-insecure-mode --auto-ping-connection --auto-accept-invites --auto-accept-requests --wallet-key secret --wallet-name ProviderAgent--wallet-type indy --genesis-url http://172.0.0.0:9000/genesis

For more info about ProviderAgent:  https://github.com/MiguelASilva98/readmeteste/wiki/Agent-Startup-and-Settings#holder-agent-provider

## Verifier Agent (Consumer)

This agent should be started with the below parameters:

    aca-py start --inbound-transport http 0.0.0.0 8022 --outbound-transport http --endpoint http://0.0.0.0:8022 --label ConsumerAgent --seed Agent000000000000000000000000000 --admin 0.0.0.0 8023 --admin-insecure-mode --auto-ping-connection --auto-accept-invites --auto-accept-requests --auto-verify-presentation --wallet-key secret --wallet-name ConsumerAgent --wallet-type indy --genesis-url http://172.0.0.0:9000/genesis

For more info about ConsumerAgent: https://github.com/MiguelASilva98/readmeteste/wiki/Agent-Startup-and-Settings#verifier-agent-consumer

## Admin Agent

This agent should be started with the below parameters:

    aca-py start --inbound-transport http 0.0.0.0 8022 --outbound-transport http --endpoint http://0.0.0.0:8022 --label AdminAgent --seed Agent000000000000000000000000000 --admin 0.0.0.0 8023 --admin-insecure-mode --auto-ping-connection --auto-accept-invites --auto-accept-requests --auto-respond-credential-offer --auto-respond-credential-proposal --auto-respond-credential-request--auto-store-credential --auto-verify-presentation --wallet-key secret --wallet-name AdminAgent --wallet-type indy --genesis-url http://172.0.0.0:9000/genesis

For more info about AdminAgent:  https://github.com/MiguelASilva98/readmeteste/wiki/Agent-Startup-and-Settings#admin-agent
