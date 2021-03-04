---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: e5f961b5bd3acc1db716d68f43147e1a6c5611f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937785"
---
# <span data-ttu-id="ae30a-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="ae30a-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="ae30a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae30a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae30a-103">A társviszony-létesítéshez kapott útvonalakat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="ae30a-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="ae30a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ae30a-104">SYNTAX</span></span>

### <span data-ttu-id="ae30a-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ae30a-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae30a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae30a-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae30a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ae30a-107">DESCRIPTION</span></span>
<span data-ttu-id="ae30a-108">Társviszony-létesítésből kapott útvonalak listája</span><span class="sxs-lookup"><span data-stu-id="ae30a-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="ae30a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ae30a-109">EXAMPLES</span></span>

### <span data-ttu-id="ae30a-110">List top 100 received routes for a peering</span><span class="sxs-lookup"><span data-stu-id="ae30a-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="ae30a-111">A társviszonyhoz kapott összes útvonal listája</span><span class="sxs-lookup"><span data-stu-id="ae30a-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="ae30a-112">Szűrés AS Path szerint</span><span class="sxs-lookup"><span data-stu-id="ae30a-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="ae30a-113">Egy társviszonyhoz kapott összes útvonal listája as szűrővel</span><span class="sxs-lookup"><span data-stu-id="ae30a-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="ae30a-114">Szűrés RPKIValidationState szerint</span><span class="sxs-lookup"><span data-stu-id="ae30a-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="ae30a-115">Egy társviszonyhoz kapott összes útvonal listája az RPKIValidationState szűrővel</span><span class="sxs-lookup"><span data-stu-id="ae30a-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="ae30a-116">Filter by OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="ae30a-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="ae30a-117">Egy társviszonyhoz kapott összes útvonal listája az OriginAsValidationState szűrővel</span><span class="sxs-lookup"><span data-stu-id="ae30a-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="ae30a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae30a-118">PARAMETERS</span></span>

### <span data-ttu-id="ae30a-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="ae30a-119">-AsPath</span></span>
<span data-ttu-id="ae30a-120">Szűrés AS Path szerint.</span><span class="sxs-lookup"><span data-stu-id="ae30a-120">Filter by AS Path.</span></span>
<span data-ttu-id="ae30a-121">Például: '9342 1234 4567'</span><span class="sxs-lookup"><span data-stu-id="ae30a-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="ae30a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae30a-122">-DefaultProfile</span></span>
<span data-ttu-id="ae30a-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ae30a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae30a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ae30a-124">-Name</span></span>
<span data-ttu-id="ae30a-125">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="ae30a-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae30a-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="ae30a-126">-OriginAsValidationState</span></span>
<span data-ttu-id="ae30a-127">Szűrés forrás AS érvényességi állapota szerint</span><span class="sxs-lookup"><span data-stu-id="ae30a-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="ae30a-128">-Előtag</span><span class="sxs-lookup"><span data-stu-id="ae30a-128">-Prefix</span></span>
<span data-ttu-id="ae30a-129">Szűrés előtag alapján.</span><span class="sxs-lookup"><span data-stu-id="ae30a-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="ae30a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae30a-130">-ResourceGroupName</span></span>
<span data-ttu-id="ae30a-131">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="ae30a-131">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae30a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae30a-132">-ResourceId</span></span>
<span data-ttu-id="ae30a-133">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="ae30a-133">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae30a-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="ae30a-134">-RPKIValidationState</span></span>
<span data-ttu-id="ae30a-135">Szűrés RPKI-érvényesítési állapot szerint.</span><span class="sxs-lookup"><span data-stu-id="ae30a-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="ae30a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae30a-136">CommonParameters</span></span>
<span data-ttu-id="ae30a-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae30a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae30a-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae30a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae30a-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae30a-139">INPUTS</span></span>

### <span data-ttu-id="ae30a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ae30a-140">System.String</span></span>

## <span data-ttu-id="ae30a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ae30a-141">OUTPUTS</span></span>

### <span data-ttu-id="ae30a-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="ae30a-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="ae30a-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ae30a-143">NOTES</span></span>

## <span data-ttu-id="ae30a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ae30a-144">RELATED LINKS</span></span>
