---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186112"
---
# <span data-ttu-id="f7ec5-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="f7ec5-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="f7ec5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ec5-103">Szerezzen be egy vagy több feladatot a tervekhez.</span><span class="sxs-lookup"><span data-stu-id="f7ec5-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="f7ec5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7ec5-104">SYNTAX</span></span>

### <span data-ttu-id="f7ec5-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7ec5-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7ec5-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="f7ec5-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7ec5-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="f7ec5-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7ec5-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="f7ec5-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7ec5-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7ec5-109">DESCRIPTION</span></span>
<span data-ttu-id="f7ec5-110">Szerezzen be egy vagy több feladatot a tervekhez.</span><span class="sxs-lookup"><span data-stu-id="f7ec5-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="f7ec5-111">A Blueprint-hozzárendelések létezik az előfizetési tartományon.</span><span class="sxs-lookup"><span data-stu-id="f7ec5-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="f7ec5-112">Példák</span><span class="sxs-lookup"><span data-stu-id="f7ec5-112">EXAMPLES</span></span>

### <span data-ttu-id="f7ec5-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f7ec5-113">Example 1</span></span>
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

<span data-ttu-id="f7ec5-114">A megadott előfizetésből származó feladatok kiosztásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="f7ec5-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="f7ec5-115">2. példa</span><span class="sxs-lookup"><span data-stu-id="f7ec5-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="f7ec5-116">A megadott előfizetéshez tartozó megadott névvel beolvashatja a terv hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="f7ec5-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="f7ec5-117">3. példa</span><span class="sxs-lookup"><span data-stu-id="f7ec5-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="f7ec5-118">A terv szerinti hozzárendelések beszerzése a megadott felügyeleti csoportba.</span><span class="sxs-lookup"><span data-stu-id="f7ec5-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="f7ec5-119">4. példa</span><span class="sxs-lookup"><span data-stu-id="f7ec5-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="f7ec5-120">A megadott nevű felügyeleti csoportban adja meg a terv hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="f7ec5-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="f7ec5-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7ec5-121">PARAMETERS</span></span>

### <span data-ttu-id="f7ec5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ec5-122">-DefaultProfile</span></span>
<span data-ttu-id="f7ec5-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7ec5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7ec5-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f7ec5-124">-ManagementGroupId</span></span>
<span data-ttu-id="f7ec5-125">Annak a kezelési csoportnak az azonosítója, amelybe a Blueprint-hozzárendelést mentette.</span><span class="sxs-lookup"><span data-stu-id="f7ec5-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="f7ec5-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f7ec5-126">-Name</span></span>
<span data-ttu-id="f7ec5-127">Terv hozzárendelésének neve.</span><span class="sxs-lookup"><span data-stu-id="f7ec5-127">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="f7ec5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7ec5-128">-SubscriptionId</span></span>
<span data-ttu-id="f7ec5-129">Előfizetés azonosítója: a terv-hozzárendelés üzembe helyezése.</span><span class="sxs-lookup"><span data-stu-id="f7ec5-129">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="f7ec5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ec5-130">CommonParameters</span></span>
<span data-ttu-id="f7ec5-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7ec5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ec5-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f7ec5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ec5-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7ec5-133">INPUTS</span></span>

### <span data-ttu-id="f7ec5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f7ec5-134">System.String</span></span>

## <span data-ttu-id="f7ec5-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7ec5-135">OUTPUTS</span></span>

### <span data-ttu-id="f7ec5-136">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="f7ec5-136">System.Object</span></span>
## <span data-ttu-id="f7ec5-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7ec5-137">NOTES</span></span>

## <span data-ttu-id="f7ec5-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7ec5-138">RELATED LINKS</span></span>