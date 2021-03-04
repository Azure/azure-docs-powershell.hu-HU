---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 77f6ac36f756e89859d38a0c608139dfe28c9667
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919906"
---
# Set-AzKeyVaultAccessPolicy

## SYNOPSIS
Megadja vagy módosítja egy felhasználó, alkalmazás vagy biztonsági csoport meglévő engedélyét, hogy műveleteket hajtson végre egy kulcstárban.

## SZINTAXIS

### ByUserPrincipalName (alapértelmezett)
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByObjectId
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByEmailAddress
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ForVault
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectByObjectId
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectByUserPrincipalName
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectByEmailAddress
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### InputObjectForVault
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByObjectId
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByServicePrincipalName
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdByUserPrincipalName
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdByEmailAddress
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdForVault
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## LEÍRÁS
A **Set-AzKeyVaultAccessPolicy** parancsmag megadja vagy módosítja egy felhasználó, alkalmazás vagy biztonsági csoport meglévő engedélyét, hogy végrehajtsa a megadott műveleteket egy kulcstárban. Nem módosítja azokat az engedélyeket, amelyek más felhasználók, alkalmazások vagy biztonsági csoportok számára a kulcstárban vannak.
Ha egy biztonsági csoport engedélyét ad meg, ez a művelet csak az adott biztonsági csoport felhasználóit érinti.
A következő címtáraknak mindnek azonos Azure-címtárnak kell lennie:
- Annak az Azure-előfizetésnek az alapértelmezett címtára, amelyben a kulcstár található.
- Az Azure-címtár, amely azt a felhasználót vagy alkalmazáscsoportot tartalmazza, amelyhez engedélyeket ad.
Példák olyan esetekre, amikor ezek a feltételek nem teljesülnek, és ez a parancsmag nem működik:
- Egy másik szervezetből származó felhasználónak a kulcstár kezeléséhez való hozzáférése.
Mindegyik szervezetnek saját címtára van.
- Azure-fiókja több könyvtárral rendelkezik.
Ha nem az alapértelmezett címtárban regisztrál egy alkalmazást, akkor nem engedélyezheti az alkalmazásnak a kulcstár használatát.
Az alkalmazásnak az alapértelmezett címtárban kell lennie.
Vegye figyelembe, hogy bár az erőforráscsoport megadása nem kötelező ehhez a parancsmaghoz, a jobb teljesítmény érdekében ezt kell megtennie.

> [!NOTE]
> Amikor egyszerű szolgáltatásnév használatával hozzáférési házirend-engedélyeket ad meg, a paramétert kell `-BypassObjectIdValidation` használnia.

## PÉLDÁK

### 1. példa: Engedélyek megadása egy felhasználónak egy kulcstárhoz és az engedélyek módosítása
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

Az első parancs engedélyeket ad egy felhasználónak az Azure Active Directoryban, hogy műveleteket hajtson végre a kulcsokon és a titkosságon PattiFuller@contoso.com a Contoso03Vault nevű kulcstárban. A *PassThru paraméter* eredménye a frissített objektum, amelyet a parancsmag ad vissza.
A második parancs módosítja az első parancsban megadott engedélyeket, így mostantól a beállításukon és törlésüken kívül lehetővé teszi a titkos adatok PattiFuller@contoso.com beszerzését. A kulcsműveletekkel kapcsolatos engedélyek a parancs után is változatlanok maradnak.
Az utolsó parancs tovább módosítja a kulcsműveletekkel kapcsolatos összes engedély eltávolításának meglévő PattiFuller@contoso.com engedélyét. A titkos műveletekre vonatkozó engedélyek a parancs után is változatlanok maradnak.

### 2. példa: Engedélyek megadása egyszerű alkalmazásszolgáltatásnak a titkos kulcsok olvasására és írására
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

