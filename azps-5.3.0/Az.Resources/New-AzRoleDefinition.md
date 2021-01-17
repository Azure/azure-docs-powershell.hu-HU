---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466436"
---
# New-AzRoleDefinition

## SYNOPSIS
Egyéni szerepkört hoz létre az Azure RBAC-ban.
Adjon meg JSON szerepkördefiníciós fájlt vagy PSRoleDefinition objektumot bemenetként.
Először a Get-AzRoleDefinition paranccsal hozzon létre egy alaptervi szerepkör-definíciós objektumot.
Ezután szükség szerint módosítsa a tulajdonságait.
Végül ezzel a paranccsal szerepkördefiníció használatával hozhat létre egyéni szerepkört.

## SZINTAXIS

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A New-AzRoleDefinition parancsmag létrehoz egy egyéni szerepkört az Azure Role-Based Hozzáférés-vezérlésben.
Adjon meg szerepkördefiníciót a parancs bemeneteként JSON-fájlként vagy PSRoleDefinition objektumként.
A bemeneti szerepkör definíciójának az alábbi tulajdonságokat kell tartalmaznia:
1) DisplayName: az egyéni szerepkör neve
2) Leírás: a szerepkör rövid leírása, amely összegzi a szerepkör által nyújtott hozzáférést.
3) Műveletek: az a műveletkészlet, amelyhez az egyéni szerepkör hozzáférést biztosít.
A Get-AzProviderOperation azure-erőforrás-szolgáltatók azure RBAC-n keresztül is biztonságos műveleteket használhatja.
Az alábbiakban néhány érvényes műveleti karakterláncot is be kell íme:
 - A "*/read" hozzáféréssel rendelkezik az összes Azure-erőforrásszolgáltató olvasási műveleteihez.
 - A "Microsoft.Network/*/read" olvasási műveletekhez biztosít hozzáférést az Azure Microsoft.Network erőforrásszolgáltatójának összes erőforrástípusához.
 - A "Microsoft.Compute/virtualMachines/*" hozzáférést biztosít a virtuális gépek és a gyermekerőforrás-típusok minden művelethez.
4) AssignableScopes: az a hatókörcsoport (Azure-előfizetések vagy erőforráscsoportok), amelyekben az egyéni szerepkör elérhető lesz a hozzárendeléshez.
A AssignableScopes használatával az egyéni szerepkört csak az előfizetések vagy erőforráscsoportok számára teszi elérhetővé, a többi előfizetés vagy erőforráscsoport felhasználói élményét nem.
Íme néhány érvényes hozzárendelhető hatókör:
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": két előfizetésben elérhetővé teszi a szerepkört a hozzárendeléshez.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": elérhetővé teszi a szerepkört egyetlen előfizetésben való hozzárendeléshez.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": csak a Hálózati erőforráscsoportban teszi elérhetővé a hozzárendelést.
A bemeneti szerepkör definíciója az alábbi tulajdonságokat tartalmazhatja:
1) NotActions: azok a műveletek, amelyekből ki kell zárni az egyéni szerepkör tényleges műveleteinek meghatározásához.
Ha van egy olyan művelet, amelyhez nem szeretne hozzáférést adni egy egyéni szerepkörben, a NotActions segítségével egyszerűen kizárhatja azt, nem kell megadnia az adott műveleten kívül az összes műveletet a Műveletekben.
2) DataActions: az az adatművelet-készlet, amelyhez az egyéni szerepkör hozzáférést biztosít.
3) NotDataActions: azok a műveletek, amelyekből ki kell zárni a DataActions műveletből az egyéni szerepkör hatékony adatműveletének meghatározásához.
Ha van egy olyan adatművelet, amelyhez nem szeretne hozzáférést adni egy egyéni szerepkörben, a NotDataActions segítségével kizárhatja a műveletet, és nem kell az adott műveleten kívül más műveleteket megadnia a Műveletekben.
MEGJEGYZÉS: Ha egy felhasználóhoz olyan szerepkör van hozzárendelve, amely a NotActions műveletben meghatároz egy műveletet, és egy másik szerepkör is hozzáférést biztosít ugyanannak a műveletnek – a felhasználó képes lesz végrehajtani ezt a műveletet.
A NotActions nem elutasítási szabály – egyszerűen kényelmes módja az engedélyezett műveletek halmazának létrehozásához, ha bizonyos műveleteket ki kell zárni.
Az alábbiakban egy json szerepkördefiníciót tartalmazó minta található, amely bevitelként meg lehet adni a következőt: { "Név": "Frissített szerepkör", "Leírás": "Figyelheti az összes erőforrást, és elindíthatja és újraindíthatja a virtuális gépeket", "Műveletek": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/container blobs/blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxxxx" \] }

## PÉLDÁK

### 1. példa: Létrehozás a PSRoleDefinitionObject használatával
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### 2. példa: Létrehozás JSON-fájllal
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

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
Egy json-szerepkördefiníciót tartalmazó fájlnév.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Szerepkör
Szerepkör-definíciós objektum.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## MEGJEGYZÉSEK
Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

