---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 7de4753d47ff2a285da6a9d3d60e0f95fcbf6e92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001461"
---
# Get-AzKeyVaultRoleAssignment

## SYNOPSIS
Felügyelt HSM szerepkör-hozzárendelések lekérte vagy listába sorolja azokat. A megfelelő paramétereket használva listába sorolja fel egy adott felhasználó hozzárendelését vagy egy szerepkördefiníciót.

## SZINTAXIS

### Lista (alapértelmezett)
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByName
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## LEÍRÁS
A paranccsal felsorolja az összes olyan szerepkör-hozzárendelést, `Get-AzKeyVaultRoleAssignment` amely hatókör szerint hatékony.
Paraméterek nélkül ez a parancs a felügyelt HSM alatt készült összes szerepkör-hozzárendelést visszaadja.
Ez a lista szűrhető a főnév, a szerepkör és a hatókör szűrési paramétereivel.
A feladat tárgyát meg kell adni.
Felhasználó megadásához használja a SignInName vagy az Azure AD ObjectId paramétereit.
Biztonsági csoport megadásához használja az Azure AD ObjectId paramétert.
Azure AD-alkalmazás megadásához használja az ApplicationId vagy az ObjectId paramétert.
A hozzárendelt szerepkört a RoleDefinitionName vagy a RoleDefinitionId paraméterrel kell megadni.
A hozzáférés hatóköre meg lehet adni. Alapértelmezés szerint a "/" értéket használja.

## PÉLDÁK

### 1. példa
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

Az alábbi példa a "myHsm" összes szerepkör-hozzárendelését felsorolja az összes hatókörben.

### 2. példa
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

Az alábbi példa felsorolja a "myHsm" szerepkör-hozzárendeléseket a "/keys" hatókörben, és a felhasználó bejelentkezési neve szerint szűri az eredményt.

## PARAMETERS

### -ApplicationId
Az alkalmazás SPN-ját.

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.

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

### -HsmName
A HSM neve.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
A felhasználó vagy csoport objektumazonosítója.

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleAssignmentName
A szerepkör-hozzárendelés neve.

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleDefinitionId
A főnévhez hozzárendelt szerepkör-azonosító.

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleDefinitionName
Annak az RBAC-szerepkörnek a neve, amelyhez a tőkenevet hozzá kell rendelni.

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
A szerepkör-hozzárendelés vagy -definíció hatóköre, például "/" vagy "/keys" vagy "/keys/{keyName}".
A "/" akkor használatos, ha nincs megadva.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SignInName
A felhasználó SignInName.

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Nincs

## KIMENETEK

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK
