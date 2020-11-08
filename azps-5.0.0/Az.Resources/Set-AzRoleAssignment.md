---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
ms.openlocfilehash: 9342ea2486c28a44ba7ff4a22f21619846ac7010
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195518"
---
# <span data-ttu-id="ad848-101">Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ad848-101">Set-AzRoleAssignment</span></span>

## <span data-ttu-id="ad848-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad848-102">SYNOPSIS</span></span>
<span data-ttu-id="ad848-103">Meglévő szerepkör-hozzárendelés frissítése</span><span class="sxs-lookup"><span data-stu-id="ad848-103">Update an existing Role Assignment.</span></span>

## <span data-ttu-id="ad848-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad848-104">SYNTAX</span></span>

### <span data-ttu-id="ad848-105">RoleAssignmentParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ad848-105">RoleAssignmentParameterSet (Default)</span></span>
```
Set-AzRoleAssignment -InputObject <PSRoleAssignment> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad848-106">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad848-106">InputFileParameterSet</span></span>
```
Set-AzRoleAssignment -InputFile <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad848-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad848-107">DESCRIPTION</span></span>
<span data-ttu-id="ad848-108">A meglévő hozzárendelések módosításához használja a New-AzRoleAssignment parancsot.</span><span class="sxs-lookup"><span data-stu-id="ad848-108">Use the New-AzRoleAssignment command to modify an existing assignment.</span></span>  
<span data-ttu-id="ad848-109">A leírások tetszőleges érvényes karakterláncok lehetnek, ezekkel a diferentiate egymástól.</span><span class="sxs-lookup"><span data-stu-id="ad848-109">Descriptions can be any valid string, use that to diferentiate from one another.</span></span>  
<span data-ttu-id="ad848-110">Ha a feltétel beállítása a feltétel, akkor a verziónak is be kell állítania, de ha olyan feltételt frissít, amely nem szükséges.</span><span class="sxs-lookup"><span data-stu-id="ad848-110">if Condition is set Condition Version has to be set as well but if you're updating a Condition that is not necesary.</span></span>
<span data-ttu-id="ad848-111">A feltétel verziója frissíthető a 1,0-ról 2,0-re, de nem visszaminősíthető.</span><span class="sxs-lookup"><span data-stu-id="ad848-111">Condition Version can be upgraded from 1.0 to 2.0 but it can't not be downgraded back.</span></span> <span data-ttu-id="ad848-112">Ügyeljen arra, hogy a 2,0 nem retrocompatible az 1,0-tel.</span><span class="sxs-lookup"><span data-stu-id="ad848-112">Be cautious as 2.0 is not retrocompatible with 1.0.</span></span>

## <span data-ttu-id="ad848-113">Példák</span><span class="sxs-lookup"><span data-stu-id="ad848-113">EXAMPLES</span></span>

### <span data-ttu-id="ad848-114">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad848-114">Example 1</span></span>
```powershell
$ConditionVersion = "2.0"
  $Description = "This is a new role assignment for John"
  $Condition = "@Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'"

  $roleAssignment = Get-AzRoleAssignment -Scope "/subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg" -PrincipalId "0c0f6cdc-90dd-4664-83c0-a0d986c4c604"
  $roleAssignment.Description = $Description
  $roleAssignment.Condition = $Condition
  $roleAssignment.ConditionVersion = $ConditionVersion

  Set-AzRoleAssignment -InputObject $roleAssignment -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="ad848-115">Meglévő szerepkör-hozzárendelés frissítése objektum módosításával</span><span class="sxs-lookup"><span data-stu-id="ad848-115">Update an existing role assignment by modifying an object</span></span>

### <span data-ttu-id="ad848-116">2. példa</span><span class="sxs-lookup"><span data-stu-id="ad848-116">Example 2</span></span>
```powershell
Set-AzRoleAssignment -InputFile "C:\RoleAssignments\example.json" -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="ad848-117">Meglévő szerepkör-hozzárendelés frissítése fájl használatával</span><span class="sxs-lookup"><span data-stu-id="ad848-117">Update an existing role assignment by using a file</span></span>

## <span data-ttu-id="ad848-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad848-118">PARAMETERS</span></span>

### <span data-ttu-id="ad848-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad848-119">-DefaultProfile</span></span>
<span data-ttu-id="ad848-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad848-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad848-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ad848-121">-InputFile</span></span>
<span data-ttu-id="ad848-122">Egyetlen szerepkör-definíciót tartalmazó fájlnév</span><span class="sxs-lookup"><span data-stu-id="ad848-122">File name containing a single role definition.</span></span>

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

### <span data-ttu-id="ad848-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad848-123">-InputObject</span></span>
<span data-ttu-id="ad848-124">Szerepkör-hozzárendelés</span><span class="sxs-lookup"><span data-stu-id="ad848-124">Role Assignment.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad848-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad848-125">-PassThru</span></span>
<span data-ttu-id="ad848-126">Ha meg van adva, a frissített szerepkör-hozzárendelést jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="ad848-126">If specified, displays the updated role assignment</span></span>

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

### <span data-ttu-id="ad848-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad848-127">-Confirm</span></span>
<span data-ttu-id="ad848-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad848-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad848-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad848-129">-WhatIf</span></span>
<span data-ttu-id="ad848-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad848-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad848-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad848-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad848-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad848-132">CommonParameters</span></span>
<span data-ttu-id="ad848-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad848-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad848-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ad848-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad848-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad848-135">INPUTS</span></span>

### <span data-ttu-id="ad848-136">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ad848-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="ad848-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad848-137">OUTPUTS</span></span>

### <span data-ttu-id="ad848-138">Microsoft. Azure. Command. Resources. modellek. Authorization. PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ad848-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="ad848-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad848-139">NOTES</span></span>

## <span data-ttu-id="ad848-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad848-140">RELATED LINKS</span></span>
