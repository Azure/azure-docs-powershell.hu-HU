---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: 741b182f6da1b9afc3433e5a79b3f174f239af23
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008629"
---
# <span data-ttu-id="edfff-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="edfff-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="edfff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edfff-102">SYNOPSIS</span></span>
<span data-ttu-id="edfff-103">Felügyeleti csoportot hoz létre</span><span class="sxs-lookup"><span data-stu-id="edfff-103">Creates a Management Group</span></span>

## <span data-ttu-id="edfff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="edfff-104">SYNTAX</span></span>

### <span data-ttu-id="edfff-105">GroupOperations (Alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="edfff-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edfff-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="edfff-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edfff-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="edfff-107">DESCRIPTION</span></span>
<span data-ttu-id="edfff-108">A **New-AzManagementGroup** parancsmag létrehoz egy felügyeleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="edfff-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="edfff-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="edfff-109">EXAMPLES</span></span>

### <span data-ttu-id="edfff-110">1. példa: Felügyeleti csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="edfff-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="edfff-111">Új csoport létrehozása a beállítással és a `DisplayName` `ParentId` `null` beállítással.</span><span class="sxs-lookup"><span data-stu-id="edfff-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="edfff-112">Ugyanaz lesz, mint a csoport szülője és szülője `DisplayName` `GroupName` lesz a bérlő.</span><span class="sxs-lookup"><span data-stu-id="edfff-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="edfff-113">2. példa: Felügyeleti csoport létrehozása megjelenítendő névvel</span><span class="sxs-lookup"><span data-stu-id="edfff-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="edfff-114">Ebben az esetben a csoport szülője lesz a bérlő, és a megadott értékre `DisplayName` lesz beállítva.</span><span class="sxs-lookup"><span data-stu-id="edfff-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="edfff-115">3. példa: Felügyeleti csoport létrehozása szülőnévvel és megjelenítendő névvel</span><span class="sxs-lookup"><span data-stu-id="edfff-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="edfff-116">4. példa: Felügyeleti csoport létrehozása szülőobjektummal (szülőobjektum használatával)</span><span class="sxs-lookup"><span data-stu-id="edfff-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

## <span data-ttu-id="edfff-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edfff-117">PARAMETERS</span></span>

### <span data-ttu-id="edfff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edfff-118">-DefaultProfile</span></span>
<span data-ttu-id="edfff-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="edfff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edfff-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="edfff-120">-DisplayName</span></span>
<span data-ttu-id="edfff-121">A felügyeleti csoport megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="edfff-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="edfff-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="edfff-122">-GroupName</span></span>
<span data-ttu-id="edfff-123">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="edfff-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfff-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="edfff-124">-ParentId</span></span>
<span data-ttu-id="edfff-125">A felügyeleti csoport szülőazonosítója</span><span class="sxs-lookup"><span data-stu-id="edfff-125">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfff-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="edfff-126">-ParentObject</span></span>
<span data-ttu-id="edfff-127">Szülőobjektum</span><span class="sxs-lookup"><span data-stu-id="edfff-127">Parent Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edfff-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edfff-128">-Confirm</span></span>
<span data-ttu-id="edfff-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="edfff-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edfff-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edfff-130">-WhatIf</span></span>
<span data-ttu-id="edfff-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="edfff-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edfff-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="edfff-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edfff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edfff-133">CommonParameters</span></span>
<span data-ttu-id="edfff-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edfff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edfff-135">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edfff-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edfff-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edfff-136">INPUTS</span></span>

### <span data-ttu-id="edfff-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="edfff-137">None</span></span>

## <span data-ttu-id="edfff-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="edfff-138">OUTPUTS</span></span>

### <span data-ttu-id="edfff-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="edfff-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="edfff-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="edfff-140">NOTES</span></span>

## <span data-ttu-id="edfff-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="edfff-141">RELATED LINKS</span></span>

[<span data-ttu-id="edfff-142">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="edfff-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="edfff-143">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="edfff-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="edfff-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="edfff-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)