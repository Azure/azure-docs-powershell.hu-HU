---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespaceauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceAuthorizationRule.md
ms.openlocfilehash: eaf34373cb17fea94c498e16f623cef4bf65e937
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467293"
---
# New-AzNotificationHubsNamespaceAuthorizationRule

## SYNOPSIS
Engedélyezési szabályt hoz létre, és hozzárendeli azt egy értesítési központ névterhez.

## SZINTAXIS

### InputFileParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzNotificationHubsNamespaceAuthorizationRule [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A **New-AzNotificationHubsNamespaceAuthorizationRule parancsmag** létrehoz egy SAS engedélyezési szabályt, és hozzárendeli egy értesítési központ névterhez.
Az engedélyezési szabályok kezelik a névtérhez és az adott névtérhez foglalt értesítési központok felhasználói jogait.
Ez a parancsmag két módszert biztosít új engedélyezési szabály létrehozására és névtérhez való hozzárendelésére.
Létrehozhatja a **SharedAccessAuthorizationRuleAttributes** objektum egy példányát, majd beállíthatja az objektumot a tulajdonságértékekkel, amelyekre az új szabálynak rendelkeznie kell.
Ezt a .NET-keretrendszer használatával lehet tenni.
Ezután az *SASRule* paraméter használatával átmásolhatja ezeket a tulajdonságértékeket az új szabályba.
Másik lehetőségként létrehozhat egy JSON (JavaScript objektum notation) fájlt, amely tartalmazza a vonatkozó konfigurációs értékeket, majd az *InputFile* paraméter használatával alkalmazza ezeket az értékeket.
A JSON-fájl olyan szövegfájl, amely a következő szintaxist használja: {  
    "Név": "ContosoAuthorizationRule",  
    "PrimaryKey": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y=",  
    "Jogok": \[  
        "Figyel",  
        "Küldés"  
    \]  
} A **New-AzNotificationHubsNamespaceAuthorizationRule** parancsmaggal együtt használva az előző JSON-minta létrehoz egy ContosoAuthorizationRule nevű engedélyezési szabályt, amely a felhasználó figyelási és küldési jogosultságát biztosítja a névtérhez.
A hitelesítéshez használt *PrimaryKey* a következő Windows PowerShell-paranccsal generálható véletlenszerűen: \[ Convert \] ::ToBase64String((1.32 |% { \[ bájt/](Get-Random -Minimum 0 -Maximum 255) }))

## PÉLDÁK

### 1. példa: Engedélyezési szabály létrehozása és hozzárendelése egy névtérhez
```
PS C:\>New-AzNotificationHubAuthorizationRule -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

Ez a parancs létrehoz egy engedélyezési szabályt, és hozzárendeli azt a ContosoNamespace névtérhez.
A szabály létrehozásakor meg kell adnia a megfelelő névteret és azt az erőforráscsoportot, amelyhez a névtér hozzá van rendelve.
Magára a szabályra vonatkozó információt azonban nem kell megadnia: a szabályinformációk a beviteli fájlból fognak C:\Configuration\NamespaceAuthorizationRules.jsbe.

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
Az új engedélyezési szabály konfigurációs adatait tartalmazó JSON-fájl elérési útját adja meg.

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
Azt a névteret adja meg, amelyhez az engedélyezési szabályokat hozzá kell rendelni.
A névterek lehetőséget nyújtanak az értesítési központok csoportosítására és kategorizálására.
Az új szabályokat hozzá kell rendelni egy meglévő névtérhez.
A **New-AzNotificationHubsNamespaceAuthorizationRule** parancsmag nem tud új névteret létrehozni.

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

### -ResourceGroup
Azt az erőforráscsoportot adja meg, amelyhez a névteret hozzárendelték.
Az erőforráscsoportok a készletkezelést és az Azure felügyeletét segítő módon rendszerezhetik az elemeket, például a névtereket, az értesítési központokat és az engedélyezési szabályokat.
Meglévő erőforráscsoportot kell használnia.
Ez a parancsmag nem tud új erőforráscsoportot létrehozni.

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

### -SASRule
Az új szabályok konfigurációs adatait tartalmazó **SharedAccessAuthorizationRuleAttributes** objektumot adja meg.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
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

### Microsoft.Azure.Commands.NotificationHubs.Models.SharedAccessAuthorizationRuleAttributes

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzNotificationHubAuthorizationRule](./Get-AzNotificationHubAuthorizationRule.md)

[Remove-AzNotificationHubAuthorizationRule](./Remove-AzNotificationHubAuthorizationRule.md)

[Set-AzNotificationHubAuthorizationRule](./Set-AzNotificationHubAuthorizationRule.md)


