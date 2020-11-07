---
Module Name: Az.EventHub
Module Guid: 5728d353-7ad5-42d8-b00a-46aaecf07b91
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.eventhub
Help Version: 4.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Az.EventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Az.EventHub.md
ms.openlocfilehash: 473672fd5cae2f8046fcce6102316deb0566e65a
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/23/2019
ms.locfileid: "93657785"
---
# Az. EventHub modul
## Leírás
Ez a témakör a súgót jeleníti meg az Azure Event hub PowerShell erőforrás-kezelő parancsmagjai között.

## Az. EventHub parancsmagok
### [Add-AzEventHubIPRule](Add-AzEventHubIPRule.md)
Egyetlen IPrule felvétele a megadott névtér NetworkRuleSet

### [Add-AzEventHubVirtualNetworkRule](Add-AzEventHubVirtualNetworkRule.md)
Egyetlen VirtualNetworkRule hozzáadása a NetworkRuleSet a megadott névtérhez

### [Get-AzEventHub](Get-AzEventHub.md)
Beolvassa az egyetlen esemény központjának részleteit, vagy megkapja az esemény-hubok listáját.

### [Get-AzEventHubAuthorizationRule](Get-AzEventHubAuthorizationRule.md)
Egy engedélyezési szabály részleteit kapja meg, vagy megkapja az engedélyezési szabályok listáját.

### [Get-AzEventHubConsumerGroup](Get-AzEventHubConsumerGroup.md)
A megadott esemény-hubok fogyasztói csoportjának részleteit kapja meg, vagy a fogyasztói csoportok listáját egy esemény központjában kapja.

### [Get-AzEventHubGeoDRConfiguration](Get-AzEventHubGeoDRConfiguration.md)
Az elsődleges vagy másodlagos névtérhez tartozó alias (katasztrófa-helyreállítási konfiguráció) beolvasása

### [Get-AzEventHubKey](Get-AzEventHubKey.md)
A megadott esemény-hubok engedélyezési szabályának elsődleges kulcsait kapja meg.

### [Get-AzEventHubNamespace](Get-AzEventHubNamespace.md)
Beolvassa az esemény-hubok névterének részleteit, vagy az aktuális Azure-előfizetésből az összes esemény-hubok névterének listáját kapja.

### [Get-AzEventHubNetworkRuleSet](Get-AzEventHubNetworkRuleSet.md)
Az aktuális Azure-előfizetésben az esemény-hubok NetwrokruleSet részleteit kapja meg.

### [Új – AzEventHub](New-AzEventHub.md)
Új esemény-hubot hoz létre.

### [Új – AzEventHubAuthorizationRule](New-AzEventHubAuthorizationRule.md)
Új esemény-hubok engedélyezési szabályának létrehozása a névtérhez vagy a eventhub.

### [Új – AzEventHubConsumerGroup](New-AzEventHubConsumerGroup.md)
Új fogyasztói csoportot hoz létre a megadott esemény központhoz.

### [Új – AzEventHubGeoDRConfiguration](New-AzEventHubGeoDRConfiguration.md)
Új alias létrehozása (katasztrófa-helyreállítási konfiguráció)

### [Új – AzEventHubKey](New-AzEventHubKey.md)
Új elsődleges vagy másodlagos kulcs létrehozása a megadott esemény-hubok engedélyezési szabályához.

### [Új – AzEventHubNamespace](New-AzEventHubNamespace.md)
Esemény-hubok névteret hoz létre.

### [Remove-AzEventHubIPRule](Remove-AzEventHubIPRule.md)
Egyetlen IPrule eltávolítása a megadott névtér NetworkRuleSet

### [Remove-AzEventHub](Remove-AzEventHub.md)
Eltávolítja a megadott esemény hub-ot.

### [Remove-AzEventHubVirtualNetworkRule](Remove-AzEventHubVirtualNetworkRule.md)
A névtér NetworkRuleSet egyetlen adott VirtualNetworkRule eltávolítása

### [Remove-AzEventHubNetworkRuleSet](Remove-AzEventHubNetworkRuleSet.md)
A megadott névtér NetwrokRuleSet eltávolítása

### [Remove-AzEventHubAuthorizationRule](Remove-AzEventHubAuthorizationRule.md)
Eltávolítja a megadott esemény központi engedélyezési szabályát.

### [Remove-AzEventHubConsumerGroup](Remove-AzEventHubConsumerGroup.md)
Törli a megadott esemény-hubok fogyasztói csoportját.

### [Remove-AzEventHubGeoDRConfiguration](Remove-AzEventHubGeoDRConfiguration.md)
Alias törlése (katasztrófa-helyreállítási konfiguráció)

### [Remove-AzEventHubNamespace](Remove-AzEventHubNamespace.md)
Eltávolítja a megadott esemény-hubok névteret.

### [Set-AzEventHub](Set-AzEventHub.md)
Frissíti a megadott esemény hub-ot.

### [Set-AzEventHubAuthorizationRule](Set-AzEventHubAuthorizationRule.md)
A megadott engedélyezési szabály frissítése az esemény központjában.

### [Set-AzEventHubConsumerGroup](Set-AzEventHubConsumerGroup.md)
Frissíti a megadott esemény-hubok fogyasztói csoportját.

### [Set-AzEventHubGeoDRConfigurationBreakPair](Set-AzEventHubGeoDRConfigurationBreakPair.md)
Ez a művelet letiltja a katasztrófa-helyreállítást, és leállítja az elsődlegestől a másodlagos névtérig történő módosítások replikálását.

### [Set-AzEventHubGeoDRConfigurationFailOver](Set-AzEventHubGeoDRConfigurationFailOver.md)
A GEO DR feladatátvételt hívja meg, és a másodlagos névtérre irányítja át az aliast.

### [Set-AzEventHubNamespace](Set-AzEventHubNamespace.md)
Frissíti a megadott esemény-hubok névteret.

### [Set-AzEventHubNetworkRuleSet](Set-AzEventHubNetworkRuleSet.md)
Frissítse az aktuális Azure-előfizetés adott Namepsace NetwrokruleSet.

### [Teszt-AzEventHubName](Test-AzEventHubName.md)
A megadott névtérbeli név vagy alias elérhetőségének ellenőrzése (DR. konfigurációs név)
