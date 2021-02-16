---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: c610339bf90069f30d6107d46fc92fd896d6816c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155402"
---
# <span data-ttu-id="a3405-101">Get-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a3405-101">Get-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="a3405-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3405-102">SYNOPSIS</span></span>
<span data-ttu-id="a3405-103">Felügyelt HSM szerepkör-hozzárendelések lekérte vagy listába sorolja azokat.</span><span class="sxs-lookup"><span data-stu-id="a3405-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="a3405-104">A megfelelő paramétereket használva listába sorolja fel egy adott felhasználó hozzárendelését vagy egy szerepkördefiníciót.</span><span class="sxs-lookup"><span data-stu-id="a3405-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="a3405-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a3405-105">SYNTAX</span></span>

### <span data-ttu-id="a3405-106">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a3405-106">List (Default)</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3405-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="a3405-107">GetByName</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3405-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a3405-108">DESCRIPTION</span></span>
<span data-ttu-id="a3405-109">A paranccsal felsorolja az összes olyan szerepkör-hozzárendelést, `Get-AzKeyVaultRoleAssignment` amely hatókör szerint hatékony.</span><span class="sxs-lookup"><span data-stu-id="a3405-109">Use the `Get-AzKeyVaultRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="a3405-110">Paraméterek nélkül ez a parancs a felügyelt HSM alatt készült összes szerepkör-hozzárendelést visszaadja.</span><span class="sxs-lookup"><span data-stu-id="a3405-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="a3405-111">Ez a lista szűrhető a főnév, a szerepkör és a hatókör szűrési paramétereivel.</span><span class="sxs-lookup"><span data-stu-id="a3405-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="a3405-112">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="a3405-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="a3405-113">Felhasználó megadásához használja a SignInName vagy az Azure AD ObjectId paramétereit.</span><span class="sxs-lookup"><span data-stu-id="a3405-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="a3405-114">Biztonsági csoport megadásához használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="a3405-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="a3405-115">Azure AD-alkalmazás megadásához használja az ApplicationId vagy az ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="a3405-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="a3405-116">A hozzárendelt szerepkört a RoleDefinitionName vagy a RoleDefinitionId paraméterrel kell megadni.</span><span class="sxs-lookup"><span data-stu-id="a3405-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="a3405-117">A hozzáférés hatóköre meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="a3405-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="a3405-118">Alapértelmezés szerint a "/" értéket használja.</span><span class="sxs-lookup"><span data-stu-id="a3405-118">It defaults to "/".</span></span>

## <span data-ttu-id="a3405-119">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a3405-119">EXAMPLES</span></span>

### <span data-ttu-id="a3405-120">1. példa</span><span class="sxs-lookup"><span data-stu-id="a3405-120">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="a3405-121">Ez a példa felsorolja a "myHsm" szerepkör-hozzárendeléseket az összes hatókörben.</span><span class="sxs-lookup"><span data-stu-id="a3405-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="a3405-122">2. példa</span><span class="sxs-lookup"><span data-stu-id="a3405-122">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="a3405-123">Ez a példa felsorolja a "myHsm" szerepkör-hozzárendeléseket a "/keys" hatókörben, és a felhasználó bejelentkezési neve szerint szűri az eredményt.</span><span class="sxs-lookup"><span data-stu-id="a3405-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="a3405-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3405-124">PARAMETERS</span></span>

### <span data-ttu-id="a3405-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a3405-125">-ApplicationId</span></span>
<span data-ttu-id="a3405-126">Az alkalmazás SPN-ét.</span><span class="sxs-lookup"><span data-stu-id="a3405-126">The app SPN.</span></span>

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

### <span data-ttu-id="a3405-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3405-127">-DefaultProfile</span></span>
<span data-ttu-id="a3405-128">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a3405-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3405-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="a3405-129">-HsmName</span></span>
<span data-ttu-id="a3405-130">A HSM neve.</span><span class="sxs-lookup"><span data-stu-id="a3405-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="a3405-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a3405-131">-ObjectId</span></span>
<span data-ttu-id="a3405-132">A felhasználó vagy csoport objektumazonosítója.</span><span class="sxs-lookup"><span data-stu-id="a3405-132">The user or group object id.</span></span>

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

### <span data-ttu-id="a3405-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="a3405-133">-RoleAssignmentName</span></span>
<span data-ttu-id="a3405-134">A szerepkör-hozzárendelés neve.</span><span class="sxs-lookup"><span data-stu-id="a3405-134">Name of the role assignment.</span></span>

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

### <span data-ttu-id="a3405-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a3405-135">-RoleDefinitionId</span></span>
<span data-ttu-id="a3405-136">Szerepkörazonosító, amelyhez a tőkenév hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="a3405-136">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="a3405-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a3405-137">-RoleDefinitionName</span></span>
<span data-ttu-id="a3405-138">Annak az RBAC-szerepkörnek a neve, amelyhez a tőkenevet hozzá kell rendelni.</span><span class="sxs-lookup"><span data-stu-id="a3405-138">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="a3405-139">-Scope</span><span class="sxs-lookup"><span data-stu-id="a3405-139">-Scope</span></span>
<span data-ttu-id="a3405-140">Annak a hatókörnek a hatóköre, amelyre a szerepkör-hozzárendelés vagy -definíció vonatkozik, például "/" vagy "/keys" vagy "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="a3405-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="a3405-141">A "/" akkor használatos, ha nincs megadva.</span><span class="sxs-lookup"><span data-stu-id="a3405-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="a3405-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="a3405-142">-SignInName</span></span>
<span data-ttu-id="a3405-143">A felhasználó SignInName.</span><span class="sxs-lookup"><span data-stu-id="a3405-143">The user SignInName.</span></span>

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

### <span data-ttu-id="a3405-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3405-144">CommonParameters</span></span>
<span data-ttu-id="a3405-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3405-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3405-146">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3405-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3405-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3405-147">INPUTS</span></span>

### <span data-ttu-id="a3405-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="a3405-148">None</span></span>

## <span data-ttu-id="a3405-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a3405-149">OUTPUTS</span></span>

### <span data-ttu-id="a3405-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a3405-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="a3405-151">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a3405-151">NOTES</span></span>

## <span data-ttu-id="a3405-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a3405-152">RELATED LINKS</span></span>
