---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: c68ad7def1b94796a020ffd29495e2b4c0b15a60
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466395"
---
# Set-AzRoleDefinition

## SYNOPSIS
Módosít egy egyéni szerepkört az Azure RBAC-ban.
Adja meg a módosított szerepkör-definíciót JSON-fájlként vagy PSRoleDefinition formátumban.
Először a Get-AzRoleDefinition paranccsal olvassa be a módosítani kívánt egyéni szerepkört.
Ezután módosítsa a módosítani kívánt tulajdonságokat.
Végül ezzel a paranccsal mentse a szerepkördefiníciót.

## SZINTAXIS

### InputFileParameterSet
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A Set-AzRoleDefinition parancsmag frissíti a meglévő egyéni szerepkört az Azure Role-Based Hozzáférés-vezérlésben.
Adja meg a frissített szerepkördefiníciót bemenetként a parancshoz JSON-fájlként vagy PSRoleDefinition objektumként.
A frissített egyéni szerepkör szerepkördefiníciójának tartalmaznia kell a szerepkör azonosítóját és minden más szükséges tulajdonságát, még akkor is, ha nem frissülnek: DisplayName, Leírás, Műveletek, AssignableScopes.
A NotActions, a DataActions és a NotDataActions paraméter megadása nem kötelező.
Az alábbiakban egy json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Műveletek": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \] , "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxxxx" \] }

## PÉLDÁK

### 1. példa: Frissítés a PSRoleDefinitionObject használatával
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### 2. példa: Létrehozás JSON-fájllal
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
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
A frissíthető json szerepkördefiníciót tartalmazó fájlnév.
Csak azok a tulajdonságok szerepeljenek, amelyek frissítve vannak a JSON-ban.
Id tulajdonság kötelező.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Szerepkör
Frissítend kell a szerepkör-definíciós objektumot

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## KIMENETEK

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## MEGJEGYZÉSEK
Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[New-AzRoleDefinition](./New-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

