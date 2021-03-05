---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8C1D738C-825D-4718-AD2A-9CFEAA7DBD3B
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleAssignment.md
ms.openlocfilehash: d941e5cc3bf4a3f2363aa8369a7f5b0518ba2e07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005798"
---
# Remove-AzRoleAssignment

## SYNOPSIS
Eltávolít egy szerepkör-hozzárendelést a megadott egyszerű felhasználóhoz, aki egy adott szerepkörhöz van hozzárendelve egy adott hatókörben.

## SZINTAXIS

### EmptyParameterSet (alapértelmezett)
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceWithObjectIdParameterSet
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceGroupWithObjectIdParameterSet
```
Remove-AzRoleAssignment -ObjectId <String> -ResourceGroupName <String> -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScopeWithObjectIdParameterSet
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RoleIdWithScopeAndObjectIdParameterSet
```
Remove-AzRoleAssignment -ObjectId <String> [-Scope <String>] -RoleDefinitionId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceWithSignInNameParameterSet
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceGroupWithSignInNameParameterSet
```
Remove-AzRoleAssignment -SignInName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScopeWithSignInNameParameterSet
```
Remove-AzRoleAssignment -SignInName <String> [-Scope <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceWithSPNParameterSet
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -ResourceName <String>
 -ResourceType <String> [-ParentResource <String>] -RoleDefinitionName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceGroupWithSPNParameterSet
```
Remove-AzRoleAssignment -ServicePrincipalName <String> -ResourceGroupName <String> -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ScopeWithSPNParameterSet
```
Remove-AzRoleAssignment -ServicePrincipalName <String> [-Scope <String>] -RoleDefinitionName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RoleAssignmentParameterSet
```
Remove-AzRoleAssignment [-PassThru] [-InputObject] <PSRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## LEÍRÁS
A Remove-AzRoleAssignment parancsmag használatával visszavonhatja a hozzáférést egy adott hatókörű és szerepkörű egyszerű felhasználóhoz.
A feladat objektuma, vagyis a főnévnek meg kell adni.
A rendszernév lehet felhasználó (a SignInName vagy az ObjectId paramétert használva azonosíthat egy felhasználót), biztonsági csoport (csoport azonosításához használja az ObjectId paramétert) vagy egyszerű szolgáltatásnév (a ServicePrincipalName vagy az ObjectId paramétert használva azonosítsa a ServicePrincipal paramétert).
A SzerepkörDefinitionName paraméterrel meg kell adni azt a szerepkört, amelyhez a főnév hozzá van rendelve.
Előfordulhat, hogy a hozzárendelés hatóköre meg van adva, és ha nincs megadva, akkor az előfizetés hatóköre lesz alapértelmezett, vagyis megpróbálja törölni a megadott fő és szerepkörhöz tartozó hozzárendelést az előfizetés hatókörében.
A hozzárendelés hatóköre az alábbi paraméterek egyikével is megadva lehet.
a.
Hatókör – Ez a teljes hatókör az /subscriptions/ b-ekkel \<subscriptionId\> kezdve.
ResourceGroupName – Az előfizetés alatt bármelyik erőforráscsoport neve.
c.
ResourceName, ResourceType, ResourceGroupName és (nem kötelező) ParentResource – Az előfizetés alatt egy adott erőforrást azonosít.

## PÉLDÁK

### 1. példa
```
PS C:\> Remove-AzRoleAssignment -ResourceGroupName rg1 -SignInName john.doe@contoso.com -RoleDefinitionName Reader
```

Eltávolít egy szerepkör-hozzárendelést az rg1 erőforráscsoport hatókörében az Olvasó john.doe@contoso.com szerepkörhöz hozzárendelt felhasználókhoz.

### 2. példa
```
PS C:\> Remove-AzRoleAssignment -ObjectId 36f81fc3-b00f-48cd-8218-3879f51ff39f -RoleDefinitionName Reader
```

Eltávolítja a szerepkör-hozzárendelést az ObjectId által azonosított csoporttaghoz, és hozzárendeli az Olvasó szerepkörhöz.
Alapértelmezés szerint az aktuális előfizetést használja hatókörként a törölni szükséges feladat megkereséhez.

### 3. példa
```
PS C:\> $roleassignment = Get-AzRoleAssignment |Select-Object -First 1 -Wait
PS C:\> Remove-AzRoleAssignment -InputObject $roleassignment
```

Eltávolítja az első szerepkör-hozzárendelési objektumot, amely lekért a Get-AzRoleAssignment parancsmagból.

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

### -InputObject
Szerepkör-hozzárendelés objektum.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
A felhasználó, csoport vagy szolgáltatásnév Azure AD-objektumazonosítója.

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ParentResource
A szülőerőforrás a hierarchiában (a ResourceName paraméterrel megadott erőforrásnál), ha van ilyen.
A ResourceGroupName, az ResourceType és az ResourceName paraméterrel együtt kell használni egy hierarchikus hatókör felépítéséhez egy relatív URI formájában, amely azonosítja az erőforrást.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Ha meg van adva, a törölt szerepkör-hozzárendelés megjelenítése

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Az erőforráscsoport neve, amelyhez a szerepkör hozzá van rendelve.
Megkísérel törölni egy hozzárendelést a megadott erőforráscsoport-hatókörben.
Ha a ResourceName, a ResourceType és a ParentResource paraméterrel együtt használja, a parancs hierarchikus hatókört épít fel egy erőforrást azonosító relatív URI-val.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Az erőforrás neve.
Például: storageaccountprod.
A ResourceGroupName, az ResourceType és (opcionálisan)ParentResource paraméterekkel együtt kell használni egy hierarchikus hatókör felépítéséhez egy relatív URI-ként, amely azonosítja az erőforrást, és törli az adott hatókörű hozzárendelést.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceType
Az erőforrás típusa.
Például: Microsoft.Network/virtualNetworks.
A ResourceGroupName, az ResourceName és a ParentResource paraméterekkel együtt kell használni egy hierarchikus hatókör felépítéséhez egy relatív URI-ként, amely azonosítja az erőforrást, és törli az adott erőforrás-hatókörben lévő hozzárendelést.

```yaml
Type: System.String
Parameter Sets: ResourceWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleDefinitionId
Annak az RBAC-szerepkörnek az azonosítója, amelynek a hozzárendelését törölni kell.

```yaml
Type: System.Guid
Parameter Sets: RoleIdWithScopeAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RoleDefinitionName
Annak az RBAC-szerepkörnek a neve, amelynek a hozzárendelését törölni kell, például olvasó, közreműködő, virtuális hálózat rendszergazdája stb.

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ResourceWithObjectIdParameterSet, ResourceGroupWithObjectIdParameterSet, ScopeWithObjectIdParameterSet, ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet, ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Scope
A törölt szerepkör-hozzárendelés hatóköre.
Relatív URI formátumban.
Például: "/subscriptions/9004a9fd-d58e-48dc-aeb2-4a4aec58606f/resourceGroups/TestRG".
Ha nincs megadva, előfizetési szinten kísérelje meg törölni a szerepkört.
Ha meg van adva, akkor a következővel kell kezdődni: "/subscriptions/{id}".

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet, ScopeWithObjectIdParameterSet, RoleIdWithScopeAndObjectIdParameterSet, ScopeWithSignInNameParameterSet, ScopeWithSPNParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Az Azure AD alkalmazás ServicePrincipalName tulajdonsága

```yaml
Type: System.String
Parameter Sets: ResourceWithSPNParameterSet, ResourceGroupWithSPNParameterSet, ScopeWithSPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SignInName
A felhasználó e-mail-címe vagy egyszerű felhasználóneve.

```yaml
Type: System.String
Parameter Sets: ResourceWithSignInNameParameterSet, ResourceGroupWithSignInNameParameterSet, ScopeWithSignInNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### System.String

### System.Guid

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment

## KIMENETEK

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment

## MEGJEGYZÉSEK
Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, vezető, erőforrás, csoport, sablon, telepítés

## KAPCSOLÓDÓ HIVATKOZÁSOK

[New-AzRoleAssignment](./New-AzRoleAssignment.md)

[Get-AzRoleAssignment](./Get-AzRoleAssignment.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

