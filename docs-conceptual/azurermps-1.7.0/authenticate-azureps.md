---
title: Bejelentkezés az Azure PowerShell-lel
description: Bejelentkezés az Azure PowerShell-lel
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 52a2ccba1886c2761d66aee52b27d66e8da4d630
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: hu-HU
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821836"
---
# <a name="log-in-with-azure-powershell"></a>Bejelentkezés az Azure PowerShell-lel

Az Azure PowerShell többféle bejelentkezési módszert támogat. Első lépésként a legegyszerűbb módszer, ha interaktívan bejelentkezik a parancssoron.

## <a name="interactive-log-in"></a>Interaktív bejelentkezés

1. Gépelje be: `Login-AzureRmAccount`. Egy párbeszédpanel jelenik meg, amelyen meg kell adnia Azure-beli hitelesítő adatait.

2. Írja be a fiókjához tartozó e-mail-címet és jelszót. Az Azure hitelesíti és menti a hitelesítő adatokat, majd bezárja az ablakot.

## <a name="log-in-with-a-service-principal"></a>Bejelentkezés szolgáltatásnévvel

A szolgáltatásnevek használatával nem interaktív fiókokat hozhat létre az erőforrások kezeléséhez. A szolgáltatásnevek olyan felhasználói fiókokhoz hasonlóak, amelyekre szabályokat alkalmazhat az Azure Active Directory használatával. Az automatizálási szkriptek biztonságának növelése érdekében csak a minimálisan szükséges engedélyeket adja meg a szolgáltatásneveknek.

1. Ha még nem rendelkezik szolgáltatásnévvel, akkor [hozzon létre egyet](create-azure-service-principal-azureps.md).

2. Jelentkezzen be a szolgáltatásnévvel.

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    A bérlőazonosító megismeréséhez jelentkezzen be interaktívan, és kérje le az előfizetésből.

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a>Bejelentkezés Azure-beli virtuális gépek felügyeltszolgáltatás-identitásaival

A Felügyeltszolgáltatás-identitás (MSI) az Azure Active Directory előzetes verzióként elérhető funkciója. Az MSI szolgáltatásnevekkel bejelentkezhet, és beszerezhet egy csak alkalmazásra érvényes hozzáférési jogkivonatot az egyéb erőforrások eléréséhez.

További információ az MSI-ről: [Az Azure-beli virtuális gépek felügyeltszolgáltatás-identitásának (MSI) használata bejelentkezéshez és jogkivonat beszerzéséhez](/azure/active-directory/msi-how-to-get-access-token-using-msi).

## <a name="log-in-to-another-cloud"></a>Bejelentkezés egy másik felhőbe

Az Azure-beli felhőszolgáltatások különböző környezeteket biztosítanak, amelyek igazodnak az egyes kormányzatok adatkezelési szabályzataihoz. Ha az Azure-fiók valamelyik kormányzati felhőben található, bejelentkezéskor meg kell adnia a környezetet. Például ha a fiók a kínai felhőszolgáltatásban található, a regisztrálás az alábbi paranccsal történik:

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

Az alábbi paranccsal olvashatja be a rendelkezésre álló környezetek listáját:

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>További információ az Azure szerepkör-alapú hozzáférés kezeléséről

Az Azure-beli hitelesítésről és előfizetés-kezelésről a [fiókok, előfizetések és rendszergazdai szerepkörök kezeléséről](/azure/active-directory/role-based-access-control-configure) szóló cikkben talál további információt.

Azure PowerShell-parancsmagok a szerepkörök kezeléséhez

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
