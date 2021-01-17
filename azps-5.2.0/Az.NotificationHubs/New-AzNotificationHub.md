---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 8EDDA991-55B6-4151-8619-E13E14599ECD
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHub.md
ms.openlocfilehash: 3fb98dc1ef4b13b87fc7cfa41e165d9bc24fc17c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336222"
---
# New-AzNotificationHub

## SYNOPSIS
Létrehoz egy értesítési központot.

## SZINTAXIS

### InputFileParameterSet
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NotificationHubParameterSet
```
New-AzNotificationHub [-ResourceGroup] <String> [-Namespace] <String>
 [-NotificationHubObj] <NotificationHubAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzNotificationHub** parancsmag létrehoz egy értesítési központot.
Az értesítési központokkal leküldéses értesítéseket lehet küldeni több ügyfélnek attól függetlenül, hogy milyen platformon használják őket.
Az értesítési központok nagyjából egyenértékűek az egyes appokkal: mindegyik alkalmazásnak általában saját értesítési központja lesz.
A **New-AzNotificationHub** parancsmag kétféleképpen hozhat létre új értesítési központot.
Létrehozhatja az **NotificationHubAttributes** objektum egy példányát, majd beállíthatja azt.
Ezután az *NotificationHubObj* paraméterrel átmásolhatja ezeket a tulajdonságértékeket az új központba.
Másik lehetőségként létrehozhat egy JSON (JavaScript objektum notation) fájlt, amely tartalmazza a vonatkozó konfigurációs értékeket, majd az *InputFile* paraméter használatával alkalmazza ezeket az értékeket.
A **New-AzNotificationHub** parancsmaggal együtt használva az előző JSON-minta létrehoz egy ContosoNotificationHub nevű értesítési központot az EGYESÜLT ÁLLAMOK nyugati részén található adatközpontban.

## PÉLDÁK

### 1. példa: Értesítési központ létrehozása
```
PS C:\>New-AzNotificationHub -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configurations\InternalHub.json"
```

Ez a parancs létrehoz egy értesítési központot a ContosoNamespace névterében.
Az új központ hozzá lesz rendelve a ContosoNotificationsGroup csoporthoz.
Nem kell megadnia a központ nevét vagy egyéb konfigurációs adatait; adatokat a rendszer a bemeneti fájlból fogja C:\Configurations\InternalHub.jsbe.

## PARAMETERS

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

### -InputFile
Az új értesítési központ konfigurációs értékeit tartalmazó JSON-fájl elérési útját adja meg.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Azt a névteret adja meg, amelyhez az értesítési központot hozzá kell rendelni.
A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.
Az értesítési központokat hozzá kell rendelni egy meglévő névtérhez.
A **New-AzNotificationHub** parancsmag nem tud új névteret létrehozni.

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

### -NotificationHubObj
Az új központ konfigurációs adatait tartalmazó **NotificationHubAttributes** objektumot adja meg.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes
Parameter Sets: NotificationHubParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
Azt az erőforráscsoportot adja meg, amelyhez az értesítési központot hozzá kell rendelni.
Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.
Meglévő erőforráscsoportot kell használnia.
A **New-AzNotificationHub** parancsmag nem tud új erőforráscsoportot létrehozni.

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

### -Confirm
A parancsmag futtatása előtt a rendszer megerősítést kér.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
A parancsmag futtatásakor a program megjeleníti, hogy mi történik. A parancsmag nem fut.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.NotificationHubs.Models.NotificationHubAttributes

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHub](./Get-AzNotificationHub.md)

[Remove-AzNotificationHub](./Remove-AzNotificationHub.md)

[Set-AzNotificationHub](./Set-AzNotificationHub.md)


