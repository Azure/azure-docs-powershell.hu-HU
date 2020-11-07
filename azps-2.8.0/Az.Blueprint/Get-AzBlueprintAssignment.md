---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 121811c88493a4f6f069a60c8f9662eb9d11303e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667641"
---
# <span data-ttu-id="249a7-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="249a7-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="249a7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="249a7-102">SYNOPSIS</span></span>
<span data-ttu-id="249a7-103">Szerezzen be egy vagy több feladatot a tervekhez.</span><span class="sxs-lookup"><span data-stu-id="249a7-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="249a7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="249a7-104">SYNTAX</span></span>

### <span data-ttu-id="249a7-105">BlueprintAssignmentsBySubscription (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="249a7-105">BlueprintAssignmentsBySubscription (Default)</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="249a7-106">BlueprintAssignmentByName</span><span class="sxs-lookup"><span data-stu-id="249a7-106">BlueprintAssignmentByName</span></span>
```
Get-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="249a7-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="249a7-107">DESCRIPTION</span></span>
<span data-ttu-id="249a7-108">Szerezzen be egy vagy több feladatot a tervekhez.</span><span class="sxs-lookup"><span data-stu-id="249a7-108">Get one or more blueprint assignments.</span></span> <span data-ttu-id="249a7-109">A Blueprint-hozzárendelések létezik az előfizetési tartományon.</span><span class="sxs-lookup"><span data-stu-id="249a7-109">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="249a7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="249a7-110">EXAMPLES</span></span>

### <span data-ttu-id="249a7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="249a7-111">Example 1</span></span>
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

<span data-ttu-id="249a7-112">A megadott előfizetésből származó feladatok kiosztásának beszerzése</span><span class="sxs-lookup"><span data-stu-id="249a7-112">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="249a7-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="249a7-113">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="249a7-114">A megadott előfizetéshez tartozó megadott névvel beolvashatja a terv hozzárendelését.</span><span class="sxs-lookup"><span data-stu-id="249a7-114">Get the blueprint assignment with the given name within the specified subscription.</span></span>

## <span data-ttu-id="249a7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="249a7-115">PARAMETERS</span></span>

### <span data-ttu-id="249a7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="249a7-116">-DefaultProfile</span></span>
<span data-ttu-id="249a7-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="249a7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="249a7-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="249a7-118">-Name</span></span>
<span data-ttu-id="249a7-119">Terv hozzárendelésének neve.</span><span class="sxs-lookup"><span data-stu-id="249a7-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="249a7-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="249a7-120">-SubscriptionId</span></span>
<span data-ttu-id="249a7-121">Előfizetés azonosítója: a terv-hozzárendelés üzembe helyezése.</span><span class="sxs-lookup"><span data-stu-id="249a7-121">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="249a7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="249a7-122">CommonParameters</span></span>
<span data-ttu-id="249a7-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="249a7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="249a7-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="249a7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="249a7-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="249a7-125">INPUTS</span></span>

### <span data-ttu-id="249a7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="249a7-126">System.String</span></span>

## <span data-ttu-id="249a7-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="249a7-127">OUTPUTS</span></span>

### <span data-ttu-id="249a7-128">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="249a7-128">System.Object</span></span>
## <span data-ttu-id="249a7-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="249a7-129">NOTES</span></span>

## <span data-ttu-id="249a7-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="249a7-130">RELATED LINKS</span></span>
