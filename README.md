# EN. General Guidelines
- The assignment will be available in the README.md of the GitHub repository.
- Please share your screen during the entire live coding session.
- Open Remix IDE (https://remix.ethereum.org/) in your browser and import the GitHub repository (we will send you the link in the Zoom chat once you start screen sharing).
- You will need to complete a simple task — implementing a Solidity Staking Smart Contract.
- The main KPI for evaluation: using your full knowledge of Solidity to deliver a working, compilable smart contract.
- The assignment is intentionally simple — one of the key requirements is to make decisions independently.
- Test your contract as you go using Ctrl (|| command) + S and the Solidity Compiler tab in Remix.
- Once you finish the task, let the interviewer know.
- **Important**: Do not use any AI tools during this session. However, using Google or official documentation is allowed.
- You have 30 minutes to complete the assignment. Please inform the interviewer when you’re ready to begin.

## Assignment: Very Simple Balance Tracking Smart Contract (Solidity)

Implement a smart contract SimpleStaking in Solidity 0.8.x that includes the following features:

- A user can send ETH to the contract using the stake() function.
- The amount is added to their personal balance.
- Store (ONLY) the users who have made a deposit in the depositors array.
- Addresses must not be duplicated if a user makes multiple deposits.
- Use balances to store deposit amounts for each address.
- When deploying the contract, a wallet address must be passed as a parameter — this address will become the owner of the contract.
- The function getAllDepositors() must return all addresses that have made deposits (but not the amounts). This function can only be called by the address that is equal to the owner.
- Use the modifier onlyPositiveDeposit() to check that the user is sending msg.value > 0. This should be reusable code that can be applied to any function.
- The function getMyBalance() must return the amount of ETH held by the calling user in the contract.
- Emit the Staked() event on each deposit.
- ** Emit the Withdrawn() event on each withdrawal (advanced task).
- ** Create a withdraw() function — it should allow the owner to withdraw user funds (advanced task).

# RU. Общие положения
1. Cамо задание будет в README.md репозитория
2. Кандидату надо расшарить экран
3. Необходимо открыть **IDE Remix** (https://remix.ethereum.org/) и выполнить import GitHub репозитория (репозиторий вам скинут в zoom чат после того как вы пошарите экран) 
4. Нужно будет выполнить задание (оно простое: **Solidity Staking Solana Smart Contract**)
5. Главный KPI по которому будет оцениваться работа - использование всех доступных знаний по работе Solidity. Компилируемый смарт-контракт. 
6. Задание очень простое и одно из главных требований - самостоятельно принимать решение. 
7. Проверяйте работу контракта через Ctrl + S и во вкладке Solidity Compiler   
8. Когда выполните задание - сообщите об этом интервьюеру
9. **Большая просьба** - нельзя использовать любые AI. Google или документация - одобряется. 
10. Время на выполнение 30 минут. Сообщите интервьюеру когда будете готовы. 

## Задание: Очень простой смарт-контракт записи балансов (Solidity)

Реализуйте на Solidity 0.8.x смарт-контракт SimpleStaking, который включает в себя следующие возможности:

- Пользователь может отправить ETH в контракт через функцию stake(). 
- Сумма добавляется к его персональному счету.
- Храните (ТОЛЬКО) данные пользователей которые сделали депозит в depositors.
- Адреса не должны повторяться при повторных пополнениях.
- Используйте balances для хранения сумм депозитов для каждого адреса.

- При деплое контракта необходимо передавать паратмером любой адрес кошелька который станет owner этого смарт-контракта  
- Функция getAllDepositors() должна возвращать все адреса кто вносил деньги (но не сами суммы). Эту функцию может вызывать только address == owner
- Проверяйте с помощь onlyPositiveDeposit() — что пользователь отправляет > 0. Это должен быть переиспользуемый код который можно использовать для любой функции. 

- Функция getMyBalance() должна возвращать сумму ETH в смарт-контракте пользователя который вызывает контракт.
- Отправляйте событие Staked() при каждом депозите.
- * Отправляйте событие Withdrawn() при каждом снятии средств (задание повышенной сложности) 
- * Создайте функцию withdraw() - которая позволит снимать средства пользователя только владельцу (задание повышенной сложности) 
