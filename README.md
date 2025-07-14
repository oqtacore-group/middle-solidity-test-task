## EN. Assignment: Very Simple Balance Tracking Smart Contract (Solidity)

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

## RU. Задание: Очень простой смарт-контракт записи балансов (Solidity)

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
