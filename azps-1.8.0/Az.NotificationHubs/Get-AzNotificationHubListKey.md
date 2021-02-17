---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 326C87EB-EC3B-4B04-B593-EAC56FFA854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/get-aznotificationhublistkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Get-AzNotificationHubListKey.md
ms.openlocfilehash: 7ce6c3c08c1794e2bed794186203a5c6c0d1fdea
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399889"
---
# Get-AzNotificationHubListKey

## SYNOPSIS
Egy értesítési központ engedélyezési szabályához társított elsődleges és másodlagos kapcsolati karakterláncokat kapja meg.

## SZINTAXIS

```
Get-AzNotificationHubListKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [-AuthorizationRule] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A **Get-AzNotificationHubListKey** parancsmag egy értesítési központ Megosztott hozzáférés-aláírás (SAS) engedélyezési szabályának elsődleges és másodlagos kapcsolati karakterláncát adja vissza.
Az engedélyezési szabályok kezelik a felhasználói jogokat a központban.
Minden szabály tartalmaz egy elsődleges és egy másodlagos kapcsolati karakterláncot.
Az alábbi kapcsolati karakterláncok (URI-k) az alábbi műveleteket hajtják végre:
- Mutasson a felhasználóknak egy erőforrásra.
- Lekérdezésparamétereket tartalmazó jogkivonatot is tartalmazhat.
A paraméterek egyike, az aláírás a felhasználó hitelesítésére és a megadott szintű hozzáférés elérésére használható.

## PÉLDÁK

### 1. példa: Az engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncának le kérése
```
PS C:\>Get-AzNotificationHubListKey -Namespace "ContosoNamespace" -NotificationHub "ContosoInternalHub" -ResourceGroup "ContosoNotificationsGroup" -AuthorizationRule "ListenRule"
```

Ez a parancs a ContosoInternalHub értesítési központhoz rendelt szabály, a ListenRule engedélyezési szabály elsődleges és másodlagos kapcsolati karakterláncát kapja meg.
A parancsnak tartalmaznia kell a központi névteret és az erőforráscsoportot.

## PARAMETERS

### -AuthorizationRule
A megosztott hozzáférésű aláírás (SAS) hitelesítési szabály nevét adja meg.
Ezek a szabályok határozzák meg, hogy a felhasználók milyen típusú hozzáféréssel férnek hozzá az értesítési központhoz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Azt a névteret adja meg, amelyhez az értesítési központ hozzá van rendelve.
A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationHub
Azt az értesítési központot adja meg, amelyhez ez a parancsmag engedélyezési szabályt rendel.
Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek attól függetlenül, hogy milyen platformon használják őket.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
Azt az erőforráscsoportot adja meg, amelyhez az értesítési központ hozzá van rendelve.
Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK



