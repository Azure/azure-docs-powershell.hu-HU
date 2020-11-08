---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 038049af40d84b678da12a57918328b3b0725127
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185288"
---
# <span data-ttu-id="71cf9-101">Remove-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="71cf9-101">Remove-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="71cf9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="71cf9-103">Eltávolítja a szerepkör-hozzárendelést a meghatározott megbízóhoz, aki egy bizonyos hatókörben meghatározott szerepkörhöz van rendelve.</span><span class="sxs-lookup"><span data-stu-id="71cf9-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="71cf9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71cf9-104">SYNTAX</span></span>

### <span data-ttu-id="71cf9-105">DefinitionNameSignInName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="71cf9-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71cf9-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="71cf9-106">DefinitionNameApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71cf9-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="71cf9-107">DefinitionNameObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71cf9-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="71cf9-108">DefinitionIdApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71cf9-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="71cf9-109">DefinitionIdObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71cf9-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="71cf9-110">DefinitionIdSignInName</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71cf9-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="71cf9-111">RemoveByNameParameterSet</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru]
 -RoleAssignmentName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71cf9-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="71cf9-112">InputObject</span></span>
```
Remove-AzManagedHsmRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71cf9-113">Leírás</span><span class="sxs-lookup"><span data-stu-id="71cf9-113">DESCRIPTION</span></span>
<span data-ttu-id="71cf9-114">A parancsmag használatával a `Remove-AzManagedHsmRoleAssignment` megadott hatókör és a megadott szerepkör szerint visszavonhatja a jogosultságokat.</span><span class="sxs-lookup"><span data-stu-id="71cf9-114">Use the `Remove-AzManagedHsmRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="71cf9-115">A feladat objektumát, azaz a megbízót meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="71cf9-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="71cf9-116">A megbízó lehet egy felhasználó (a SignInName vagy a ObjectId paraméterrel a felhasználó azonosítóját használhatja), a biztonsági csoportot (a ObjectId paramétert használva azonosíthat egy csoportot) vagy a szolgáltatót (a ApplicationId vagy ObjectId paraméterekkel azonosíthat egy ServicePrincipal.</span><span class="sxs-lookup"><span data-stu-id="71cf9-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="71cf9-117">A megbízó által hozzárendelt szerepkört a RoleDefinitionName vagy a RoleDefinitionId paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="71cf9-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="71cf9-118">Példák</span><span class="sxs-lookup"><span data-stu-id="71cf9-118">EXAMPLES</span></span>

### <span data-ttu-id="71cf9-119">Példa 1</span><span class="sxs-lookup"><span data-stu-id="71cf9-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="71cf9-120">Ez a példa visszavonja a "felügyelt HSM-házirend rendszergazdája" szerepkört a " user1@microsoft.com " at "/Keys" hatókörben.</span><span class="sxs-lookup"><span data-stu-id="71cf9-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="71cf9-121">2. példa</span><span class="sxs-lookup"><span data-stu-id="71cf9-121">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzManagedHsmRoleAssignment
```

<span data-ttu-id="71cf9-122">Ez a példa visszavonja a "minden szerepkörét" user1@microsoft.com minden hatókörben.</span><span class="sxs-lookup"><span data-stu-id="71cf9-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="71cf9-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71cf9-123">PARAMETERS</span></span>

### <span data-ttu-id="71cf9-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="71cf9-124">-ApplicationId</span></span>
<span data-ttu-id="71cf9-125">Az alkalmazás SPN-je.</span><span class="sxs-lookup"><span data-stu-id="71cf9-125">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameApplicationId, DefinitionIdApplicationId
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cf9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71cf9-126">-DefaultProfile</span></span>
<span data-ttu-id="71cf9-127">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71cf9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71cf9-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="71cf9-128">-HsmName</span></span>
<span data-ttu-id="71cf9-129">A HSM neve.</span><span class="sxs-lookup"><span data-stu-id="71cf9-129">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId, DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName, RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cf9-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71cf9-130">-InputObject</span></span>
<span data-ttu-id="71cf9-131">Szerepkör-hozzárendelési objektum</span><span class="sxs-lookup"><span data-stu-id="71cf9-131">Role assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71cf9-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="71cf9-132">-ObjectId</span></span>
<span data-ttu-id="71cf9-133">A felhasználó vagy csoport objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="71cf9-133">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameObjectId, DefinitionIdObjectId
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cf9-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71cf9-134">-PassThru</span></span>
<span data-ttu-id="71cf9-135">Igaz érték visszaadása a HSM visszaállításakor</span><span class="sxs-lookup"><span data-stu-id="71cf9-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="71cf9-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="71cf9-136">-RoleAssignmentName</span></span>
<span data-ttu-id="71cf9-137">A szerepkör-hozzárendelés neve</span><span class="sxs-lookup"><span data-stu-id="71cf9-137">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cf9-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="71cf9-138">-RoleDefinitionId</span></span>
<span data-ttu-id="71cf9-139">Annak a szerepkörnek az azonosítója, amelyhez a megbízó hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="71cf9-139">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cf9-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="71cf9-140">-RoleDefinitionName</span></span>
<span data-ttu-id="71cf9-141">Annak a RBAC-szerepkörnek a neve, amelyhez a megbízót hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="71cf9-141">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cf9-142">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="71cf9-142">-Scope</span></span>
<span data-ttu-id="71cf9-143">Az a hatókör, amelyen a szerepkör-hozzárendelés vagy-definíció érvényes, például "/" vagy "/Keys" vagy "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="71cf9-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="71cf9-144">a "/" érték kihagyása esetén használatos.</span><span class="sxs-lookup"><span data-stu-id="71cf9-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="71cf9-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="71cf9-145">-SignInName</span></span>
<span data-ttu-id="71cf9-146">A felhasználó SignInName.</span><span class="sxs-lookup"><span data-stu-id="71cf9-146">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionIdSignInName
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71cf9-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71cf9-147">-Confirm</span></span>
<span data-ttu-id="71cf9-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71cf9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71cf9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71cf9-149">-WhatIf</span></span>
<span data-ttu-id="71cf9-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71cf9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71cf9-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71cf9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71cf9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71cf9-152">CommonParameters</span></span>
<span data-ttu-id="71cf9-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71cf9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71cf9-154">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="71cf9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71cf9-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71cf9-155">INPUTS</span></span>

### <span data-ttu-id="71cf9-156">Microsoft. Azure. Command. PSKeyVaultRoleAssignment. models.</span><span class="sxs-lookup"><span data-stu-id="71cf9-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="71cf9-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71cf9-157">OUTPUTS</span></span>

### <span data-ttu-id="71cf9-158">Microsoft. Azure. Command. PSKeyVaultRoleAssignment. models.</span><span class="sxs-lookup"><span data-stu-id="71cf9-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="71cf9-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71cf9-159">NOTES</span></span>

## <span data-ttu-id="71cf9-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71cf9-160">RELATED LINKS</span></span>
