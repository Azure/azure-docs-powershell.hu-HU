---
Module Name: Az.ServiceBus
Module Guid: cc69c625-e961-43f4-8b50-0061eba6e4b6
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicebus
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Az.ServiceBus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Az.ServiceBus.md
ms.openlocfilehash: ad8666a0524482521a5c1054ab46862ec6ce8dde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343698"
---
# Az.ServiceBus modul
## Leírás
Ez a témakör az Azure Service Bus parancsmagok súgótémakörét mutatja be.

## Az.ServiceBus-parancsmagok
### [Complete-AzServiceBusMigration](Complete-AzServiceBusMigration.md)
A parancsmagok az Áttelepítés standardról prémium névtérre teljesként, a normál névtér kapcsolati karakterláncai pedig a Prémium névtérre mutatnak

### [Get-AzServiceBusAuthorizationRule](Get-AzServiceBusAuthorizationRule.md)
Egy adott névtérhez, várólistához, témakörhez vagy aliashoz (GeoDR-konfigurációk) megadott engedélyezési szabály leírását kapja. 

### [Get-AzServiceBusGeoDRConfiguration](Get-AzServiceBusGeoDRConfiguration.md)
Beolvassa az alias(katasztrófa-helyreállítási konfiguráció) beállítást az elsődleges vagy másodlagos névtérhez

### [Get-AzServiceBusKey](Get-AzServiceBusKey.md)
A megadott Névtér, Várólista vagy Témakör vagy Alias (GeoDR-konfigurációk) elsődleges és másodlagos kapcsolati karakterláncát kapja meg.

### [Get-AzServiceBusMigration](Get-AzServiceBusMigration.md)
Beolvassa a MigrationConfiguration nevet a névtérhez

### [Get-AzServiceBusNamespace](Get-AzServiceBusNamespace.md)
Az erőforráscsoporton belül a szolgáltatás-busz névterének leírását adja meg.

### [Get-AzServiceBusOperation](Get-AzServiceBusOperation.md)
Támogatott ServiceBus-műveletek listája

### [Get-AzServiceBusQueue](Get-AzServiceBusQueue.md)
A megadott szolgáltatásbusz-várólistához ad leírást.

### [Get-AzServiceBusRule](Get-AzServiceBusRule.md)
Új szabályt hoz létre egy adott témakör-előfizetéshez. 

### [Get-AzServiceBusSubscription](Get-AzServiceBusSubscription.md)
A megadott témakör előfizetési leírását adja eredményül.

### [Get-AzServiceBusTopic](Get-AzServiceBusTopic.md)
A megadott Service Bus-témakör leírását adja eredményül.

### [New-AzServiceBusAuthorizationRule](New-AzServiceBusAuthorizationRule.md)
Új engedélyezési szabályt hoz létre a megadott Service Bus névterhez, várólistához vagy témakörhez.

### [New-AzServiceBusAuthorizationRuleSASToken](New-AzServiceBusAuthorizationRuleSASToken.md)
Egy SAS-tolen-t hoz létre a névtér/várólista/témakör Azure serviucebus engedélyezési szabályához. 

### [New-AzServiceBusGeoDRConfiguration](New-AzServiceBusGeoDRConfiguration.md)
Létrehoz egy új aliast(katasztrófa-helyreállítási konfiguráció)

### [New-AzServiceBusKey](New-AzServiceBusKey.md)
A Szolgáltatásbusz névterében, illetve várólistában vagy témakörben található elsődleges vagy másodlagos kapcsolati karakterláncok újragenerálása.

### [New-AzServiceBusNamespace](New-AzServiceBusNamespace.md)
Új Service Bus névteret hoz létre.

### [New-AzServiceBusQueue](New-AzServiceBusQueue.md)
Szolgáltatásbusz-várólistát hoz létre a szolgáltatásbusz névterében.

### [New-AzServiceBusRule](New-AzServiceBusRule.md)
Új szabályt hoz létre egy adott témakör-előfizetéshez. 

