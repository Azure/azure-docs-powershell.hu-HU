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
# <span data-ttu-id="0ebf5-101">Get-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0ebf5-101">Get-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="0ebf5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0ebf5-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebf5-103">Felügyelt HSM szerepkör-hozzárendelések beszerzése vagy listázása</span><span class="sxs-lookup"><span data-stu-id="0ebf5-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="0ebf5-104">A megfelelő paraméterekkel kilistázhatja a hozzárendeléseket egy adott felhasználó vagy szerepkör-definíció használatával.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="0ebf5-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0ebf5-105">SYNTAX</span></span>

### <span data-ttu-id="0ebf5-106">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0ebf5-106">List (Default)</span></span>
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ebf5-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="0ebf5-107">GetByName</span></span>
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ebf5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="0ebf5-108">DESCRIPTION</span></span>
<span data-ttu-id="0ebf5-109">A `Get-AzManagedHsmRoleAssignment` parancs segítségével listázhatja az összes olyan szerepkör-hozzárendelést, amely egy hatókörre érvényes.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-109">Use the `Get-AzManagedHsmRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="0ebf5-110">Paraméterek nélkül a parancs az összes szerepkör-hozzárendelést visszaküldi a felügyelt HSM csoportba.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="0ebf5-111">Ezt a listát a megbízó, a szerep és a hatókör szűrési paramétereinek használatával lehet szűrni.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="0ebf5-112">A feladat tárgyát meg kell adni.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="0ebf5-113">A felhasználók megadásához használja a SignInName vagy az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="0ebf5-114">Ha meg szeretne adni egy biztonsági csoportot, használja az Azure AD ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="0ebf5-115">Az Azure AD-alkalmazások megadásához használja a ApplicationId vagy a ObjectId paramétert.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="0ebf5-116">A hozzárendelt szerepkört a RoleDefinitionName vagy a RoleDefinitionId paraméter használatával kell megadni.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="0ebf5-117">Az Access által megadott hatókört meg lehet adni.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="0ebf5-118">Alapértelmezés szerint "/".</span><span class="sxs-lookup"><span data-stu-id="0ebf5-118">It defaults to "/".</span></span>

## <span data-ttu-id="0ebf5-119">Példák</span><span class="sxs-lookup"><span data-stu-id="0ebf5-119">EXAMPLES</span></span>

### <span data-ttu-id="0ebf5-120">Példa 1</span><span class="sxs-lookup"><span data-stu-id="0ebf5-120">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="0ebf5-121">Ebben a példában a "myHsm" minden szerepkör-hozzárendelését felsorolja az összes hatókörben.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="0ebf5-122">2. példa</span><span class="sxs-lookup"><span data-stu-id="0ebf5-122">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="0ebf5-123">Ebben a példában a "myHsm" "/Keys" tartomány összes szerepkör-hozzárendelését felsorolja, és a felhasználó bejelentkezési nevével szűri az eredményt.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="0ebf5-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0ebf5-124">PARAMETERS</span></span>

### <span data-ttu-id="0ebf5-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0ebf5-125">-ApplicationId</span></span>
<span data-ttu-id="0ebf5-126">Az alkalmazás SPN-je.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-126">The app SPN.</span></span>

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

### <span data-ttu-id="0ebf5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebf5-127">-DefaultProfile</span></span>
<span data-ttu-id="0ebf5-128">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ebf5-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0ebf5-129">-HsmName</span></span>
<span data-ttu-id="0ebf5-130">A HSM neve.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="0ebf5-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0ebf5-131">-ObjectId</span></span>
<span data-ttu-id="0ebf5-132">A felhasználó vagy csoport objektum-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-132">The user or group object id.</span></span>

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

### <span data-ttu-id="0ebf5-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0ebf5-133">-RoleAssignmentName</span></span>
<span data-ttu-id="0ebf5-134">A szerepkör-hozzárendelés neve</span><span class="sxs-lookup"><span data-stu-id="0ebf5-134">Name of the role assignment.</span></span>

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

### <span data-ttu-id="0ebf5-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0ebf5-135">-RoleDefinitionId</span></span>
<span data-ttu-id="0ebf5-136">Annak a szerepkörnek az azonosítója, amelyhez a megbízó hozzá van rendelve.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-136">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="0ebf5-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0ebf5-137">-RoleDefinitionName</span></span>
<span data-ttu-id="0ebf5-138">Annak a RBAC-szerepkörnek a neve, amelyhez a megbízót hozzá szeretné rendelni.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-138">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="0ebf5-139">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="0ebf5-139">-Scope</span></span>
<span data-ttu-id="0ebf5-140">Az a hatókör, amelyen a szerepkör-hozzárendelés vagy-definíció érvényes, például "/" vagy "/Keys" vagy "/keys/{keyName}".</span><span class="sxs-lookup"><span data-stu-id="0ebf5-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="0ebf5-141">a "/" érték kihagyása esetén használatos.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="0ebf5-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="0ebf5-142">-SignInName</span></span>
<span data-ttu-id="0ebf5-143">A felhasználó SignInName.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-143">The user SignInName.</span></span>

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

### <span data-ttu-id="0ebf5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebf5-144">CommonParameters</span></span>
<span data-ttu-id="0ebf5-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0ebf5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebf5-146">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebf5-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ebf5-147">INPUTS</span></span>

### <span data-ttu-id="0ebf5-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="0ebf5-148">None</span></span>

## <span data-ttu-id="0ebf5-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0ebf5-149">OUTPUTS</span></span>

### <span data-ttu-id="0ebf5-150">Microsoft. Azure. Command. PSKeyVaultRoleAssignment. models.</span><span class="sxs-lookup"><span data-stu-id="0ebf5-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="0ebf5-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0ebf5-151">NOTES</span></span>

## <span data-ttu-id="0ebf5-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0ebf5-152">RELATED LINKS</span></span>
