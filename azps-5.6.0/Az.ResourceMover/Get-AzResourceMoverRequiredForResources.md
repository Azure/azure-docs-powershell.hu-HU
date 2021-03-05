---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverrequiredforresources
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverRequiredForResources.md
ms.openlocfilehash: 9aa09de52a6b731fbf57b309fb605c0ba07325da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000006"
---
# <span data-ttu-id="cbc1e-101">Get-AzResourceMoverRequiredForResources</span><span class="sxs-lookup"><span data-stu-id="cbc1e-101">Get-AzResourceMoverRequiredForResources</span></span>

## <span data-ttu-id="cbc1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbc1e-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc1e-103">Azon áthelyezési erőforrások listája, amelyekhez szükséges a felkarerőforrás.</span><span class="sxs-lookup"><span data-stu-id="cbc1e-103">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="cbc1e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cbc1e-104">SYNTAX</span></span>

```
Get-AzResourceMoverRequiredForResources -MoveCollectionName <String> -ResourceGroupName <String>
 -SourceId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cbc1e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cbc1e-105">DESCRIPTION</span></span>
<span data-ttu-id="cbc1e-106">Azon áthelyezési erőforrások listája, amelyekhez szükséges a felkarerőforrás.</span><span class="sxs-lookup"><span data-stu-id="cbc1e-106">List of the move resources for which an arm resource is required for.</span></span>

## <span data-ttu-id="cbc1e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cbc1e-107">EXAMPLES</span></span>

### <span data-ttu-id="cbc1e-108">1. példa: A megadott erőforrás hozzáadásához szükséges ARMID-erőforrások listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="cbc1e-108">Example 1: Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>
```powershell
PS C:\> Get-AzResourceMoverRequiredForResources -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups"

/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Compute/virtualMachines/PSDemoVM
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="cbc1e-109">A megadott erőforrás hozzáadásához szükséges ARMID-erőforrások listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="cbc1e-109">Get a list of required resource ARMIDs that are required to be added, to add the specified resource.</span></span>

## <span data-ttu-id="cbc1e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbc1e-110">PARAMETERS</span></span>

### <span data-ttu-id="cbc1e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc1e-111">-DefaultProfile</span></span>
<span data-ttu-id="cbc1e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbc1e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc1e-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="cbc1e-113">-MoveCollectionName</span></span>
<span data-ttu-id="cbc1e-114">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="cbc1e-114">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc1e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbc1e-115">-ResourceGroupName</span></span>
<span data-ttu-id="cbc1e-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="cbc1e-116">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc1e-117">-SourceId</span><span class="sxs-lookup"><span data-stu-id="cbc1e-117">-SourceId</span></span>
<span data-ttu-id="cbc1e-118">Az a sourceId, amelyhez az api meg van hívva.</span><span class="sxs-lookup"><span data-stu-id="cbc1e-118">The sourceId for which the api is invoked.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc1e-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cbc1e-119">-SubscriptionId</span></span>
<span data-ttu-id="cbc1e-120">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cbc1e-120">The Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbc1e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc1e-121">CommonParameters</span></span>
<span data-ttu-id="cbc1e-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbc1e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc1e-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbc1e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc1e-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbc1e-124">INPUTS</span></span>

## <span data-ttu-id="cbc1e-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbc1e-125">OUTPUTS</span></span>

### <span data-ttu-id="cbc1e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="cbc1e-126">System.String</span></span>

## <span data-ttu-id="cbc1e-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cbc1e-127">NOTES</span></span>

<span data-ttu-id="cbc1e-128">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="cbc1e-128">ALIASES</span></span>

## <span data-ttu-id="cbc1e-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbc1e-129">RELATED LINKS</span></span>

