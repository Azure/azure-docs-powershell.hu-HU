---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 9e2dd07ac0346cacb99bbcc2e05d47b57ac8ccd6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476973"
---
# <span data-ttu-id="e2819-101">Remove-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e2819-101">Remove-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="e2819-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2819-102">SYNOPSIS</span></span>
<span data-ttu-id="e2819-103">Eltávolít egy szerepkör-hozzárendelést a megadott egyszerű felhasználóhoz, aki egy adott szerepkörhöz van hozzárendelve egy adott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="e2819-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="e2819-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e2819-104">SYNTAX</span></span>

### <span data-ttu-id="e2819-105">DefinitionNameSignInName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e2819-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2819-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="e2819-106">DefinitionNameApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2819-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="e2819-107">DefinitionNameObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2819-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="e2819-108">DefinitionIdApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2819-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="e2819-109">DefinitionIdObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2819-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="e2819-110">DefinitionIdSignInName</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2819-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2819-111">RemoveByNameParameterSet</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2819-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="e2819-112">InputObject</span></span>
```
Remove-AzKeyVaultRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2819-113">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e2819-113">DESCRIPTION</span></span>
<span data-ttu-id="e2819-114">A parancsmag használatával visszavonhatja a hozzáférést egy adott hatókörű és `Remove-AzKeyVaultRoleAssignment` szerepkörű egyszerű felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="e2819-114">Use the `Remove-AzKeyVaultRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="e2819-115">A feladat objektuma, vagyis a főnévnek meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="e2819-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="e2819-116">A főnév lehet egy felhasználó (a SignInName vagy az ObjectId paraméter használatával azonosíthat egy felhasználót), biztonsági csoport (az ObjectId paraméter használata egy csoport azonosításához) vagy egyszerű szolgáltatásnév (Az ApplicationId vagy az ObjectId paramétereit használva azonosíthatja a ServicePrincipal értékeket.</span><span class="sxs-lookup"><span data-stu-id="e2819-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="e2819-117">A SzerepkörDefinitionName vagy a RoleDefinitionId paraméterrel meg kell adni azt a szerepkört, amelyhez a fő tag hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="e2819-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="e2819-118">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e2819-118">EXAMPLES</span></span>

### <span data-ttu-id="e2819-119">1. példa</span><span class="sxs-lookup"><span data-stu-id="e2819-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="e2819-120">Ez a példa visszavonja a "Felügyelt HSM-házirend-rendszergazda" "at user1@microsoft.com "/keys" hatókörű szerepkört.</span><span class="sxs-lookup"><span data-stu-id="e2819-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="e2819-121">2. példa</span><span class="sxs-lookup"><span data-stu-id="e2819-121">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzKeyVaultRoleAssignment
```

<span data-ttu-id="e2819-122">Ez a példa az " " összes szerepkörét user1@microsoft.com minden hatókörben visszavonja.</span><span class="sxs-lookup"><span data-stu-id="e2819-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="e2819-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2819-123">PARAMETERS</span></span>

### <span data-ttu-id="e2819-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e2819-124">-ApplicationId</span></span>
<span data-ttu-id="e2819-125">Az alkalmazás SPN-ját.</span><span class="sxs-lookup"><span data-stu-id="e2819-125">The app SPN.</span></span>

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

### <span data-ttu-id="e2819-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2819-126">-DefaultProfile</span></span>
<span data-ttu-id="e2819-127">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2819-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2819-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="e2819-128">-HsmName</span></span>
<span data-ttu-id="e2819-129">A HSM neve.</span><span class="sxs-lookup"><span data-stu-id="e2819-129">Name of the HSM.</span></span>

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

### <span data-ttu-id="e2819-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e2819-130">-InputObject</span></span>
<span data-ttu-id="e2819-131">Szerepkör-hozzárendelési objektum.</span><span class="sxs-lookup"><span data-stu-id="e2819-131">Role assignment object.</span></span>

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

### <span data-ttu-id="e2819-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e2819-132">-ObjectId</span></span>
<span data-ttu-id="e2819-133">A felhasználó vagy csoport objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="e2819-133">The user or group object id.</span></span>

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

### <span data-ttu-id="e2819-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2819-134">-PassThru</span></span>
<span data-ttu-id="e2819-135">A HSM visszaállításakor a visszatérési érték igaz.</span><span class="sxs-lookup"><span data-stu-id="e2819-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="e2819-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="e2819-136">-RoleAssignmentName</span></span>
<span data-ttu-id="e2819-137">A szerepkör-hozzárendelés neve.</span><span class="sxs-lookup"><span data-stu-id="e2819-137">Name of the role assignment.</span></span>

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

### <span data-ttu-id="e2819-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e2819-138">-RoleDefinitionId</span></span>
<span data-ttu-id="e2819-139">A főnévhez hozzárendelt szerepkör-azonosító.</span><span class="sxs-lookup"><span data-stu-id="e2819-139">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="e2819-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e2819-140">-RoleDefinitionName</span></span>
<span data-ttu-id="e2819-141">Annak az RBAC-szerepkörnek a neve, amelyhez a tőkenevet hozzá kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="e2819-141">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="e2819-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="e2819-142">-Scope</span></span>
<span data-ttu-id="e2819-143">Annak a hatókörnek a hatóköre, amelyre a szerepkör-hozzárendelés vagy -definíció vonatkozik, például "/" vagy "/keys" vagy "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="e2819-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="e2819-144">A "/" akkor használatos, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="e2819-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="e2819-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="e2819-145">-SignInName</span></span>
<span data-ttu-id="e2819-146">A felhasználó SignInName.</span><span class="sxs-lookup"><span data-stu-id="e2819-146">The user SignInName.</span></span>

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

### <span data-ttu-id="e2819-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e2819-147">-Confirm</span></span>
<span data-ttu-id="e2819-148">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e2819-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2819-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2819-149">-WhatIf</span></span>
<span data-ttu-id="e2819-150">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e2819-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2819-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e2819-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2819-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2819-152">CommonParameters</span></span>
<span data-ttu-id="e2819-153">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2819-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2819-154">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2819-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2819-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e2819-155">INPUTS</span></span>

### <span data-ttu-id="e2819-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e2819-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="e2819-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2819-157">OUTPUTS</span></span>

### <span data-ttu-id="e2819-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e2819-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="e2819-159">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e2819-159">NOTES</span></span>

## <span data-ttu-id="e2819-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2819-160">RELATED LINKS</span></span>
