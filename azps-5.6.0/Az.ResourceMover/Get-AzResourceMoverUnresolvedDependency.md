---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 34cae1bcc6020e2e0c2a8b2f6b70e302c8576f2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999990"
---
# <span data-ttu-id="c579e-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="c579e-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="c579e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c579e-102">SYNOPSIS</span></span>
<span data-ttu-id="c579e-103">A nem megoldott függőségek listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c579e-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="c579e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c579e-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DependencyLevel <DependencyLevel>] [-Filter <String>] [-Orderby <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c579e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c579e-105">DESCRIPTION</span></span>
<span data-ttu-id="c579e-106">A nem megoldott függőségek listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c579e-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="c579e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c579e-107">EXAMPLES</span></span>

### <span data-ttu-id="c579e-108">1. példa: Egy áthelyezési gyűjtemény azonosítatlan függő erőforrásainak listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="c579e-108">Example 1: Get list of unresolved dependent resources for a Move Collection.</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -ResourceGroupName "RG-MoveCollection-demoRMS" -DependencyLevel Descendant
Count Id                                                                                                                                        
----- --                                                                                                                                        
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111   
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
    1 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
    3 /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm
```

<span data-ttu-id="c579e-109">Az Áthelyezési gyűjtemény azonosítatlan függő erőforrásainak listája.</span><span class="sxs-lookup"><span data-stu-id="c579e-109">Get a list of unresolved dependent resources for a Move Collection.</span></span>

## <span data-ttu-id="c579e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c579e-110">PARAMETERS</span></span>

### <span data-ttu-id="c579e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c579e-111">-DefaultProfile</span></span>
<span data-ttu-id="c579e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c579e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c579e-113">-DependencyLevel</span><span class="sxs-lookup"><span data-stu-id="c579e-113">-DependencyLevel</span></span>
<span data-ttu-id="c579e-114">A függőségi szintet határozza meg.</span><span class="sxs-lookup"><span data-stu-id="c579e-114">Defines the dependency level.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.DependencyLevel
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c579e-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="c579e-115">-Filter</span></span>
<span data-ttu-id="c579e-116">A műveletre alkalmazandó szűrő.</span><span class="sxs-lookup"><span data-stu-id="c579e-116">The filter to apply on the operation.</span></span>
<span data-ttu-id="c579e-117">Például: $apply=filter(count eq 2).</span><span class="sxs-lookup"><span data-stu-id="c579e-117">For example, $apply=filter(count eq 2).</span></span>

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

### <span data-ttu-id="c579e-118">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="c579e-118">-MoveCollectionName</span></span>
<span data-ttu-id="c579e-119">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="c579e-119">The Move Collection Name.</span></span>

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

### <span data-ttu-id="c579e-120">-Orderby</span><span class="sxs-lookup"><span data-stu-id="c579e-120">-Orderby</span></span>
<span data-ttu-id="c579e-121">OData-sorrend lekérdezések szerint beállítás.</span><span class="sxs-lookup"><span data-stu-id="c579e-121">OData order by query option.</span></span>
<span data-ttu-id="c579e-122">Használhatja például a $orderby=Count desc használhatja.</span><span class="sxs-lookup"><span data-stu-id="c579e-122">For example, you can use $orderby=Count desc.</span></span>

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

### <span data-ttu-id="c579e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c579e-123">-ResourceGroupName</span></span>
<span data-ttu-id="c579e-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c579e-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="c579e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c579e-125">-SubscriptionId</span></span>
<span data-ttu-id="c579e-126">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c579e-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="c579e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c579e-127">CommonParameters</span></span>
<span data-ttu-id="c579e-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c579e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c579e-129">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c579e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c579e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c579e-130">INPUTS</span></span>

## <span data-ttu-id="c579e-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c579e-131">OUTPUTS</span></span>

### <span data-ttu-id="c579e-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="c579e-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IUnresolvedDependency</span></span>

## <span data-ttu-id="c579e-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c579e-133">NOTES</span></span>

<span data-ttu-id="c579e-134">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c579e-134">ALIASES</span></span>

## <span data-ttu-id="c579e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c579e-135">RELATED LINKS</span></span>

