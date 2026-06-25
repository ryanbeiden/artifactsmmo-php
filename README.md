# Artifacts MMO – PHP SDK

Artifacts is an API-based MMO game where you can manage 5 characters to explore, fight, gather resources, craft items and much more.

Website: https://artifactsmmo.com/

Documentation: https://docs.artifactsmmo.com/

OpenAPI Spec: https://api.artifactsmmo.com/openapi.json

## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

```sh
composer require ryanbeiden/artifactsmmo-php
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');




$apiInstance = new ArtifactsMmo\Api\AccountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$addAccountSchema = new \ArtifactsMmo\Model\AddAccountSchema(); // \ArtifactsMmo\Model\AddAccountSchema

try {
    $result = $apiInstance->createAccountAccountsCreatePost($addAccountSchema);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountsApi->createAccountAccountsCreatePost: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccountsApi* | [**createAccountAccountsCreatePost**](docs/Api/AccountsApi.md#createaccountaccountscreatepost) | **POST** /accounts/create | Create Account
*AccountsApi* | [**forgotPasswordAccountsForgotPasswordPost**](docs/Api/AccountsApi.md#forgotpasswordaccountsforgotpasswordpost) | **POST** /accounts/forgot_password | Forgot Password
*AccountsApi* | [**getAccountAccountsAccountGet**](docs/Api/AccountsApi.md#getaccountaccountsaccountget) | **GET** /accounts/{account} | Get Account
*AccountsApi* | [**getAccountAchievementsAccountsAccountAchievementsGet**](docs/Api/AccountsApi.md#getaccountachievementsaccountsaccountachievementsget) | **GET** /accounts/{account}/achievements | Get Account Achievements
*AccountsApi* | [**getAccountCharactersAccountsAccountCharactersGet**](docs/Api/AccountsApi.md#getaccountcharactersaccountsaccountcharactersget) | **GET** /accounts/{account}/characters | Get Account Characters
*AccountsApi* | [**resetPasswordAccountsResetPasswordPost**](docs/Api/AccountsApi.md#resetpasswordaccountsresetpasswordpost) | **POST** /accounts/reset_password | Reset Password
*AchievementsApi* | [**getAchievementAchievementsCodeGet**](docs/Api/AchievementsApi.md#getachievementachievementscodeget) | **GET** /achievements/{code} | Get Achievement
*AchievementsApi* | [**getAllAchievementsAchievementsGet**](docs/Api/AchievementsApi.md#getallachievementsachievementsget) | **GET** /achievements | Get All Achievements
*BadgesApi* | [**getAllBadgesBadgesGet**](docs/Api/BadgesApi.md#getallbadgesbadgesget) | **GET** /badges | Get All Badges
*BadgesApi* | [**getBadgeBadgesCodeGet**](docs/Api/BadgesApi.md#getbadgebadgescodeget) | **GET** /badges/{code} | Get Badge
*CharactersApi* | [**createCharacterCharactersCreatePost**](docs/Api/CharactersApi.md#createcharactercharacterscreatepost) | **POST** /characters/create | Create Character
*CharactersApi* | [**deleteCharacterCharactersDeletePost**](docs/Api/CharactersApi.md#deletecharactercharactersdeletepost) | **POST** /characters/delete | Delete Character
*CharactersApi* | [**getActiveCharactersCharactersActiveGet**](docs/Api/CharactersApi.md#getactivecharacterscharactersactiveget) | **GET** /characters/active | Get Active Characters
*CharactersApi* | [**getCharacterCharactersNameGet**](docs/Api/CharactersApi.md#getcharactercharactersnameget) | **GET** /characters/{name} | Get Character
*EffectsApi* | [**getAllEffectsEffectsGet**](docs/Api/EffectsApi.md#getalleffectseffectsget) | **GET** /effects | Get All Effects
*EffectsApi* | [**getEffectEffectsCodeGet**](docs/Api/EffectsApi.md#geteffecteffectscodeget) | **GET** /effects/{code} | Get Effect
*EventsApi* | [**getAllActiveEventsEventsActiveGet**](docs/Api/EventsApi.md#getallactiveeventseventsactiveget) | **GET** /events/active | Get All Active Events
*EventsApi* | [**getAllEventsEventsGet**](docs/Api/EventsApi.md#getalleventseventsget) | **GET** /events | Get All Events
*EventsApi* | [**spawnEventEventsSpawnPost**](docs/Api/EventsApi.md#spawneventeventsspawnpost) | **POST** /events/spawn | Spawn Event
*GrandExchangeApi* | [**getGeHistoryGrandexchangeHistoryCodeGet**](docs/Api/GrandExchangeApi.md#getgehistorygrandexchangehistorycodeget) | **GET** /grandexchange/history/{code} | Get Ge History
*GrandExchangeApi* | [**getGeOrderGrandexchangeOrdersIdGet**](docs/Api/GrandExchangeApi.md#getgeordergrandexchangeordersidget) | **GET** /grandexchange/orders/{id} | Get Ge Order
*GrandExchangeApi* | [**getGeOrdersGrandexchangeOrdersGet**](docs/Api/GrandExchangeApi.md#getgeordersgrandexchangeordersget) | **GET** /grandexchange/orders | Get Ge Orders
*ItemsApi* | [**getAllItemsItemsGet**](docs/Api/ItemsApi.md#getallitemsitemsget) | **GET** /items | Get All Items
*ItemsApi* | [**getItemItemsCodeGet**](docs/Api/ItemsApi.md#getitemitemscodeget) | **GET** /items/{code} | Get Item
*LeaderboardApi* | [**getAccountsLeaderboardLeaderboardAccountsGet**](docs/Api/LeaderboardApi.md#getaccountsleaderboardleaderboardaccountsget) | **GET** /leaderboard/accounts | Get Accounts Leaderboard
*LeaderboardApi* | [**getCharactersLeaderboardLeaderboardCharactersGet**](docs/Api/LeaderboardApi.md#getcharactersleaderboardleaderboardcharactersget) | **GET** /leaderboard/characters | Get Characters Leaderboard
*MapsApi* | [**getAllMapsMapsGet**](docs/Api/MapsApi.md#getallmapsmapsget) | **GET** /maps | Get All Maps
*MapsApi* | [**getLayerMapsMapsLayerGet**](docs/Api/MapsApi.md#getlayermapsmapslayerget) | **GET** /maps/{layer} | Get Layer Maps
*MapsApi* | [**getMapByIdMapsIdMapIdGet**](docs/Api/MapsApi.md#getmapbyidmapsidmapidget) | **GET** /maps/id/{map_id} | Get Map By Id
*MapsApi* | [**getMapByPositionMapsLayerXYGet**](docs/Api/MapsApi.md#getmapbypositionmapslayerxyget) | **GET** /maps/{layer}/{x}/{y} | Get Map By Position
*MonstersApi* | [**getAllMonstersMonstersGet**](docs/Api/MonstersApi.md#getallmonstersmonstersget) | **GET** /monsters | Get All Monsters
*MonstersApi* | [**getMonsterMonstersCodeGet**](docs/Api/MonstersApi.md#getmonstermonsterscodeget) | **GET** /monsters/{code} | Get Monster
*MyAccountApi* | [**changePasswordMyChangePasswordPost**](docs/Api/MyAccountApi.md#changepasswordmychangepasswordpost) | **POST** /my/change_password | Change Password
*MyAccountApi* | [**getAccountDetailsMyDetailsGet**](docs/Api/MyAccountApi.md#getaccountdetailsmydetailsget) | **GET** /my/details | Get Account Details
*MyAccountApi* | [**getBankDetailsMyBankGet**](docs/Api/MyAccountApi.md#getbankdetailsmybankget) | **GET** /my/bank | Get Bank Details
*MyAccountApi* | [**getBankItemsMyBankItemsGet**](docs/Api/MyAccountApi.md#getbankitemsmybankitemsget) | **GET** /my/bank/items | Get Bank Items
*MyAccountApi* | [**getGeHistoryMyGrandexchangeHistoryGet**](docs/Api/MyAccountApi.md#getgehistorymygrandexchangehistoryget) | **GET** /my/grandexchange/history | Get Ge History
*MyAccountApi* | [**getGeOrdersMyGrandexchangeOrdersGet**](docs/Api/MyAccountApi.md#getgeordersmygrandexchangeordersget) | **GET** /my/grandexchange/orders | Get Ge Orders
*MyAccountApi* | [**getPendingItemsMyPendingItemsGet**](docs/Api/MyAccountApi.md#getpendingitemsmypendingitemsget) | **GET** /my/pending-items | Get Pending Items
*MyCharactersApi* | [**actionAcceptNewTaskMyNameActionTaskNewPost**](docs/Api/MyCharactersApi.md#actionacceptnewtaskmynameactiontasknewpost) | **POST** /my/{name}/action/task/new | Action Accept New Task
*MyCharactersApi* | [**actionBuyBankExpansionMyNameActionBankBuyExpansionPost**](docs/Api/MyCharactersApi.md#actionbuybankexpansionmynameactionbankbuyexpansionpost) | **POST** /my/{name}/action/bank/buy_expansion | Action Buy Bank Expansion
*MyCharactersApi* | [**actionChangeSkinMyNameActionChangeSkinPost**](docs/Api/MyCharactersApi.md#actionchangeskinmynameactionchangeskinpost) | **POST** /my/{name}/action/change_skin | Action Change Skin
*MyCharactersApi* | [**actionClaimPendingItemMyNameActionClaimItemIdPost**](docs/Api/MyCharactersApi.md#actionclaimpendingitemmynameactionclaimitemidpost) | **POST** /my/{name}/action/claim_item/{id} | Action Claim Pending Item
*MyCharactersApi* | [**actionCompleteTaskMyNameActionTaskCompletePost**](docs/Api/MyCharactersApi.md#actioncompletetaskmynameactiontaskcompletepost) | **POST** /my/{name}/action/task/complete | Action Complete Task
*MyCharactersApi* | [**actionCraftingMyNameActionCraftingPost**](docs/Api/MyCharactersApi.md#actioncraftingmynameactioncraftingpost) | **POST** /my/{name}/action/crafting | Action Crafting
*MyCharactersApi* | [**actionDeleteItemMyNameActionDeletePost**](docs/Api/MyCharactersApi.md#actiondeleteitemmynameactiondeletepost) | **POST** /my/{name}/action/delete | Action Delete Item
*MyCharactersApi* | [**actionDepositBankGoldMyNameActionBankDepositGoldPost**](docs/Api/MyCharactersApi.md#actiondepositbankgoldmynameactionbankdepositgoldpost) | **POST** /my/{name}/action/bank/deposit/gold | Action Deposit Bank Gold
*MyCharactersApi* | [**actionDepositBankItemMyNameActionBankDepositItemPost**](docs/Api/MyCharactersApi.md#actiondepositbankitemmynameactionbankdeposititempost) | **POST** /my/{name}/action/bank/deposit/item | Action Deposit Bank Item
*MyCharactersApi* | [**actionEquipItemMyNameActionEquipPost**](docs/Api/MyCharactersApi.md#actionequipitemmynameactionequippost) | **POST** /my/{name}/action/equip | Action Equip Item
*MyCharactersApi* | [**actionFightMyNameActionFightPost**](docs/Api/MyCharactersApi.md#actionfightmynameactionfightpost) | **POST** /my/{name}/action/fight | Action Fight
*MyCharactersApi* | [**actionGatheringMyNameActionGatheringPost**](docs/Api/MyCharactersApi.md#actiongatheringmynameactiongatheringpost) | **POST** /my/{name}/action/gathering | Action Gathering
*MyCharactersApi* | [**actionGeBuyItemMyNameActionGrandexchangeBuyPost**](docs/Api/MyCharactersApi.md#actiongebuyitemmynameactiongrandexchangebuypost) | **POST** /my/{name}/action/grandexchange/buy | Action Ge Buy Item
*MyCharactersApi* | [**actionGeCancelOrderMyNameActionGrandexchangeCancelPost**](docs/Api/MyCharactersApi.md#actiongecancelordermynameactiongrandexchangecancelpost) | **POST** /my/{name}/action/grandexchange/cancel | Action Ge Cancel Order
*MyCharactersApi* | [**actionGeCreateBuyOrderMyNameActionGrandexchangeCreateBuyOrderPost**](docs/Api/MyCharactersApi.md#actiongecreatebuyordermynameactiongrandexchangecreatebuyorderpost) | **POST** /my/{name}/action/grandexchange/create-buy-order | Action Ge Create Buy Order
*MyCharactersApi* | [**actionGeCreateSellOrderMyNameActionGrandexchangeCreateSellOrderPost**](docs/Api/MyCharactersApi.md#actiongecreatesellordermynameactiongrandexchangecreatesellorderpost) | **POST** /my/{name}/action/grandexchange/create-sell-order | Action Ge Create Sell Order
*MyCharactersApi* | [**actionGeFillMyNameActionGrandexchangeFillPost**](docs/Api/MyCharactersApi.md#actiongefillmynameactiongrandexchangefillpost) | **POST** /my/{name}/action/grandexchange/fill | Action Ge Fill
*MyCharactersApi* | [**actionGiveGoldMyNameActionGiveGoldPost**](docs/Api/MyCharactersApi.md#actiongivegoldmynameactiongivegoldpost) | **POST** /my/{name}/action/give/gold | Action Give Gold
*MyCharactersApi* | [**actionGiveItemsMyNameActionGiveItemPost**](docs/Api/MyCharactersApi.md#actiongiveitemsmynameactiongiveitempost) | **POST** /my/{name}/action/give/item | Action Give Items
*MyCharactersApi* | [**actionMoveMyNameActionMovePost**](docs/Api/MyCharactersApi.md#actionmovemynameactionmovepost) | **POST** /my/{name}/action/move | Action Move
*MyCharactersApi* | [**actionNpcBuyItemMyNameActionNpcBuyPost**](docs/Api/MyCharactersApi.md#actionnpcbuyitemmynameactionnpcbuypost) | **POST** /my/{name}/action/npc/buy | Action Npc Buy Item
*MyCharactersApi* | [**actionNpcSellItemMyNameActionNpcSellPost**](docs/Api/MyCharactersApi.md#actionnpcsellitemmynameactionnpcsellpost) | **POST** /my/{name}/action/npc/sell | Action Npc Sell Item
*MyCharactersApi* | [**actionRecyclingMyNameActionRecyclingPost**](docs/Api/MyCharactersApi.md#actionrecyclingmynameactionrecyclingpost) | **POST** /my/{name}/action/recycling | Action Recycling
*MyCharactersApi* | [**actionRestMyNameActionRestPost**](docs/Api/MyCharactersApi.md#actionrestmynameactionrestpost) | **POST** /my/{name}/action/rest | Action Rest
*MyCharactersApi* | [**actionTaskCancelMyNameActionTaskCancelPost**](docs/Api/MyCharactersApi.md#actiontaskcancelmynameactiontaskcancelpost) | **POST** /my/{name}/action/task/cancel | Action Task Cancel
*MyCharactersApi* | [**actionTaskExchangeMyNameActionTaskExchangePost**](docs/Api/MyCharactersApi.md#actiontaskexchangemynameactiontaskexchangepost) | **POST** /my/{name}/action/task/exchange | Action Task Exchange
*MyCharactersApi* | [**actionTaskTradeMyNameActionTaskTradePost**](docs/Api/MyCharactersApi.md#actiontasktrademynameactiontasktradepost) | **POST** /my/{name}/action/task/trade | Action Task Trade
*MyCharactersApi* | [**actionTransitionMyNameActionTransitionPost**](docs/Api/MyCharactersApi.md#actiontransitionmynameactiontransitionpost) | **POST** /my/{name}/action/transition | Action Transition
*MyCharactersApi* | [**actionUnequipItemMyNameActionUnequipPost**](docs/Api/MyCharactersApi.md#actionunequipitemmynameactionunequippost) | **POST** /my/{name}/action/unequip | Action Unequip Item
*MyCharactersApi* | [**actionUseItemMyNameActionUsePost**](docs/Api/MyCharactersApi.md#actionuseitemmynameactionusepost) | **POST** /my/{name}/action/use | Action Use Item
*MyCharactersApi* | [**actionWithdrawBankGoldMyNameActionBankWithdrawGoldPost**](docs/Api/MyCharactersApi.md#actionwithdrawbankgoldmynameactionbankwithdrawgoldpost) | **POST** /my/{name}/action/bank/withdraw/gold | Action Withdraw Bank Gold
*MyCharactersApi* | [**actionWithdrawBankItemMyNameActionBankWithdrawItemPost**](docs/Api/MyCharactersApi.md#actionwithdrawbankitemmynameactionbankwithdrawitempost) | **POST** /my/{name}/action/bank/withdraw/item | Action Withdraw Bank Item
*MyCharactersApi* | [**getAllCharactersLogsMyLogsGet**](docs/Api/MyCharactersApi.md#getallcharacterslogsmylogsget) | **GET** /my/logs | Get All Characters Logs
*MyCharactersApi* | [**getCharacterLogsMyLogsNameGet**](docs/Api/MyCharactersApi.md#getcharacterlogsmylogsnameget) | **GET** /my/logs/{name} | Get Character Logs
*MyCharactersApi* | [**getMyCharactersMyCharactersGet**](docs/Api/MyCharactersApi.md#getmycharactersmycharactersget) | **GET** /my/characters | Get My Characters
*NPCsApi* | [**getAllNpcsItemsNpcsItemsGet**](docs/Api/NPCsApi.md#getallnpcsitemsnpcsitemsget) | **GET** /npcs/items | Get All Npcs Items
*NPCsApi* | [**getAllNpcsNpcsDetailsGet**](docs/Api/NPCsApi.md#getallnpcsnpcsdetailsget) | **GET** /npcs/details | Get All Npcs
*NPCsApi* | [**getNpcItemsNpcsItemsCodeGet**](docs/Api/NPCsApi.md#getnpcitemsnpcsitemscodeget) | **GET** /npcs/items/{code} | Get Npc Items
*NPCsApi* | [**getNpcNpcsDetailsCodeGet**](docs/Api/NPCsApi.md#getnpcnpcsdetailscodeget) | **GET** /npcs/details/{code} | Get Npc
*ResourcesApi* | [**getAllResourcesResourcesGet**](docs/Api/ResourcesApi.md#getallresourcesresourcesget) | **GET** /resources | Get All Resources
*ResourcesApi* | [**getResourceResourcesCodeGet**](docs/Api/ResourcesApi.md#getresourceresourcescodeget) | **GET** /resources/{code} | Get Resource
*ServerDetailsApi* | [**getServerDetailsGet**](docs/Api/ServerDetailsApi.md#getserverdetailsget) | **GET** / | Get Server Details
*SimulationApi* | [**fightSimulationSimulationFightSimulationPost**](docs/Api/SimulationApi.md#fightsimulationsimulationfightsimulationpost) | **POST** /simulation/fight_simulation | Fight Simulation
*TasksApi* | [**getAllTasksRewardsTasksRewardsGet**](docs/Api/TasksApi.md#getalltasksrewardstasksrewardsget) | **GET** /tasks/rewards | Get All Tasks Rewards
*TasksApi* | [**getAllTasksTasksListGet**](docs/Api/TasksApi.md#getalltaskstaskslistget) | **GET** /tasks/list | Get All Tasks
*TasksApi* | [**getTaskTasksListCodeGet**](docs/Api/TasksApi.md#gettasktaskslistcodeget) | **GET** /tasks/list/{code} | Get Task
*TasksApi* | [**getTasksRewardTasksRewardsCodeGet**](docs/Api/TasksApi.md#gettasksrewardtasksrewardscodeget) | **GET** /tasks/rewards/{code} | Get Tasks Reward
*TokenApi* | [**generateTokenTokenPost**](docs/Api/TokenApi.md#generatetokentokenpost) | **POST** /token | Generate Token

## Models

- [AccessSchema](docs/Model/AccessSchema.md)
- [AccountAchievementObjectiveSchema](docs/Model/AccountAchievementObjectiveSchema.md)
- [AccountAchievementSchema](docs/Model/AccountAchievementSchema.md)
- [AccountDetails](docs/Model/AccountDetails.md)
- [AccountDetailsSchema](docs/Model/AccountDetailsSchema.md)
- [AccountLeaderboardSchema](docs/Model/AccountLeaderboardSchema.md)
- [AccountLeaderboardType](docs/Model/AccountLeaderboardType.md)
- [AccountStatus](docs/Model/AccountStatus.md)
- [AchievementObjectiveSchema](docs/Model/AchievementObjectiveSchema.md)
- [AchievementResponseSchema](docs/Model/AchievementResponseSchema.md)
- [AchievementRewardsSchema](docs/Model/AchievementRewardsSchema.md)
- [AchievementSchema](docs/Model/AchievementSchema.md)
- [AchievementType](docs/Model/AchievementType.md)
- [ActionType](docs/Model/ActionType.md)
- [ActiveCharacterSchema](docs/Model/ActiveCharacterSchema.md)
- [ActiveEventResponseSchema](docs/Model/ActiveEventResponseSchema.md)
- [ActiveEventSchema](docs/Model/ActiveEventSchema.md)
- [AddAccountSchema](docs/Model/AddAccountSchema.md)
- [AddCharacterSchema](docs/Model/AddCharacterSchema.md)
- [BadgeConditionSchema](docs/Model/BadgeConditionSchema.md)
- [BadgeResponseSchema](docs/Model/BadgeResponseSchema.md)
- [BadgeSchema](docs/Model/BadgeSchema.md)
- [BankExtensionSchema](docs/Model/BankExtensionSchema.md)
- [BankExtensionTransactionResponseSchema](docs/Model/BankExtensionTransactionResponseSchema.md)
- [BankExtensionTransactionSchema](docs/Model/BankExtensionTransactionSchema.md)
- [BankGoldTransactionResponseSchema](docs/Model/BankGoldTransactionResponseSchema.md)
- [BankGoldTransactionSchema](docs/Model/BankGoldTransactionSchema.md)
- [BankItemTransactionResponseSchema](docs/Model/BankItemTransactionResponseSchema.md)
- [BankItemTransactionSchema](docs/Model/BankItemTransactionSchema.md)
- [BankResponseSchema](docs/Model/BankResponseSchema.md)
- [BankSchema](docs/Model/BankSchema.md)
- [ChangePassword](docs/Model/ChangePassword.md)
- [ChangeSkinCharacterDataSchema](docs/Model/ChangeSkinCharacterDataSchema.md)
- [ChangeSkinCharacterSchema](docs/Model/ChangeSkinCharacterSchema.md)
- [ChangeSkinResponseSchema](docs/Model/ChangeSkinResponseSchema.md)
- [CharacterFightDataSchema](docs/Model/CharacterFightDataSchema.md)
- [CharacterFightResponseSchema](docs/Model/CharacterFightResponseSchema.md)
- [CharacterFightSchema](docs/Model/CharacterFightSchema.md)
- [CharacterLeaderboardSchema](docs/Model/CharacterLeaderboardSchema.md)
- [CharacterLeaderboardType](docs/Model/CharacterLeaderboardType.md)
- [CharacterMovementDataSchema](docs/Model/CharacterMovementDataSchema.md)
- [CharacterMovementResponseSchema](docs/Model/CharacterMovementResponseSchema.md)
- [CharacterMultiFightResultSchema](docs/Model/CharacterMultiFightResultSchema.md)
- [CharacterResponseSchema](docs/Model/CharacterResponseSchema.md)
- [CharacterRestDataSchema](docs/Model/CharacterRestDataSchema.md)
- [CharacterRestResponseSchema](docs/Model/CharacterRestResponseSchema.md)
- [CharacterSchema](docs/Model/CharacterSchema.md)
- [CharacterSkin](docs/Model/CharacterSkin.md)
- [CharacterTransitionDataSchema](docs/Model/CharacterTransitionDataSchema.md)
- [CharacterTransitionResponseSchema](docs/Model/CharacterTransitionResponseSchema.md)
- [CharactersListSchema](docs/Model/CharactersListSchema.md)
- [ClaimPendingItemDataSchema](docs/Model/ClaimPendingItemDataSchema.md)
- [ClaimPendingItemResponseSchema](docs/Model/ClaimPendingItemResponseSchema.md)
- [CombatResultSchema](docs/Model/CombatResultSchema.md)
- [CombatSimulationDataSchema](docs/Model/CombatSimulationDataSchema.md)
- [CombatSimulationRequestSchema](docs/Model/CombatSimulationRequestSchema.md)
- [CombatSimulationResponseSchema](docs/Model/CombatSimulationResponseSchema.md)
- [ConditionOperator](docs/Model/ConditionOperator.md)
- [ConditionSchema](docs/Model/ConditionSchema.md)
- [CooldownSchema](docs/Model/CooldownSchema.md)
- [CraftSchema](docs/Model/CraftSchema.md)
- [CraftSkill](docs/Model/CraftSkill.md)
- [CraftingSchema](docs/Model/CraftingSchema.md)
- [DataPageAccountAchievementSchema](docs/Model/DataPageAccountAchievementSchema.md)
- [DataPageAccountLeaderboardSchema](docs/Model/DataPageAccountLeaderboardSchema.md)
- [DataPageActiveCharacterSchema](docs/Model/DataPageActiveCharacterSchema.md)
- [DataPageCharacterLeaderboardSchema](docs/Model/DataPageCharacterLeaderboardSchema.md)
- [DataPageGEOrderSchema](docs/Model/DataPageGEOrderSchema.md)
- [DataPageGeOrderHistorySchema](docs/Model/DataPageGeOrderHistorySchema.md)
- [DataPageLogSchema](docs/Model/DataPageLogSchema.md)
- [DataPagePendingItemSchema](docs/Model/DataPagePendingItemSchema.md)
- [DataPageSimpleItemSchema](docs/Model/DataPageSimpleItemSchema.md)
- [DeleteCharacterSchema](docs/Model/DeleteCharacterSchema.md)
- [DeleteItemResponseSchema](docs/Model/DeleteItemResponseSchema.md)
- [DeleteItemSchema](docs/Model/DeleteItemSchema.md)
- [DepositWithdrawGoldSchema](docs/Model/DepositWithdrawGoldSchema.md)
- [DestinationSchema](docs/Model/DestinationSchema.md)
- [DropRateSchema](docs/Model/DropRateSchema.md)
- [DropSchema](docs/Model/DropSchema.md)
- [EffectResponseSchema](docs/Model/EffectResponseSchema.md)
- [EffectSchema](docs/Model/EffectSchema.md)
- [EffectSubtype](docs/Model/EffectSubtype.md)
- [EffectType](docs/Model/EffectType.md)
- [EquipRequestSchema](docs/Model/EquipRequestSchema.md)
- [EquipSchema](docs/Model/EquipSchema.md)
- [EquipmentResponseSchema](docs/Model/EquipmentResponseSchema.md)
- [ErrorResponseSchema](docs/Model/ErrorResponseSchema.md)
- [ErrorSchema](docs/Model/ErrorSchema.md)
- [EventContentSchema](docs/Model/EventContentSchema.md)
- [EventMapSchema](docs/Model/EventMapSchema.md)
- [EventSchema](docs/Model/EventSchema.md)
- [FakeCharacterSchema](docs/Model/FakeCharacterSchema.md)
- [FightRequestSchema](docs/Model/FightRequestSchema.md)
- [FightResult](docs/Model/FightResult.md)
- [GEBuyOrderCreationSchema](docs/Model/GEBuyOrderCreationSchema.md)
- [GEBuyOrderSchema](docs/Model/GEBuyOrderSchema.md)
- [GECancelOrderSchema](docs/Model/GECancelOrderSchema.md)
- [GECreateOrderTransactionResponseSchema](docs/Model/GECreateOrderTransactionResponseSchema.md)
- [GEFillBuyOrderSchema](docs/Model/GEFillBuyOrderSchema.md)
- [GEOrderCreatedSchema](docs/Model/GEOrderCreatedSchema.md)
- [GEOrderCreationrSchema](docs/Model/GEOrderCreationrSchema.md)
- [GEOrderResponseSchema](docs/Model/GEOrderResponseSchema.md)
- [GEOrderSchema](docs/Model/GEOrderSchema.md)
- [GEOrderTransactionSchema](docs/Model/GEOrderTransactionSchema.md)
- [GEOrderType](docs/Model/GEOrderType.md)
- [GETransactionListSchema](docs/Model/GETransactionListSchema.md)
- [GETransactionResponseSchema](docs/Model/GETransactionResponseSchema.md)
- [GETransactionSchema](docs/Model/GETransactionSchema.md)
- [GatheringSkill](docs/Model/GatheringSkill.md)
- [GeOrderHistorySchema](docs/Model/GeOrderHistorySchema.md)
- [GiveGoldDataSchema](docs/Model/GiveGoldDataSchema.md)
- [GiveGoldResponseSchema](docs/Model/GiveGoldResponseSchema.md)
- [GiveGoldSchema](docs/Model/GiveGoldSchema.md)
- [GiveItemDataSchema](docs/Model/GiveItemDataSchema.md)
- [GiveItemResponseSchema](docs/Model/GiveItemResponseSchema.md)
- [GiveItemsSchema](docs/Model/GiveItemsSchema.md)
- [GoldSchema](docs/Model/GoldSchema.md)
- [HTTPValidationError](docs/Model/HTTPValidationError.md)
- [InteractionSchema](docs/Model/InteractionSchema.md)
- [InventorySlot](docs/Model/InventorySlot.md)
- [ItemResponseSchema](docs/Model/ItemResponseSchema.md)
- [ItemSchema](docs/Model/ItemSchema.md)
- [ItemSlot](docs/Model/ItemSlot.md)
- [ItemType](docs/Model/ItemType.md)
- [LocationInner](docs/Model/LocationInner.md)
- [LogSchema](docs/Model/LogSchema.md)
- [LogType](docs/Model/LogType.md)
- [MapAccessType](docs/Model/MapAccessType.md)
- [MapContentSchema](docs/Model/MapContentSchema.md)
- [MapContentType](docs/Model/MapContentType.md)
- [MapLayer](docs/Model/MapLayer.md)
- [MapResponseSchema](docs/Model/MapResponseSchema.md)
- [MapSchema](docs/Model/MapSchema.md)
- [MonsterResponseSchema](docs/Model/MonsterResponseSchema.md)
- [MonsterSchema](docs/Model/MonsterSchema.md)
- [MonsterType](docs/Model/MonsterType.md)
- [MyAccountDetails](docs/Model/MyAccountDetails.md)
- [MyAccountDetailsSchema](docs/Model/MyAccountDetailsSchema.md)
- [MyCharactersListSchema](docs/Model/MyCharactersListSchema.md)
- [NPCItem](docs/Model/NPCItem.md)
- [NPCResponseSchema](docs/Model/NPCResponseSchema.md)
- [NPCSchema](docs/Model/NPCSchema.md)
- [NPCType](docs/Model/NPCType.md)
- [NpcItemTransactionSchema](docs/Model/NpcItemTransactionSchema.md)
- [NpcMerchantBuySchema](docs/Model/NpcMerchantBuySchema.md)
- [NpcMerchantTransactionResponseSchema](docs/Model/NpcMerchantTransactionResponseSchema.md)
- [NpcMerchantTransactionSchema](docs/Model/NpcMerchantTransactionSchema.md)
- [PasswordResetConfirmSchema](docs/Model/PasswordResetConfirmSchema.md)
- [PasswordResetRequestSchema](docs/Model/PasswordResetRequestSchema.md)
- [PasswordResetResponseSchema](docs/Model/PasswordResetResponseSchema.md)
- [PendingItemSchema](docs/Model/PendingItemSchema.md)
- [PendingItemSource](docs/Model/PendingItemSource.md)
- [RateLimitSchema](docs/Model/RateLimitSchema.md)
- [RecyclingDataSchema](docs/Model/RecyclingDataSchema.md)
- [RecyclingItemsSchema](docs/Model/RecyclingItemsSchema.md)
- [RecyclingResponseSchema](docs/Model/RecyclingResponseSchema.md)
- [RecyclingSchema](docs/Model/RecyclingSchema.md)
- [ResourceResponseSchema](docs/Model/ResourceResponseSchema.md)
- [ResourceSchema](docs/Model/ResourceSchema.md)
- [ResponseSchema](docs/Model/ResponseSchema.md)
- [RewardDataResponseSchema](docs/Model/RewardDataResponseSchema.md)
- [RewardDataSchema](docs/Model/RewardDataSchema.md)
- [RewardItemSchema](docs/Model/RewardItemSchema.md)
- [RewardResponseSchema](docs/Model/RewardResponseSchema.md)
- [RewardsSchema](docs/Model/RewardsSchema.md)
- [SeasonBadgeSchema](docs/Model/SeasonBadgeSchema.md)
- [SeasonSchema](docs/Model/SeasonSchema.md)
- [SeasonSkinSchema](docs/Model/SeasonSkinSchema.md)
- [SimpleEffectSchema](docs/Model/SimpleEffectSchema.md)
- [SimpleItemSchema](docs/Model/SimpleItemSchema.md)
- [SimpleNPCItem](docs/Model/SimpleNPCItem.md)
- [Skill](docs/Model/Skill.md)
- [SkillDataSchema](docs/Model/SkillDataSchema.md)
- [SkillInfoSchema](docs/Model/SkillInfoSchema.md)
- [SkillResponseSchema](docs/Model/SkillResponseSchema.md)
- [SpawnEventRequest](docs/Model/SpawnEventRequest.md)
- [StaticDataPageAchievementSchema](docs/Model/StaticDataPageAchievementSchema.md)
- [StaticDataPageActiveEventSchema](docs/Model/StaticDataPageActiveEventSchema.md)
- [StaticDataPageBadgeSchema](docs/Model/StaticDataPageBadgeSchema.md)
- [StaticDataPageDropRateSchema](docs/Model/StaticDataPageDropRateSchema.md)
- [StaticDataPageEffectSchema](docs/Model/StaticDataPageEffectSchema.md)
- [StaticDataPageEventSchema](docs/Model/StaticDataPageEventSchema.md)
- [StaticDataPageItemSchema](docs/Model/StaticDataPageItemSchema.md)
- [StaticDataPageMapSchema](docs/Model/StaticDataPageMapSchema.md)
- [StaticDataPageMonsterSchema](docs/Model/StaticDataPageMonsterSchema.md)
- [StaticDataPageNPCItem](docs/Model/StaticDataPageNPCItem.md)
- [StaticDataPageNPCSchema](docs/Model/StaticDataPageNPCSchema.md)
- [StaticDataPageResourceSchema](docs/Model/StaticDataPageResourceSchema.md)
- [StaticDataPageTaskFullSchema](docs/Model/StaticDataPageTaskFullSchema.md)
- [StatusResponseSchema](docs/Model/StatusResponseSchema.md)
- [StatusSchema](docs/Model/StatusSchema.md)
- [StorageEffectSchema](docs/Model/StorageEffectSchema.md)
- [TaskCancelledResponseSchema](docs/Model/TaskCancelledResponseSchema.md)
- [TaskCancelledSchema](docs/Model/TaskCancelledSchema.md)
- [TaskDataSchema](docs/Model/TaskDataSchema.md)
- [TaskFullResponseSchema](docs/Model/TaskFullResponseSchema.md)
- [TaskFullSchema](docs/Model/TaskFullSchema.md)
- [TaskResponseSchema](docs/Model/TaskResponseSchema.md)
- [TaskSchema](docs/Model/TaskSchema.md)
- [TaskTradeDataSchema](docs/Model/TaskTradeDataSchema.md)
- [TaskTradeResponseSchema](docs/Model/TaskTradeResponseSchema.md)
- [TaskTradeSchema](docs/Model/TaskTradeSchema.md)
- [TaskType](docs/Model/TaskType.md)
- [TokenResponseSchema](docs/Model/TokenResponseSchema.md)
- [TransitionSchema](docs/Model/TransitionSchema.md)
- [UnequipSchema](docs/Model/UnequipSchema.md)
- [UseItemResponseSchema](docs/Model/UseItemResponseSchema.md)
- [UseItemSchema](docs/Model/UseItemSchema.md)
- [ValidationError](docs/Model/ValidationError.md)

## Authorization

```php
/** @var ArtifactsMmo\Configuration */
Configuration::getDefaultConfiguration(
    ->setHost(config('artifacts.host'))
    ->setAccessToken(config('artifacts.token'));
```

- [Artifacts Host](https://api.artifactsmmo.com/docs/#/operations/get_server_details__get) (i.e. https://api.artifactsmmo.com)
- [Artifacts Token](https://artifactsmmo.com/my) (must be logged in)

### Usage

```php
/**
 * @return CharacterSchema[]
 */
protected function getMyCharacters(): array
{
    try {
        $config = Configuration::getDefaultConfiguration()
            ->setHost(config('artifacts.host'))
            ->setAccessToken(config('artifacts.token'));

        $api = new MyCharactersApi(config: $config);

        return $api->getMyCharactersMyCharactersGet()->getData();
    } catch (\Throwable $e) {
        Log::error('Could not get my characters');

        return [];
    }
}
```

Using a Service Provider (Laravel)
```php
/**
 * ArtifactsServiceProvider.php
 */
public function register(): void
{
    $this->app->singleton(Configuration::class, function () {
        return Configuration::getDefaultConfiguration()
            ->setHost(config('artifacts.host'))
            ->setAccessToken(config('artifacts.token'));
    });

    $this->app->bind(MyCharactersApi::class, function ($app) {
        return new MyCharactersApi(config: $app->make(Configuration::class));
    });
}

/**
 * Usage
 */
protected function getMyCharacters(): array
{
    try {
        return app(MyCharactersApi::class)
            ->getMyCharactersMyCharactersGet()
            ->getData();
    } catch (\Throwable $e) {
        Log::error('Could not get my characters');

        return [];
    }
}
```

## Author

The Artifacts MMO game: https://docs.artifactsmmo.com/funding 

Author of this package: [@ryanbeiden](https://github.com/ryanbeiden)

SDK Generated using: [OpenAPITools/openapi-generator](https://github.com/OpenAPITools/openapi-generator)

## About this package

API method for this PHP package are automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `7.0.4`
    - Package version: `1.0.0`
    - Generator version: `7.23.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
