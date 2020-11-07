---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: e63171f3d4497bf558a4349ff013726e24b079f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838921"
---
# <span data-ttu-id="baf8c-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="baf8c-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="baf8c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="baf8c-102">SYNOPSIS</span></span>
<span data-ttu-id="baf8c-103">Felügyeleti csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="baf8c-103">Creates a Management Group</span></span>

## <span data-ttu-id="baf8c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="baf8c-104">SYNTAX</span></span>

### <span data-ttu-id="baf8c-105">GroupOperations (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="baf8c-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baf8c-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="baf8c-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baf8c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="baf8c-107">DESCRIPTION</span></span>
<span data-ttu-id="baf8c-108">A **New-AzManagementGroup** parancsmag létrehoz egy felügyeleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="baf8c-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="baf8c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="baf8c-109">EXAMPLES</span></span>

### <span data-ttu-id="baf8c-110">Példa 1: felügyeleti csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="baf8c-110">Example 1: Create a Management Group</span></span>
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

<span data-ttu-id="baf8c-111">Új csoport létrehozása `DisplayName` és `ParentId` beállítása `null`</span><span class="sxs-lookup"><span data-stu-id="baf8c-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="baf8c-112">Az `DisplayName` ugyanaz lesz, mint a `GroupName` csoport anyavállalata lesz a bérlő.</span><span class="sxs-lookup"><span data-stu-id="baf8c-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="baf8c-113">2. példa: felügyeleti csoport létrehozása megjelenítendő névvel</span><span class="sxs-lookup"><span data-stu-id="baf8c-113">Example 2: Create a Management Group with a display name</span></span>
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

<span data-ttu-id="baf8c-114">Ebben az esetben a csoport szülője lesz a bérlő, és a `DisplayName` megjelenő érték az adott értékre lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="baf8c-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="baf8c-115">3. példa: felügyeleti csoport létrehozása szülővel és megjelenített névvel</span><span class="sxs-lookup"><span data-stu-id="baf8c-115">Example 3: Create a Management Group with a parent and a display name</span></span>
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

### <span data-ttu-id="baf8c-116">4. példa: felügyeleti csoport létrehozása szülővel (szülő objektum használatával)</span><span class="sxs-lookup"><span data-stu-id="baf8c-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
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

## <span data-ttu-id="baf8c-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="baf8c-117">PARAMETERS</span></span>

### <span data-ttu-id="baf8c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf8c-118">-DefaultProfile</span></span>
<span data-ttu-id="baf8c-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="baf8c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baf8c-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="baf8c-120">-DisplayName</span></span>
<span data-ttu-id="baf8c-121">A felügyeleti csoport megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="baf8c-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="baf8c-122">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="baf8c-122">-GroupName</span></span>
<span data-ttu-id="baf8c-123">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="baf8c-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf8c-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="baf8c-124">-ParentId</span></span>
<span data-ttu-id="baf8c-125">A felügyeleti csoport fölérendelt azonosítója</span><span class="sxs-lookup"><span data-stu-id="baf8c-125">Parent Id of the management group</span></span>

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

### <span data-ttu-id="baf8c-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="baf8c-126">-ParentObject</span></span>
<span data-ttu-id="baf8c-127">Fölérendelt objektum</span><span class="sxs-lookup"><span data-stu-id="baf8c-127">Parent Object</span></span>

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

### <span data-ttu-id="baf8c-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="baf8c-128">-Confirm</span></span>
<span data-ttu-id="baf8c-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="baf8c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baf8c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baf8c-130">-WhatIf</span></span>
<span data-ttu-id="baf8c-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="baf8c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="baf8c-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="baf8c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baf8c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf8c-133">CommonParameters</span></span>
<span data-ttu-id="baf8c-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="baf8c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf8c-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baf8c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf8c-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="baf8c-136">INPUTS</span></span>

### <span data-ttu-id="baf8c-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="baf8c-137">None</span></span>

## <span data-ttu-id="baf8c-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="baf8c-138">OUTPUTS</span></span>

### <span data-ttu-id="baf8c-139">Microsoft. Azure. Command. Resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="baf8c-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="baf8c-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="baf8c-140">NOTES</span></span>

## <span data-ttu-id="baf8c-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="baf8c-141">RELATED LINKS</span></span>

[<span data-ttu-id="baf8c-142">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="baf8c-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="baf8c-143">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="baf8c-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="baf8c-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="baf8c-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)