### [New-AzServiceBusSubscription](New-AzServiceBusSubscription.md)
Létrehoz egy előfizetést a megadott Service Bus témához.

### [New-AzServiceBusTopic](New-AzServiceBusTopic.md)
Létrehoz egy új Service Bus-témakört a megadott Service Bus névterében.

### [Remove-AzServiceBusAuthorizationRule](Remove-AzServiceBusAuthorizationRule.md)
Eltávolítja egy szolgáltatásbusz névterének vagy várólistájának vagy témájának engedélyezési szabályát a megadott erőforráscsoportból.

### [Remove-AzServiceBusGeoDRConfiguration](Remove-AzServiceBusGeoDRConfiguration.md)
Alias törlése(Katasztrófa-helyreállítás konfiguráció)

### [Remove-AzServiceBusMigration](Remove-AzServiceBusMigration.md)
Parancsmag törli a Standard–Premium névterek áttelepítési konfigurációját

### [Remove-AzServiceBusNamespace](Remove-AzServiceBusNamespace.md)
Eltávolítja a névteret a megadott erőforráscsoportból. 

### [Remove-AzServiceBusQueue](Remove-AzServiceBusQueue.md)
Eltávolítja a várólistát a szolgáltatásbusz megadott névterében.

### [Remove-AzServiceBusRule](Remove-AzServiceBusRule.md)
Egy adott előfizetés megadott szabályának eltávolítása.

### [Remove-AzServiceBusSubscription](Remove-AzServiceBusSubscription.md)
Eltávolítja egy témakör előfizetését a megadott Service Bus névtérből.

### [Remove-AzServiceBusTopic](Remove-AzServiceBusTopic.md)
Eltávolítja a témakört a szolgáltatásbusz megadott névterében.

### [Set-AzServiceBusAuthorizationRule](Set-AzServiceBusAuthorizationRule.md)
Frissíti a szolgáltatási-busz névterének vagy várólistájának vagy témájának engedélyezési szabályának megadott leírását.

### [Set-AzServiceBusGeoDRConfigurationBreakPair](Set-AzServiceBusGeoDRConfigurationBreakPair.md)
Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja a módosítások elsődlegesről másodlagos névterekbe való replikálását.

### [Set-AzServiceBusGeoDRConfigurationFailOver](Set-AzServiceBusGeoDRConfigurationFailOver.md)
A GEO DR feladatátvételének meghívása és az alias újrakonfigurálása a másodlagos névtérre

### [Set-AzServiceBusNamespace](Set-AzServiceBusNamespace.md)
Frissíti egy meglévő Szolgáltatásbusz névterének leírását.

### [Set-AzServiceBusQueue](Set-AzServiceBusQueue.md)
Frissíti a Szolgáltatásbusz várólistájának leírását a megadott Service Bus névterében.

### [Set-AzServiceBusRule](Set-AzServiceBusRule.md)
Frissíti az adott előfizetéshez megadott szabályleírást.

### [Set-AzServiceBusSubscription](Set-AzServiceBusSubscription.md)
Frissíti a Szolgáltatásbusz témakör előfizetési leírását a megadott Service Bus névterében.

### [Set-AzServiceBusTopic](Set-AzServiceBusTopic.md)
Frissíti a Szolgáltatásbusz témakör leírását a megadott Service Bus névterében.

### [Start-AzServiceBusMigration](Start-AzServiceBusMigration.md)
Új áttelepítési konfigurációt hoz létre, és megkezdi az entitások áttelepítését a Standardból a Prémium névterekbe

### [Stop-AzServiceBusMigration](Stop-AzServiceBusMigration.md)
{{Fill in the Synopsis}}

### [Test-AzServiceBusName](Test-AzServiceBusName.md)
A megadott Névtérnév vagy Alias elérhetőségének ellenőrzése (DR konfiguráció neve) 

