---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: bdef58db8dcda735a7a8c08350b806c9fd00cf21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467205"
---
# <span data-ttu-id="22cc4-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="22cc4-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="22cc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="22cc4-103">Felügyeleti csoport frissítése</span><span class="sxs-lookup"><span data-stu-id="22cc4-103">Updates a Management Group</span></span>

## <span data-ttu-id="22cc4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22cc4-104">SYNTAX</span></span>

### <span data-ttu-id="22cc4-105">GroupOperations (Alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22cc4-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22cc4-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="22cc4-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22cc4-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="22cc4-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22cc4-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="22cc4-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22cc4-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22cc4-109">DESCRIPTION</span></span>
<span data-ttu-id="22cc4-110">Az **Update-AzManagementGroup** parancsmag frissíti egy felügyeleti csoport **ParentId** vagy **DisplayName** tulajdonságát.</span><span class="sxs-lookup"><span data-stu-id="22cc4-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="22cc4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22cc4-111">EXAMPLES</span></span>

### <span data-ttu-id="22cc4-112">1. példa: Felügyeleti csoport megjelenítendő nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="22cc4-112">Example 1: Update a Management Group's Display Name</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -DisplayName "New Display Name"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : New Display Name
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
```

### <span data-ttu-id="22cc4-113">2. példa: Felügyeleti csoport szülőcsoportja frissítése</span><span class="sxs-lookup"><span data-stu-id="22cc4-113">Example 2: Update a Management Group's Parent</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="22cc4-114">3. példa: Felügyeleti csoport frissítése a PSManagementGroup-objektum kivezetésével</span><span class="sxs-lookup"><span data-stu-id="22cc4-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Update-AzManagementGroup -DisplayName "TestDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestDisplayName
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="22cc4-115">4. példa: Felügyeleti csoport szülőcsoportja frissítése a ParentObject használatával</span><span class="sxs-lookup"><span data-stu-id="22cc4-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> Update-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="22cc4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22cc4-116">PARAMETERS</span></span>

### <span data-ttu-id="22cc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cc4-117">-DefaultProfile</span></span>
<span data-ttu-id="22cc4-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="22cc4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22cc4-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="22cc4-119">-DisplayName</span></span>
<span data-ttu-id="22cc4-120">A felügyeleti csoport megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="22cc4-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="22cc4-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="22cc4-121">-GroupName</span></span>
<span data-ttu-id="22cc4-122">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="22cc4-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22cc4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22cc4-123">-InputObject</span></span>
<span data-ttu-id="22cc4-124">Input Object from the Get call</span><span class="sxs-lookup"><span data-stu-id="22cc4-124">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22cc4-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="22cc4-125">-ParentId</span></span>
<span data-ttu-id="22cc4-126">A felügyeleti csoport szülőazonosítója</span><span class="sxs-lookup"><span data-stu-id="22cc4-126">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ManagementGroupObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22cc4-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="22cc4-127">-ParentObject</span></span>
<span data-ttu-id="22cc4-128">Input Object from the Get call</span><span class="sxs-lookup"><span data-stu-id="22cc4-128">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22cc4-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22cc4-129">-Confirm</span></span>
<span data-ttu-id="22cc4-130">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="22cc4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22cc4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22cc4-131">-WhatIf</span></span>
<span data-ttu-id="22cc4-132">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="22cc4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22cc4-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="22cc4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22cc4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cc4-134">CommonParameters</span></span>
<span data-ttu-id="22cc4-135">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22cc4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cc4-136">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22cc4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cc4-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22cc4-137">INPUTS</span></span>

### <span data-ttu-id="22cc4-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="22cc4-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="22cc4-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22cc4-139">OUTPUTS</span></span>

### <span data-ttu-id="22cc4-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="22cc4-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="22cc4-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22cc4-141">NOTES</span></span>

## <span data-ttu-id="22cc4-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22cc4-142">RELATED LINKS</span></span>
