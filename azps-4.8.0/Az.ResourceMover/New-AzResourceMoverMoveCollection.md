---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 01fa891933c8c3e3c0b4681a84d17b95ea06a6b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181437"
---
# <span data-ttu-id="a33ac-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="a33ac-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="a33ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a33ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a33ac-103">Áthelyezési gyűjtemény létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="a33ac-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="a33ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a33ac-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a33ac-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a33ac-105">DESCRIPTION</span></span>
<span data-ttu-id="a33ac-106">Áthelyezési gyűjtemény létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="a33ac-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="a33ac-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a33ac-107">EXAMPLES</span></span>

### <span data-ttu-id="a33ac-108">Példa 1: új áthelyezési gyűjtemény létrehozása.</span><span class="sxs-lookup"><span data-stu-id="a33ac-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name PS-centralus-westcentralus-demoRM  -ResourceGroupName RG-MoveCollection-demoRM -SourceRegion centralus -TargetRegion westcentralus -Location eastus2

Location Name                               Type
-------- ----                               ----
eastus2  PS-centralus-westcentralus-demoRM  Microsoft.Migrate/moveCollections
```

<span data-ttu-id="a33ac-109">Új áthelyezési gyűjtemény létrehozása az előfizetésen belül.</span><span class="sxs-lookup"><span data-stu-id="a33ac-109">Create a new Move collection within a subscription.</span></span>

## <span data-ttu-id="a33ac-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a33ac-110">PARAMETERS</span></span>

### <span data-ttu-id="a33ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a33ac-111">-DefaultProfile</span></span>
<span data-ttu-id="a33ac-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a33ac-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a33ac-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="a33ac-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="a33ac-114">A fő azonosítót kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="a33ac-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="a33ac-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="a33ac-115">-IdentityTenantId</span></span>
<span data-ttu-id="a33ac-116">A bérlői azonosítót kapja vagy állítja be.</span><span class="sxs-lookup"><span data-stu-id="a33ac-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="a33ac-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a33ac-117">-IdentityType</span></span>
<span data-ttu-id="a33ac-118">A területi áthelyezési szolgáltatáshoz használt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="a33ac-118">The type of identity used for the region move service.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.ResourceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33ac-119">-Hely</span><span class="sxs-lookup"><span data-stu-id="a33ac-119">-Location</span></span>
<span data-ttu-id="a33ac-120">Az a földrajzi hely, ahol az erőforrás él.</span><span class="sxs-lookup"><span data-stu-id="a33ac-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="a33ac-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a33ac-121">-Name</span></span>
<span data-ttu-id="a33ac-122">Az áthelyezés gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="a33ac-122">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a33ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="a33ac-124">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a33ac-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="a33ac-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="a33ac-125">-SourceRegion</span></span>
<span data-ttu-id="a33ac-126">A forrás terület beolvasása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="a33ac-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="a33ac-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a33ac-127">-SubscriptionId</span></span>
<span data-ttu-id="a33ac-128">Az előfizetési azonosító.</span><span class="sxs-lookup"><span data-stu-id="a33ac-128">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33ac-129">-Címke</span><span class="sxs-lookup"><span data-stu-id="a33ac-129">-Tag</span></span>
<span data-ttu-id="a33ac-130">Erőforrás-címkék.</span><span class="sxs-lookup"><span data-stu-id="a33ac-130">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a33ac-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="a33ac-131">-TargetRegion</span></span>
<span data-ttu-id="a33ac-132">A cél területének beolvasása vagy beállítása.</span><span class="sxs-lookup"><span data-stu-id="a33ac-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="a33ac-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a33ac-133">-Confirm</span></span>
<span data-ttu-id="a33ac-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a33ac-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a33ac-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a33ac-135">-WhatIf</span></span>
<span data-ttu-id="a33ac-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a33ac-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a33ac-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a33ac-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a33ac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a33ac-138">CommonParameters</span></span>
<span data-ttu-id="a33ac-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a33ac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a33ac-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a33ac-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a33ac-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a33ac-141">INPUTS</span></span>

## <span data-ttu-id="a33ac-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a33ac-142">OUTPUTS</span></span>

### <span data-ttu-id="a33ac-143">Microsoft. Azure. PowerShell. parancsmagok. ResourceMover. modellek. Api20191001Preview. IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="a33ac-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IMoveCollection</span></span>

## <span data-ttu-id="a33ac-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a33ac-144">NOTES</span></span>

<span data-ttu-id="a33ac-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="a33ac-145">ALIASES</span></span>

## <span data-ttu-id="a33ac-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a33ac-146">RELATED LINKS</span></span>

