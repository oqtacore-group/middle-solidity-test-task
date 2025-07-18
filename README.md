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

1. A user can send ETH to the contract via the stake() function. The amount is added to their personal account in the smart contract (balances).
2. Use the balances mapping to store deposit amounts for each address.
3. Store (ONLY) user addresses in depositors (those who have made a deposit). Addresses must not be duplicated on repeated deposits.
4. When deploying the contract, an arbitrary wallet address must be passed as a parameter, which will become the owner of this smart contract.
5. The getAllDepositors() function must return all addresses that have deposited funds (but not the amounts). This function can only be called by address == owner.
6. Use onlyPositiveDeposit() to check that the user is sending > 0. This should be reusable code that can be applied to any function.
7. The getMyBalance() function must return the amount of ETH in the smart contract for the user who called the function (without passing any parameters).
8. Emit the Staked() event on each deposit.
9. ** Emit the Withdrawn() event on each withdrawal (advanced task).
10. ** Create a withdraw() function — it should allow the owner to withdraw user funds (advanced task).

# RU. Общие положения
- Cамо задание будет в README.md репозитория
- Кандидату надо расшарить экран
- Необходимо открыть **IDE Remix** (https://remix.ethereum.org/) и выполнить import GitHub репозитория (репозиторий вам скинут в zoom чат после того как вы пошарите экран)
- Нужно будет выполнить задание (оно простое: **Solidity Simple Staking Smart Contract**)
- Главный KPI по которому будет оцениваться работа - использование всех доступных знаний по работе Solidity. Компилируемый смарт-контракт.
- Задание очень простое и одно из главных требований - самостоятельно принимать решение.
- Проверяйте работу контракта через Ctrl + S и во вкладке Solidity Compiler
- Когда выполните задание - сообщите об этом интервьюеру
- **Большая просьба** - нельзя использовать любые AI. Google или документация - одобряется.
- Время на выполнение 30 минут. Сообщите интервьюеру когда будете готовы. 

## Задание: Очень простой смарт-контракт записи балансов (Solidity)

Реализуйте на Solidity 0.8.x смарт-контракт SimpleStaking, который включает в себя следующие возможности:

1. Пользователь может отправить ETH в контракт через функцию stake(). Сумма добавляется к его персональному счету в смарт-контракте (balances).
2. Используйте balances для хранения сумм депозитов для каждого адреса.
3. Храните (ТОЛЬКО) адреса пользователей в depositors (которые сделали депозит). Адреса не должны повторяться при повторных пополнениях
4. При развертыввании контракта необходимо передавать паратмером любой адрес кошелька который станет **owner** этого смарт-контракта.
5. Функция getAllDepositors() должна возвращать все адреса кто вносил деньги (но не сами суммы). Эту функцию может вызывать только **address == owner**
6. Проверять с помощь onlyPositiveDeposit() — что пользователь отправляет > 0. Это должен быть переиспользуемый код который можно использовать для любой функции.
7. Функция getMyBalance() должна возвращать сумму ETH в смарт-контракте пользователя который вызвал контракт (без передачи параметров).
8. Отправляйте событие Staked() при каждом депозите.
9. ** Отправляйте событие Withdrawn() при каждом снятии средств (задание повышенной сложности)
10. ** Создайте функцию withdraw() - которая позволит снимать средства пользователя только владельцу (задание повышенной сложности) 
