---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: f21a6d641e06916ce70c71338b539ef0909db6de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146050"
---
# <span data-ttu-id="9eadb-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9eadb-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="9eadb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eadb-102">SYNOPSIS</span></span>
<span data-ttu-id="9eadb-103">Felügyeleti csoport(ak) lekérte</span><span class="sxs-lookup"><span data-stu-id="9eadb-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="9eadb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9eadb-104">SYNTAX</span></span>

### <span data-ttu-id="9eadb-105">ListOperation (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9eadb-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eadb-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="9eadb-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eadb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9eadb-107">DESCRIPTION</span></span>
<span data-ttu-id="9eadb-108">A Get-AzManagementGroup parancsmag az összeset vagy egy adott felügyeleti csoportot kap.</span><span class="sxs-lookup"><span data-stu-id="9eadb-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="9eadb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9eadb-109">EXAMPLES</span></span>

### <span data-ttu-id="9eadb-110">1. példa: Az összes felügyeleti csoport lekérte</span><span class="sxs-lookup"><span data-stu-id="9eadb-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzManagementGroup

Id          : /providers/Microsoft.Management/managementGroups/TestGroup
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroup
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupDisplayName

Id          : /providers/Microsoft.Management/managementGroups/TestGroupChild
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroupChild
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupChildDisplayName
```

### <span data-ttu-id="9eadb-111">2. példa: Adott felügyeleti csoport lekérte</span><span class="sxs-lookup"><span data-stu-id="9eadb-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName TestGroup

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="9eadb-112">3. példa: Adott felügyeleti csoport és a hierarchia első szintje</span><span class="sxs-lookup"><span data-stu-id="9eadb-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzManagementGroup -GroupName TestGroupParent -Expand
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    :
```

<span data-ttu-id="9eadb-113">A jelölővel navigálhat a tömbben, és `Expand` `Children` lekérte az egyes gyermekek adatait.</span><span class="sxs-lookup"><span data-stu-id="9eadb-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="9eadb-114">Megadhatja például a megjelenítendő nevet tartalmazó `Children[0]` csoport `TestGroup1DisplayName` adatait.</span><span class="sxs-lookup"><span data-stu-id="9eadb-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="9eadb-115">4. példa: Adott felügyeleti csoport és a hierarchia minden szintje</span><span class="sxs-lookup"><span data-stu-id="9eadb-115">Example 4: Get specific Management Group and all levels of hierarchy</span></span>
```
PS C:\> $response = Get-AzManagementGroup -GroupName TestGroupParent -Expand -Recurse
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    : {TestRecurseChild}

PS C:\> $response.Children[0].Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestRecurseChild
Name        : TestRecurseChild
DisplayName : TestRecurseChild
Children    :
```

## <span data-ttu-id="9eadb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eadb-116">PARAMETERS</span></span>

### <span data-ttu-id="9eadb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eadb-117">-DefaultProfile</span></span>
<span data-ttu-id="9eadb-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9eadb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eadb-119">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="9eadb-119">-Expand</span></span>
<span data-ttu-id="9eadb-120">Bontsa ki a kimenetet a felügyeleti csoport gyermekeinek listájához</span><span class="sxs-lookup"><span data-stu-id="9eadb-120">Expand the output to list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eadb-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="9eadb-121">-GroupName</span></span>
<span data-ttu-id="9eadb-122">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="9eadb-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eadb-123">-Recurse</span><span class="sxs-lookup"><span data-stu-id="9eadb-123">-Recurse</span></span>
<span data-ttu-id="9eadb-124">A felügyeleti csoport gyermekeinek rekurzív listája</span><span class="sxs-lookup"><span data-stu-id="9eadb-124">Recursively list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eadb-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9eadb-125">-Confirm</span></span>
<span data-ttu-id="9eadb-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="9eadb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eadb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eadb-127">-WhatIf</span></span>
<span data-ttu-id="9eadb-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="9eadb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eadb-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9eadb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eadb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eadb-130">CommonParameters</span></span>
<span data-ttu-id="9eadb-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eadb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eadb-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9eadb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eadb-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9eadb-133">INPUTS</span></span>

### <span data-ttu-id="9eadb-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="9eadb-134">None</span></span>

## <span data-ttu-id="9eadb-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9eadb-135">OUTPUTS</span></span>

### <span data-ttu-id="9eadb-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="9eadb-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="9eadb-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="9eadb-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="9eadb-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9eadb-138">NOTES</span></span>

## <span data-ttu-id="9eadb-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9eadb-139">RELATED LINKS</span></span>
