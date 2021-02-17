---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205134"
---
# <span data-ttu-id="574de-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="574de-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="574de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="574de-102">SYNOPSIS</span></span>
<span data-ttu-id="574de-103">Egy vagy több tervrajz-feladat kiosztása.</span><span class="sxs-lookup"><span data-stu-id="574de-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="574de-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="574de-104">SYNTAX</span></span>

### <span data-ttu-id="574de-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="574de-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="574de-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="574de-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="574de-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="574de-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="574de-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="574de-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="574de-109">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="574de-109">DESCRIPTION</span></span>
<span data-ttu-id="574de-110">Egy vagy több terv-feladat kiosztása.</span><span class="sxs-lookup"><span data-stu-id="574de-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="574de-111">A terv-hozzárendelések az előfizetés hatókörében léteznek.</span><span class="sxs-lookup"><span data-stu-id="574de-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="574de-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="574de-112">EXAMPLES</span></span>

### <span data-ttu-id="574de-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="574de-113">Example 1</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name              : Assignment-PS-BlueprintDefinition
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : AllResourcesReadOnly
ProvisioningState : Succeeded
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="574de-114">Szerezze be a terv-hozzárendeléseket a megadott előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="574de-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="574de-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="574de-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="574de-116">Szerezze be a terv-hozzárendelést a megadott néven a megadott előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="574de-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="574de-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="574de-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="574de-118">Szerezze be a terv-hozzárendeléseket a megadott felügyeleti csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="574de-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="574de-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="574de-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="574de-120">Szerezze be a terv-hozzárendelést a megadott néven a megadott felügyeleti csoporton belül.</span><span class="sxs-lookup"><span data-stu-id="574de-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="574de-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="574de-121">PARAMETERS</span></span>

### <span data-ttu-id="574de-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="574de-122">-DefaultProfile</span></span>
<span data-ttu-id="574de-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="574de-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="574de-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="574de-124">-ManagementGroupId</span></span>
<span data-ttu-id="574de-125">Annak a felügyeleti csoportnak az azonosítója, amelybe a Tervrajz feladatot mentette.</span><span class="sxs-lookup"><span data-stu-id="574de-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574de-126">-Name</span><span class="sxs-lookup"><span data-stu-id="574de-126">-Name</span></span>
<span data-ttu-id="574de-127">A terv feladatának neve.</span><span class="sxs-lookup"><span data-stu-id="574de-127">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574de-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="574de-128">-SubscriptionId</span></span>
<span data-ttu-id="574de-129">Előfizetés azonosítója: A terv hozzárendelése telepítve van.</span><span class="sxs-lookup"><span data-stu-id="574de-129">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="574de-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="574de-130">CommonParameters</span></span>
<span data-ttu-id="574de-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="574de-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="574de-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="574de-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="574de-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="574de-133">INPUTS</span></span>

### <span data-ttu-id="574de-134">System.String</span><span class="sxs-lookup"><span data-stu-id="574de-134">System.String</span></span>

## <span data-ttu-id="574de-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="574de-135">OUTPUTS</span></span>

### <span data-ttu-id="574de-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="574de-136">System.Object</span></span>
## <span data-ttu-id="574de-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="574de-137">NOTES</span></span>

## <span data-ttu-id="574de-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="574de-138">RELATED LINKS</span></span>
