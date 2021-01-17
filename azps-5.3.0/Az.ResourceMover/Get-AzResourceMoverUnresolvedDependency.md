---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468578"
---
# <span data-ttu-id="888ab-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="888ab-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="888ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="888ab-102">SYNOPSIS</span></span>
<span data-ttu-id="888ab-103">A nem megoldott függőségek listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="888ab-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="888ab-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="888ab-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="888ab-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="888ab-105">DESCRIPTION</span></span>
<span data-ttu-id="888ab-106">A nem megoldott függőségek listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="888ab-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="888ab-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="888ab-107">EXAMPLES</span></span>

### <span data-ttu-id="888ab-108">1. példa: A meg nem oldott függő erőforrások listájának lekérte</span><span class="sxs-lookup"><span data-stu-id="888ab-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="888ab-109">Az Áthelyezés gyűjtemény azonosítatlan függő erőforrásainak listájának lekérte.</span><span class="sxs-lookup"><span data-stu-id="888ab-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="888ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="888ab-110">PARAMETERS</span></span>

### <span data-ttu-id="888ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="888ab-111">-DefaultProfile</span></span>
<span data-ttu-id="888ab-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="888ab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="888ab-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="888ab-113">-MoveCollectionName</span></span>
<span data-ttu-id="888ab-114">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="888ab-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="888ab-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="888ab-115">-ResourceGroupName</span></span>
<span data-ttu-id="888ab-116">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="888ab-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="888ab-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="888ab-117">-SubscriptionId</span></span>
<span data-ttu-id="888ab-118">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="888ab-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="888ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="888ab-119">CommonParameters</span></span>
<span data-ttu-id="888ab-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="888ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="888ab-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="888ab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="888ab-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="888ab-122">INPUTS</span></span>

## <span data-ttu-id="888ab-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="888ab-123">OUTPUTS</span></span>

### <span data-ttu-id="888ab-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="888ab-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="888ab-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="888ab-125">NOTES</span></span>

<span data-ttu-id="888ab-126">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="888ab-126">ALIASES</span></span>

## <span data-ttu-id="888ab-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="888ab-127">RELATED LINKS</span></span>

