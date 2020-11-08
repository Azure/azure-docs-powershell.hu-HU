---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: bdef58db8dcda735a7a8c08350b806c9fd00cf21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188200"
---
# <span data-ttu-id="72802-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="72802-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="72802-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72802-102">SYNOPSIS</span></span>
<span data-ttu-id="72802-103">Felügyeleti csoport frissítése</span><span class="sxs-lookup"><span data-stu-id="72802-103">Updates a Management Group</span></span>

## <span data-ttu-id="72802-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72802-104">SYNTAX</span></span>

### <span data-ttu-id="72802-105">GroupOperations (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="72802-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72802-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="72802-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72802-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="72802-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72802-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="72802-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72802-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="72802-109">DESCRIPTION</span></span>
<span data-ttu-id="72802-110">Az **Update-AzManagementGroup** parancsmag frissíti a **ParentID** vagy a **DisplayName attribútumot** egy kezelési csoportban.</span><span class="sxs-lookup"><span data-stu-id="72802-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="72802-111">Példák</span><span class="sxs-lookup"><span data-stu-id="72802-111">EXAMPLES</span></span>

### <span data-ttu-id="72802-112">Példa 1: a felügyeleti csoport megjelenítendő nevének frissítése</span><span class="sxs-lookup"><span data-stu-id="72802-112">Example 1: Update a Management Group's Display Name</span></span>
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

### <span data-ttu-id="72802-113">2. példa: a felügyeleti csoport szülőjének frissítése</span><span class="sxs-lookup"><span data-stu-id="72802-113">Example 2: Update a Management Group's Parent</span></span>
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

### <span data-ttu-id="72802-114">3. példa: felügyeleti csoport frissítése csővezeték-PSManagementGroup objektummal</span><span class="sxs-lookup"><span data-stu-id="72802-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
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

### <span data-ttu-id="72802-115">Példa 4: a felügyeleti csoport szülőjének frissítése a ParentObject használatával</span><span class="sxs-lookup"><span data-stu-id="72802-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
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

## <span data-ttu-id="72802-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72802-116">PARAMETERS</span></span>

### <span data-ttu-id="72802-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72802-117">-DefaultProfile</span></span>
<span data-ttu-id="72802-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72802-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72802-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="72802-119">-DisplayName</span></span>
<span data-ttu-id="72802-120">A felügyeleti csoport megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="72802-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="72802-121">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="72802-121">-GroupName</span></span>
<span data-ttu-id="72802-122">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="72802-122">Management Group Id</span></span>

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

### <span data-ttu-id="72802-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72802-123">-InputObject</span></span>
<span data-ttu-id="72802-124">Beviteli objektum a hívás kérése</span><span class="sxs-lookup"><span data-stu-id="72802-124">Input Object from the Get call</span></span>

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

### <span data-ttu-id="72802-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="72802-125">-ParentId</span></span>
<span data-ttu-id="72802-126">A felügyeleti csoport fölérendelt azonosítója</span><span class="sxs-lookup"><span data-stu-id="72802-126">Parent Id of the management group</span></span>

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

### <span data-ttu-id="72802-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="72802-127">-ParentObject</span></span>
<span data-ttu-id="72802-128">Beviteli objektum a hívás kérése</span><span class="sxs-lookup"><span data-stu-id="72802-128">Input Object from the Get call</span></span>

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

### <span data-ttu-id="72802-129">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="72802-129">-Confirm</span></span>
<span data-ttu-id="72802-130">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="72802-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72802-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72802-131">-WhatIf</span></span>
<span data-ttu-id="72802-132">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="72802-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72802-133">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="72802-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72802-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72802-134">CommonParameters</span></span>
<span data-ttu-id="72802-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="72802-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72802-136">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="72802-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72802-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72802-137">INPUTS</span></span>

### <span data-ttu-id="72802-138">Microsoft. Azure. Command. Resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="72802-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="72802-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72802-139">OUTPUTS</span></span>

### <span data-ttu-id="72802-140">Microsoft. Azure. Command. Resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="72802-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="72802-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72802-141">NOTES</span></span>

## <span data-ttu-id="72802-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72802-142">RELATED LINKS</span></span>