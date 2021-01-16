---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326937"
---
# <span data-ttu-id="5fd14-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="5fd14-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="5fd14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fd14-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd14-103">A társviszony-létesítéshez kapott útvonalakat sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="5fd14-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="5fd14-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5fd14-104">SYNTAX</span></span>

### <span data-ttu-id="5fd14-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5fd14-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5fd14-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5fd14-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fd14-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5fd14-107">DESCRIPTION</span></span>
<span data-ttu-id="5fd14-108">Társviszony-létesítésből kapott útvonalak listája</span><span class="sxs-lookup"><span data-stu-id="5fd14-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="5fd14-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5fd14-109">EXAMPLES</span></span>

### <span data-ttu-id="5fd14-110">List top 100 received routes for a peering</span><span class="sxs-lookup"><span data-stu-id="5fd14-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="5fd14-111">A társviszonyhoz kapott összes útvonal listája</span><span class="sxs-lookup"><span data-stu-id="5fd14-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="5fd14-112">Szűrés AS Path szerint</span><span class="sxs-lookup"><span data-stu-id="5fd14-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="5fd14-113">Egy társviszonyhoz kapott összes útvonal listája as szűrővel</span><span class="sxs-lookup"><span data-stu-id="5fd14-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="5fd14-114">Szűrés RPKIValidationState szerint</span><span class="sxs-lookup"><span data-stu-id="5fd14-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="5fd14-115">Egy társviszonyhoz kapott összes útvonal listája az RPKIValidationState szűrővel</span><span class="sxs-lookup"><span data-stu-id="5fd14-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="5fd14-116">Filter by OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="5fd14-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="5fd14-117">Egy társviszonyhoz kapott összes útvonal listája az OriginAsValidationState szűrővel</span><span class="sxs-lookup"><span data-stu-id="5fd14-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="5fd14-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fd14-118">PARAMETERS</span></span>

### <span data-ttu-id="5fd14-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="5fd14-119">-AsPath</span></span>
<span data-ttu-id="5fd14-120">Szűrés AS Path szerint.</span><span class="sxs-lookup"><span data-stu-id="5fd14-120">Filter by AS Path.</span></span>
<span data-ttu-id="5fd14-121">Például: '9342 1234 4567'</span><span class="sxs-lookup"><span data-stu-id="5fd14-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="5fd14-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd14-122">-DefaultProfile</span></span>
<span data-ttu-id="5fd14-123">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5fd14-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fd14-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5fd14-124">-Name</span></span>
<span data-ttu-id="5fd14-125">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="5fd14-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="5fd14-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="5fd14-126">-OriginAsValidationState</span></span>
<span data-ttu-id="5fd14-127">Szűrés forrás AS érvényességi állapota szerint</span><span class="sxs-lookup"><span data-stu-id="5fd14-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="5fd14-128">-Előtag</span><span class="sxs-lookup"><span data-stu-id="5fd14-128">-Prefix</span></span>
<span data-ttu-id="5fd14-129">Szűrés előtag alapján.</span><span class="sxs-lookup"><span data-stu-id="5fd14-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="5fd14-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd14-130">-ResourceGroupName</span></span>
<span data-ttu-id="5fd14-131">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="5fd14-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="5fd14-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fd14-132">-ResourceId</span></span>
<span data-ttu-id="5fd14-133">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="5fd14-133">The resource id string name.</span></span>

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

### <span data-ttu-id="5fd14-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="5fd14-134">-RPKIValidationState</span></span>
<span data-ttu-id="5fd14-135">Szűrés RPKI-érvényesítési állapot szerint.</span><span class="sxs-lookup"><span data-stu-id="5fd14-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="5fd14-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd14-136">CommonParameters</span></span>
<span data-ttu-id="5fd14-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fd14-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd14-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fd14-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd14-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fd14-139">INPUTS</span></span>

### <span data-ttu-id="5fd14-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5fd14-140">System.String</span></span>

## <span data-ttu-id="5fd14-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5fd14-141">OUTPUTS</span></span>

### <span data-ttu-id="5fd14-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="5fd14-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="5fd14-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5fd14-143">NOTES</span></span>

## <span data-ttu-id="5fd14-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5fd14-144">RELATED LINKS</span></span>
