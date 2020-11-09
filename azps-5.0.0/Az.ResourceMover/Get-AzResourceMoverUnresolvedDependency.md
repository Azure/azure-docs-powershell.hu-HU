---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/get-azresourcemoverunresolveddependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Get-AzResourceMoverUnresolvedDependency.md
ms.openlocfilehash: 261ca79618f6d0568647f9126e0fddeaeb8db540
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302504"
---
# <span data-ttu-id="10b8a-101">Get-AzResourceMoverUnresolvedDependency</span><span class="sxs-lookup"><span data-stu-id="10b8a-101">Get-AzResourceMoverUnresolvedDependency</span></span>

## <span data-ttu-id="10b8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="10b8a-103">A feloldatlan függőségek listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="10b8a-103">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="10b8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10b8a-104">SYNTAX</span></span>

```
Get-AzResourceMoverUnresolvedDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="10b8a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="10b8a-105">DESCRIPTION</span></span>
<span data-ttu-id="10b8a-106">A feloldatlan függőségek listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="10b8a-106">Gets a list of unresolved dependencies.</span></span>

## <span data-ttu-id="10b8a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="10b8a-107">EXAMPLES</span></span>

### <span data-ttu-id="10b8a-108">Példa 1: a feloldatlan függő erőforrások listájának beolvasása</span><span class="sxs-lookup"><span data-stu-id="10b8a-108">Example 1: Get list of unresolved dependent resources</span></span>
```powershell
PS C:\> Get-AzResourceMoverUnresolvedDependency -MoveCollectionName PS-centralus-westcentralus-demoRM -ResourceGroupName RG-MoveCollection-demoRM
Count Id
----- --
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/publicipaddresses/psdemovm-ip
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/virtualnetworks/psdemorm-vnet
1     /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg
```

<span data-ttu-id="10b8a-109">Az áthelyezési gyűjtemények feloldatlan függő erőforrásainak listája</span><span class="sxs-lookup"><span data-stu-id="10b8a-109">Get list of unresolved dependent resources for a Move collection.</span></span>

## <span data-ttu-id="10b8a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10b8a-110">PARAMETERS</span></span>

### <span data-ttu-id="10b8a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b8a-111">-DefaultProfile</span></span>
<span data-ttu-id="10b8a-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10b8a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10b8a-113">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="10b8a-113">-MoveCollectionName</span></span>
<span data-ttu-id="10b8a-114">Az áthelyezés gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="10b8a-114">The Move Collection Name.</span></span>

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

### <span data-ttu-id="10b8a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10b8a-115">-ResourceGroupName</span></span>
<span data-ttu-id="10b8a-116">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="10b8a-116">The Resource Group Name.</span></span>

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

### <span data-ttu-id="10b8a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="10b8a-117">-SubscriptionId</span></span>
<span data-ttu-id="10b8a-118">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="10b8a-118">The Subscription ID.</span></span>

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

### <span data-ttu-id="10b8a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b8a-119">CommonParameters</span></span>
<span data-ttu-id="10b8a-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10b8a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b8a-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="10b8a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b8a-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10b8a-122">INPUTS</span></span>

## <span data-ttu-id="10b8a-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10b8a-123">OUTPUTS</span></span>

### <span data-ttu-id="10b8a-124">Microsoft. Azure. PowerShell. parancsmagok. ResourceMover. modellek. Api20191001Preview. IUnresolvedDependencyCollection</span><span class="sxs-lookup"><span data-stu-id="10b8a-124">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IUnresolvedDependencyCollection</span></span>

## <span data-ttu-id="10b8a-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10b8a-125">NOTES</span></span>

<span data-ttu-id="10b8a-126">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="10b8a-126">ALIASES</span></span>

## <span data-ttu-id="10b8a-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10b8a-127">RELATED LINKS</span></span>