Ez a parancs engedélyeket ad az alkalmazásokhoz a Contoso03Vault nevű kulcstárhoz.
A *ServicePrincipalName paraméter* megadja az alkalmazást. Az alkalmazásnak regisztrálva kell lennie az Azure Active Directoryban. A *ServicePrincipalName* paraméter értékének vagy az alkalmazás egyszerű szolgáltatásnevének vagy a GUID azonosítónak kell lennie.
Ebben a példában az egyszerű szolgáltatásnevet adhatja meg, és a parancs olvasási és írási engedélyeket ad az `http://payroll.contoso.com` alkalmazásnak.

### 3. példa: Engedélyek megadása egy alkalmazáshoz az objektumazonosító használatával
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

Ez a parancs hozzáférési engedélyt ad az alkalmazásnak a titkos kulcsok olvasására és írására.
Ebben a példában az alkalmazás az alkalmazás egyszerű szolgáltatásnévének objektumazonosítóját használja.

### 4. példa: Egyszerű felhasználónév engedélyeinek megadása
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

Ez a parancs hozzáférési, lista- és beállítási engedélyeket ad a megadott egyszerű felhasználónévnek a titkos információkhoz való hozzáféréshez.

### 5. példa: Annak engedélyezése, hogy a Microsoft.Compute erőforrásszolgáltató beolvassa a titkos adatokat egy kulcstárból
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

Ez a parancs megadja a Microsoft.Compute erőforrásszolgáltatója által a Contoso03Vault kulcstárból beolvasandó titkos információkhoz szükséges engedélyeket.

### 6. példa: Engedélyek megadása biztonsági csoportnak
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

Az első parancs a Get-AzADGroup parancsmagot használja az összes Active Directory-csoport be szerezni. A kimenetben 3 visszaadott csoport látható, a **csoport1,** **a csoport2** és a **csoport3.** Több csoportnak lehet ugyanaz a neve, de mindig egyedi ObjectId azonosítóval rendelkezik. Ha több, azonos nevű csoportot ad vissza, a kimenetben az ObjectId érték használatával azonosítsa a használni kívánt csoportot.
Ezután használhatja a parancs kimenetét a Set-AzKeyVaultAccessPolicy, hogy engedélyeket adjon a group2 kulcstárának **(myownvault) számára.** Az alábbi példa a "group2" nevű csoportokat számba veszi ugyanabban a parancssorban.
A visszaadott listában több "csoport2" nevű csoport is lehet.
Ebben a példában az elsőt választjuk ki, amelyet a 0 index jelez \[ a \] visszaadott listában.

### 7. példa: Azure Information Protection-hozzáférés megadása az ügyfél által kezelt bérlői kulcshoz (BYOK)
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

Ez a parancs engedélyezi az Azure Information Protectionnek, hogy az Azure Information Protection bérlői kulcsként ügyfél által kezelt kulcsot (a saját kulcsát hozza magával, vagy a "BYOK" esetet) használjon.
A parancs futtatásakor meg kell adnia a saját kulcstárnevét, de meg kell adnia a *ServicePrincipalName* paramétert a GUID **00000012-0000-0000-c000-00000000000000** azonosítóval, és meg kell adnia a példában az engedélyeket.

## PARAMETERS

### -ApplicationId
Későbbi használatra.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BypassObjectIdValidation
Lehetővé teszi az objektumazonosítók megadását anélkül, hogy érvényesíte volna az objektum Azure Active Directoryban való létezik-e.
Ezt a paramétert csak akkor használja, ha hozzáférést szeretne a kulcstárhoz egy olyan objektumazonosítóhoz, amely egy másik Azure-bérlő delegált biztonsági csoportjára hivatkozik.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -EmailAddress
Annak a felhasználónak az e-mail-címét adja meg, akinek engedélyt kell kiadó felhasználónak.
Ennek az e-mail-címnek az aktuális előfizetéshez társított címtárban kell lennie, és egyedinek kell lennie.

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForDeployment
Lehetővé teszi a Microsoft.Compute erőforrásszolgáltatónak, hogy beolvassa a titkos értékeket ebből a kulcstárból, amikor erre a kulcstárra hivatkozik az erőforrás-létrehozás során, például virtuális gép létrehozásakor.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForDiskEncryption
Lehetővé teszi az Azure lemeztitkosítási szolgáltatásának, hogy titkos adatokat és kulcsokat olvasson le ebből a kulcstárból.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForTemplateDeployment
Lehetővé teszi az Azure Resource Manager számára, hogy titkos titkos szolgáltatásokat rejtsen ebből a kulcstárból, amikor erre a kulcstárra hivatkozik egy sablon központi telepítésében.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Key Vault objektum

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
Annak a felhasználónak vagy szolgáltatásnévnek az objektumazonosítóját adja meg az Azure Active Directoryban, amelynek az engedélyét meg kell adni.

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.
Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.

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

