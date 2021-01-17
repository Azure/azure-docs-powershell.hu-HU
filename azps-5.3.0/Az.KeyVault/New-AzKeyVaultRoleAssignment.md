---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: ee90ab1b4ba22f1a5c40427f7fc435c75cef992d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98465963"
---
# <span data-ttu-id="0ee4e-101">New-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0ee4e-101">New-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="0ee4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ee4e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ee4e-103">Hozzárendeli a megadott rbac szerepkört a megadott egyszerű felhasználóhoz a megadott hatókörben.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="0ee4e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0ee4e-104">SYNTAX</span></span>

### <span data-ttu-id="0ee4e-105">DefinitionNameSignInName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ee4e-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ee4e-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="0ee4e-106">DefinitionNameApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ee4e-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="0ee4e-107">DefinitionNameObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ee4e-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="0ee4e-108">DefinitionIdApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ee4e-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="0ee4e-109">DefinitionIdObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ee4e-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="0ee4e-110">DefinitionIdSignInName</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ee4e-111">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0ee4e-111">DESCRIPTION</span></span>
<span data-ttu-id="0ee4e-112">Hozzáférés `New-AzKeyVaultRoleAssignment` megadása a paranccsal.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-112">Use the `New-AzKeyVaultRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="0ee4e-113">Az Access úgy adható meg, hogy a megfelelő RBAC-szerepkört rendeli hozzájuk a megfelelő hatókörben.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="0ee4e-114">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="0ee4e-115">Felhasználó megadásához használja a SignInName vagy az Azure AD ObjectId paramétereit.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="0ee4e-116">Biztonsági csoport megadásához használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="0ee4e-117">Azure AD-alkalmazás megadásához használja az ApplicationId vagy az ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="0ee4e-118">A hozzárendelt szerepkört a RoleDefinitionName pr RoleDefinitionId paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="0ee4e-119">A hozzáférés hatóköre meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="0ee4e-120">Alapértelmezés szerint a kijelölt előfizetést használja.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="0ee4e-121">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0ee4e-121">EXAMPLES</span></span>

### <span data-ttu-id="0ee4e-122">1. példa</span><span class="sxs-lookup"><span data-stu-id="0ee4e-122">Example 1</span></span>
```powershell
PS C:\> New-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="0ee4e-123">Ebben a példában felső hatókörben a "Felügyelt HSM-házirend-rendszergazda" szerepkört user1@microsoft.com rendeli hozzá a "" felhasználóhoz.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="0ee4e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ee4e-124">PARAMETERS</span></span>

### <span data-ttu-id="0ee4e-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0ee4e-125">-ApplicationId</span></span>
<span data-ttu-id="0ee4e-126">Az alkalmazás SPN-ját.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-126">The app SPN.</span></span>

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

### <span data-ttu-id="0ee4e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ee4e-127">-DefaultProfile</span></span>
<span data-ttu-id="0ee4e-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ee4e-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0ee4e-129">-HsmName</span></span>
<span data-ttu-id="0ee4e-130">A HSM neve.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="0ee4e-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0ee4e-131">-ObjectId</span></span>
<span data-ttu-id="0ee4e-132">A felhasználó vagy csoport objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-132">The user or group object id.</span></span>

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

### <span data-ttu-id="0ee4e-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0ee4e-133">-RoleDefinitionId</span></span>
<span data-ttu-id="0ee4e-134">A főnévhez hozzárendelt szerepkör-azonosító.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="0ee4e-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0ee4e-135">-RoleDefinitionName</span></span>
<span data-ttu-id="0ee4e-136">Annak az RBAC-szerepkörnek a neve, amelyhez a tőkenevet hozzá kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="0ee4e-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="0ee4e-137">-Scope</span></span>
<span data-ttu-id="0ee4e-138">Annak a hatókörnek a hatóköre, amelyre a szerepkör-hozzárendelés vagy -definíció vonatkozik, például "/" vagy "/keys" vagy "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="0ee4e-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="0ee4e-139">A "/" akkor használatos, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="0ee4e-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="0ee4e-140">-SignInName</span></span>
<span data-ttu-id="0ee4e-141">A felhasználó SignInName.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-141">The user SignInName.</span></span>

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

### <span data-ttu-id="0ee4e-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ee4e-142">-Confirm</span></span>
<span data-ttu-id="0ee4e-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ee4e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ee4e-144">-WhatIf</span></span>
<span data-ttu-id="0ee4e-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ee4e-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ee4e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ee4e-147">CommonParameters</span></span>
<span data-ttu-id="0ee4e-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ee4e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ee4e-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ee4e-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ee4e-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ee4e-150">INPUTS</span></span>

### <span data-ttu-id="0ee4e-151">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ee4e-151">None</span></span>

## <span data-ttu-id="0ee4e-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ee4e-152">OUTPUTS</span></span>

### <span data-ttu-id="0ee4e-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0ee4e-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="0ee4e-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0ee4e-154">NOTES</span></span>

## <span data-ttu-id="0ee4e-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ee4e-155">RELATED LINKS</span></span>
