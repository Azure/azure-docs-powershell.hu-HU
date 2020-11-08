---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 20e80617d47cd0a1f0ffb5cdb80d836656cd9abd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185306"
---
# Get-AzManagedHsmRoleAssignment

## Áttekintés
Felügyelt HSM szerepkör-hozzárendelések beszerzése vagy listázása A megfelelő paraméterekkel kilistázhatja a hozzárendeléseket egy adott felhasználó vagy szerepkör-definíció használatával.

## SZINTAXISA

### Lista (alapértelmezett)
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByName
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Leírás
A `Get-AzManagedHsmRoleAssignment` parancs segítségével listázhatja az összes olyan szerepkör-hozzárendelést, amely egy hatókörre érvényes.
Paraméterek nélkül a parancs az összes szerepkör-hozzárendelést visszaküldi a felügyelt HSM csoportba.
Ezt a listát a megbízó, a szerep és a hatókör szűrési paramétereinek használatával lehet szűrni.
A feladat tárgyát meg kell adni.
A felhasználók megadásához használja a SignInName vagy az Azure AD ObjectId paramétert.
Ha meg szeretne adni egy biztonsági csoportot, használja az Azure AD ObjectId paramétert.
Az Azure AD-alkalmazások megadásához használja a ApplicationId vagy a ObjectId paramétert.
A hozzárendelt szerepkört a RoleDefinitionName vagy a RoleDefinitionId paraméter használatával kell megadni.
Az Access által megadott hatókört meg lehet adni. Alapértelmezés szerint "/".

## Példák

### Példa 1
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

Ebben a példában a "myHsm" minden szerepkör-hozzárendelését felsorolja az összes hatókörben.

### 2. példa
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

Ebben a példában a "myHsm" "/Keys" tartomány összes szerepkör-hozzárendelését felsorolja, és a felhasználó bejelentkezési nevével szűri az eredményt.

## PARAMÉTEREK

### -ApplicationId
Az alkalmazás SPN-je.

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
Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.

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
A felhasználó vagy csoport objektum-azonosítója.

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
A szerepkör-hozzárendelés neve

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
Annak a szerepkörnek az azonosítója, amelyhez a megbízó hozzá van rendelve.

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
Annak a RBAC-szerepkörnek a neve, amelyhez a megbízót hozzá szeretné rendelni.

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

### -Scope (hatókör)
Az a hatókör, amelyen a szerepkör-hozzárendelés vagy-definíció érvényes, például "/" vagy "/Keys" vagy "/keys/{keyName}".
a "/" érték kihagyása esetén használatos.

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
Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.

## BEMENETEK

### Nincs

## KIMENETEK

### Microsoft. Azure. Command. PSKeyVaultRoleAssignment. models.

## MEGJEGYZI

## KAPCSOLÓDÓ HIVATKOZÁSOK