### -PermissionsToCertificates
Egy felhasználónak vagy egyszerű szolgáltatásnak adható tanúsítványengedélyek tömbje.
A paraméter elfogadható értékei:
- Mind
- Bej.le
- Lista
- Törlés
- Létrehozás
- Importálás
- Frissítés
- Managecontacts
- Getissuers
- Listissuers
- Setissuers
- Deleteissuers
- Manageissuers
- Helyreállítás
- Biztonsági másolat
- Visszaállítás
- Végleges végleges végleges

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToKeys
Egy felhasználónak vagy egyszerű szolgáltatásnak adható kulcsműveleti engedélyek tömbje.
A paraméter elfogadható értékei:
- Mind
- Visszafejtése
- Titkosítás
- UnwrapKey
- WrapKey
- Ellenőrzés
- Aláírás
- Bej.le
- Lista
- Frissítés
- Létrehozás
- Importálás
- Törlés
- Biztonsági másolat
- Visszaállítás
- Helyreállítás
- Végleges végleges végleges

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToSecrets
Egy felhasználónak vagy egyszerű szolgáltatásnak adható titkos műveletekre vonatkozó engedélyek tömbje.
A paraméter elfogadható értékei:
- Mind
- Bej.le
- Lista
- Beállítás
- Törlés
- Biztonsági másolat
- Visszaállítás
- Helyreállítás
- Végleges végleges végleges

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionsToStorage
A felügyelt tárfiókra és a SaS-definíciós műveletre vonatkozó engedélyeket adja meg, amelyek a felhasználónak vagy a szolgáltatásnévnek adhatók.
A paraméter elfogadható értékei:
- mind
- get
- lista
- törlés
- beállítás
- frissítés
- regeneratekey
- getsas
- listsas
- deletesas
- setsas
- helyreállítás
- biztonsági mentés
- visszaállítás
- végleges végleges végleges

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Egy erőforráscsoport nevét adja meg.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Key Vault Resource Id

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Annak az alkalmazásnak a egyszerű szolgáltatásnevét adja meg, amelyhez engedélyeket ad.
Adja meg az alkalmazáshoz az AzureActive Directoryban regisztrált alkalmazásazonosítót ( más néven ügyfélazonosítót). A paraméterként megadott egyszerű szolgáltatásnévvel megadott alkalmazást az aktuális előfizetést tartalmazó Azure-címtárban kell regisztrálni.

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserPrincipalName
Annak a felhasználónak a felhasználó egyszerű felhasználónevét adja meg, akinek az engedélyeket ki kell ad.
Az egyszerű felhasználónévnek az aktuális előfizetéshez társított címtárban kell lennie.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Egy kulcstár nevét adja meg.
Ez a parancsmag módosítja a paraméter által megadott kulcstár hozzáférési házirendét.

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
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
Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable. További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INPUTS

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem

### System.String

## KIMENETEK

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

## MEGJEGYZÉSEK

## KAPCSOLÓDÓ HIVATKOZÁSOK

[Get-AzKeyVault](./Get-AzKeyVault.md)

[Remove-AzKeyVaultAccessPolicy](./Remove-AzKeyVaultAccessPolicy.md)

