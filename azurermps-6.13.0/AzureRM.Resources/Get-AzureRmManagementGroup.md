---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagementGroup.md
ms.openlocfilehash: 275b13efa25bbffd2c104a1e9cfa3baf04fffe89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673133"
---
# <span data-ttu-id="27a03-101">Get-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="27a03-101">Get-AzureRmManagementGroup</span></span>

## <span data-ttu-id="27a03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="27a03-102">SYNOPSIS</span></span>
<span data-ttu-id="27a03-103">Felügyeleti csoport (ok) beolvasása</span><span class="sxs-lookup"><span data-stu-id="27a03-103">Gets Management Group(s)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27a03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="27a03-104">SYNTAX</span></span>

### <span data-ttu-id="27a03-105">ListOperation (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="27a03-105">ListOperation (Default)</span></span>
```
Get-AzureRmManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a03-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="27a03-106">GetOperation</span></span>
```
Get-AzureRmManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand]
 [-Recurse] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27a03-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="27a03-107">DESCRIPTION</span></span>
<span data-ttu-id="27a03-108">A Get-AzureRMManagementGroup parancsmag a teljes vagy egy bizonyos kezelési csoportot kapja.</span><span class="sxs-lookup"><span data-stu-id="27a03-108">The Get-AzureRMManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="27a03-109">Példák</span><span class="sxs-lookup"><span data-stu-id="27a03-109">EXAMPLES</span></span>

### <span data-ttu-id="27a03-110">1. példa: az összes felügyeleti csoport beolvasása</span><span class="sxs-lookup"><span data-stu-id="27a03-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzureRmManagementGroup

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

### <span data-ttu-id="27a03-111">2. példa: speciális kezelési csoport beszerzése</span><span class="sxs-lookup"><span data-stu-id="27a03-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzureRmManagementGroup -GroupName TestGroup

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

### <span data-ttu-id="27a03-112">3. példa: speciális kezelési csoport és a hierarchia első szintjének beolvasása</span><span class="sxs-lookup"><span data-stu-id="27a03-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzureRmManagementGroup -GroupName TestGroupParent -Expand
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

<span data-ttu-id="27a03-113">A `Expand` jelölővel navigálhat a `Children` tömbben, és az egyes gyermekekre vonatkozóan információkat kaphat.</span><span class="sxs-lookup"><span data-stu-id="27a03-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="27a03-114">`Children[0]`A megjelenítendő névvel rendelkező csoport adatait például részletezni fogja `TestGroup1DisplayName` .</span><span class="sxs-lookup"><span data-stu-id="27a03-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="27a03-115">Példa 4: speciális kezelési csoport és a képekből hierarchikus minden szintjének beolvasása</span><span class="sxs-lookup"><span data-stu-id="27a03-115">Example 4: Get specific Management Group and all levels of hiearchy</span></span>
```
PS C:\> $response = Get-AzureRmManagementGroup -GroupName TestGroupParent -Expand -Recurse
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

## <span data-ttu-id="27a03-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="27a03-116">PARAMETERS</span></span>

### <span data-ttu-id="27a03-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a03-117">-DefaultProfile</span></span>
<span data-ttu-id="27a03-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="27a03-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a03-119">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="27a03-119">-Expand</span></span>
<span data-ttu-id="27a03-120">A kimenet kibontása a felügyeleti csoport gyermekeinek listájára</span><span class="sxs-lookup"><span data-stu-id="27a03-120">Expand the output to list the children of the management group</span></span>

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

### <span data-ttu-id="27a03-121">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="27a03-121">-GroupName</span></span>
<span data-ttu-id="27a03-122">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="27a03-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a03-123">-Recurse</span><span class="sxs-lookup"><span data-stu-id="27a03-123">-Recurse</span></span>
<span data-ttu-id="27a03-124">A felügyeleti csoport gyermekeinek rekurzív listája</span><span class="sxs-lookup"><span data-stu-id="27a03-124">Recursively list the children of the management group</span></span>

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

### <span data-ttu-id="27a03-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="27a03-125">-Confirm</span></span>
<span data-ttu-id="27a03-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="27a03-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27a03-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27a03-127">-WhatIf</span></span>
<span data-ttu-id="27a03-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="27a03-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27a03-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="27a03-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27a03-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a03-130">CommonParameters</span></span>
<span data-ttu-id="27a03-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="27a03-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a03-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27a03-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a03-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="27a03-133">INPUTS</span></span>

### <span data-ttu-id="27a03-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="27a03-134">None</span></span>

## <span data-ttu-id="27a03-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="27a03-135">OUTPUTS</span></span>

### <span data-ttu-id="27a03-136">Microsoft. Azure. Command. Resources. models. ManagementGroups. PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="27a03-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="27a03-137">Microsoft. Azure. Command. Resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="27a03-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="27a03-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="27a03-138">NOTES</span></span>

## <span data-ttu-id="27a03-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="27a03-139">RELATED LINKS</span></span>
