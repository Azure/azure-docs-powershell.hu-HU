---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/new-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/New-AzResourceMoverMoveCollection.md
ms.openlocfilehash: 317614d67138b185dc58334d398bb368fc85911e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999893"
---
# <span data-ttu-id="1595d-101">New-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="1595d-101">New-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="1595d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1595d-102">SYNOPSIS</span></span>
<span data-ttu-id="1595d-103">Áthelyezési gyűjteményt hoz létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="1595d-103">Creates or updates a move collection.</span></span>

## <span data-ttu-id="1595d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1595d-104">SYNTAX</span></span>

```
New-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentityPrincipalId <String>] [-IdentityTenantId <String>] [-IdentityType <ResourceIdentityType>]
 [-Location <String>] [-SourceRegion <String>] [-Tag <Hashtable>] [-TargetRegion <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1595d-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1595d-105">DESCRIPTION</span></span>
<span data-ttu-id="1595d-106">Áthelyezési gyűjteményt hoz létre vagy frissíti.</span><span class="sxs-lookup"><span data-stu-id="1595d-106">Creates or updates a move collection.</span></span>

## <span data-ttu-id="1595d-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1595d-107">EXAMPLES</span></span>

### <span data-ttu-id="1595d-108">1. példa: Új áthelyezési gyűjtemény létrehozása.</span><span class="sxs-lookup"><span data-stu-id="1595d-108">Example 1: Create a new Move collection.</span></span>
```powershell
PS C:\> New-AzResourceMoverMoveCollection -Name "PS-centralus-westcentralus-demoRMS"  -ResourceGroupName "RG-MoveCollection-demoRMS" -SourceRegion "centralus" -TargetRegion "westcentralus" -Location "centraluseuap" -IdentityType "SystemAssigned"

Etag                                   Location      Name                               Type                             
----                                   --------      ----                               ----                             
"0200d92f-0000-3300-0000-6021e9ec0000" centraluseuap PS-centralus-westcentralus-demoRMs Microsoft.Migrate/moveCollections
```

<span data-ttu-id="1595d-109">Új áthelyezési gyűjtemény létrehozása</span><span class="sxs-lookup"><span data-stu-id="1595d-109">Create a new Move Collection.</span></span>

## <span data-ttu-id="1595d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1595d-110">PARAMETERS</span></span>

### <span data-ttu-id="1595d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1595d-111">-DefaultProfile</span></span>
<span data-ttu-id="1595d-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1595d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1595d-113">-IdentityPrincipalId</span><span class="sxs-lookup"><span data-stu-id="1595d-113">-IdentityPrincipalId</span></span>
<span data-ttu-id="1595d-114">Beállítja vagy beállítja a fő azonosítót.</span><span class="sxs-lookup"><span data-stu-id="1595d-114">Gets or sets the principal id.</span></span>

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

### <span data-ttu-id="1595d-115">-IdentityTenantId</span><span class="sxs-lookup"><span data-stu-id="1595d-115">-IdentityTenantId</span></span>
<span data-ttu-id="1595d-116">Beállítja vagy beállítja a bérlőazonosítót.</span><span class="sxs-lookup"><span data-stu-id="1595d-116">Gets or sets the tenant id.</span></span>

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

### <span data-ttu-id="1595d-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="1595d-117">-IdentityType</span></span>
<span data-ttu-id="1595d-118">Az erőforrás-mover szolgáltatáshoz használt identitás típusa.</span><span class="sxs-lookup"><span data-stu-id="1595d-118">The type of identity used for the resource mover service.</span></span>

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

### <span data-ttu-id="1595d-119">-Location</span><span class="sxs-lookup"><span data-stu-id="1595d-119">-Location</span></span>
<span data-ttu-id="1595d-120">Az a földrajzi hely, ahol az erőforrás található.</span><span class="sxs-lookup"><span data-stu-id="1595d-120">The geo-location where the resource lives.</span></span>

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

### <span data-ttu-id="1595d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1595d-121">-Name</span></span>
<span data-ttu-id="1595d-122">A gyűjtemény neve.</span><span class="sxs-lookup"><span data-stu-id="1595d-122">The Move Collection Name.</span></span>

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

### <span data-ttu-id="1595d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1595d-123">-ResourceGroupName</span></span>
<span data-ttu-id="1595d-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1595d-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="1595d-125">-SourceRegion</span><span class="sxs-lookup"><span data-stu-id="1595d-125">-SourceRegion</span></span>
<span data-ttu-id="1595d-126">Beállítja vagy beállítja a forrás régióját.</span><span class="sxs-lookup"><span data-stu-id="1595d-126">Gets or sets the source region.</span></span>

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

### <span data-ttu-id="1595d-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1595d-127">-SubscriptionId</span></span>
<span data-ttu-id="1595d-128">Az előfizetés azonosítója.</span><span class="sxs-lookup"><span data-stu-id="1595d-128">The Subscription ID.</span></span>

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

### <span data-ttu-id="1595d-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="1595d-129">-Tag</span></span>
<span data-ttu-id="1595d-130">Erőforráscímkék.</span><span class="sxs-lookup"><span data-stu-id="1595d-130">Resource tags.</span></span>

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

### <span data-ttu-id="1595d-131">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="1595d-131">-TargetRegion</span></span>
<span data-ttu-id="1595d-132">Beállítja vagy beállítja a célterületet.</span><span class="sxs-lookup"><span data-stu-id="1595d-132">Gets or sets the target region.</span></span>

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

### <span data-ttu-id="1595d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1595d-133">-Confirm</span></span>
<span data-ttu-id="1595d-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1595d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1595d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1595d-135">-WhatIf</span></span>
<span data-ttu-id="1595d-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1595d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1595d-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1595d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1595d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1595d-138">CommonParameters</span></span>
<span data-ttu-id="1595d-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1595d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1595d-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1595d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1595d-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1595d-141">INPUTS</span></span>

## <span data-ttu-id="1595d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1595d-142">OUTPUTS</span></span>

### <span data-ttu-id="1595d-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span><span class="sxs-lookup"><span data-stu-id="1595d-143">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IMoveCollection</span></span>

## <span data-ttu-id="1595d-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1595d-144">NOTES</span></span>

<span data-ttu-id="1595d-145">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="1595d-145">ALIASES</span></span>

## <span data-ttu-id="1595d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1595d-146">RELATED LINKS</span></span>

