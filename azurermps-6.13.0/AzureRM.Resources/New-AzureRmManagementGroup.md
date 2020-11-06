---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroup.md
ms.openlocfilehash: 20cfc2ef6b4b59e8cdd605dd14302aa1a172acb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491859"
---
# <span data-ttu-id="f069f-101">New-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f069f-101">New-AzureRmManagementGroup</span></span>

## <span data-ttu-id="f069f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f069f-102">SYNOPSIS</span></span>
<span data-ttu-id="f069f-103">Felügyeleti csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="f069f-103">Creates a Management Group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f069f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f069f-104">SYNTAX</span></span>

### <span data-ttu-id="f069f-105">GroupOperations (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f069f-105">GroupOperations (Default)</span></span>
```
New-AzureRmManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f069f-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="f069f-106">ParentGroupObject</span></span>
```
New-AzureRmManagementGroup [-GroupName] <String> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f069f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f069f-107">DESCRIPTION</span></span>
<span data-ttu-id="f069f-108">A **New-AzureRMManagementGroup** parancsmag létrehoz egy felügyeleti csoportot.</span><span class="sxs-lookup"><span data-stu-id="f069f-108">The **New-AzureRMManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="f069f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f069f-109">EXAMPLES</span></span>

### <span data-ttu-id="f069f-110">Példa 1: felügyeleti csoport létrehozása</span><span class="sxs-lookup"><span data-stu-id="f069f-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup"

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

<span data-ttu-id="f069f-111">Új csoport létrehozása `DisplayName` és `ParentId` beállítása `null`</span><span class="sxs-lookup"><span data-stu-id="f069f-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="f069f-112">Az `DisplayName` ugyanaz lesz, mint a `GroupName` csoport anyavállalata lesz a bérlő.</span><span class="sxs-lookup"><span data-stu-id="f069f-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="f069f-113">2. példa: felügyeleti csoport létrehozása megjelenítendő névvel</span><span class="sxs-lookup"><span data-stu-id="f069f-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

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

<span data-ttu-id="f069f-114">Ebben az esetben a csoport szülője lesz a bérlő, és a `DisplayName` megjelenő érték az adott értékre lesz állítva.</span><span class="sxs-lookup"><span data-stu-id="f069f-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="f069f-115">3. példa: felügyeleti csoport létrehozása szülővel és megjelenített névvel</span><span class="sxs-lookup"><span data-stu-id="f069f-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

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

### <span data-ttu-id="f069f-116">4. példa: felügyeleti csoport létrehozása szülővel (szülő objektum használatával)</span><span class="sxs-lookup"><span data-stu-id="f069f-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzureRmManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzureRmManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="f069f-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f069f-117">PARAMETERS</span></span>

### <span data-ttu-id="f069f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f069f-118">-DefaultProfile</span></span>
<span data-ttu-id="f069f-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f069f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f069f-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f069f-120">-DisplayName</span></span>
<span data-ttu-id="f069f-121">A felügyeleti csoport megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="f069f-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="f069f-122">-Csoportnév</span><span class="sxs-lookup"><span data-stu-id="f069f-122">-GroupName</span></span>
<span data-ttu-id="f069f-123">Felügyeleti csoport azonosítója</span><span class="sxs-lookup"><span data-stu-id="f069f-123">Management Group Id</span></span>

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

### <span data-ttu-id="f069f-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="f069f-124">-ParentId</span></span>
<span data-ttu-id="f069f-125">A felügyeleti csoport fölérendelt azonosítója</span><span class="sxs-lookup"><span data-stu-id="f069f-125">Parent Id of the management group</span></span>

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

### <span data-ttu-id="f069f-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f069f-126">-ParentObject</span></span>
<span data-ttu-id="f069f-127">Fölérendelt objektum</span><span class="sxs-lookup"><span data-stu-id="f069f-127">Parent Object</span></span>

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

### <span data-ttu-id="f069f-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f069f-128">-Confirm</span></span>
<span data-ttu-id="f069f-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f069f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f069f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f069f-130">-WhatIf</span></span>
<span data-ttu-id="f069f-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f069f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f069f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f069f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f069f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f069f-133">CommonParameters</span></span>
<span data-ttu-id="f069f-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f069f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f069f-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f069f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f069f-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f069f-136">INPUTS</span></span>

### <span data-ttu-id="f069f-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="f069f-137">None</span></span>

## <span data-ttu-id="f069f-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f069f-138">OUTPUTS</span></span>

### <span data-ttu-id="f069f-139">Microsoft. Azure. Command. Resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f069f-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="f069f-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f069f-140">NOTES</span></span>

## <span data-ttu-id="f069f-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f069f-141">RELATED LINKS</span></span>

[<span data-ttu-id="f069f-142">Remove-AzureRMManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f069f-142">Remove-AzureRMManagementGroup</span></span>](./Remove-AzureRMManagementGroup.md)

[<span data-ttu-id="f069f-143">Update-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f069f-143">Update-AzureRmManagementGroup</span></span>](./Update-AzureRmManagementGroup.md)

[<span data-ttu-id="f069f-144">Get-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="f069f-144">Get-AzureRmManagementGroup</span></span>](./Get-AzureRmManagementGroup.md)
