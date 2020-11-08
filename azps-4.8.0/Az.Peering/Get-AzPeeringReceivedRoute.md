---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringreceivedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringReceivedRoute.md
ms.openlocfilehash: 14557809041fc6f4268dbe28ad9d8f13a70e4054
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184299"
---
# <span data-ttu-id="3c991-101">Get-AzPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="3c991-101">Get-AzPeeringReceivedRoute</span></span>

## <span data-ttu-id="3c991-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c991-102">SYNOPSIS</span></span>
<span data-ttu-id="3c991-103">A beérkezett útvonalak listáját jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="3c991-103">Lists the received routes for a Peering.</span></span>

## <span data-ttu-id="3c991-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c991-104">SYNTAX</span></span>

### <span data-ttu-id="3c991-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c991-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceGroupName] <String> -Name <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c991-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c991-106">ByResourceId</span></span>
```
Get-AzPeeringReceivedRoute [-ResourceId] <String> [-Prefix <String>] [-AsPath <String>]
 [-OriginAsValidationState <String>] [-RPKIValidationState <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c991-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c991-107">DESCRIPTION</span></span>
<span data-ttu-id="3c991-108">A partnerektől kapott útvonalak listája</span><span class="sxs-lookup"><span data-stu-id="3c991-108">Lists recieved routes from a Peering</span></span>

## <span data-ttu-id="3c991-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3c991-109">EXAMPLES</span></span>

### <span data-ttu-id="3c991-110">A lista felső 100-beli útvonalainak átvétele</span><span class="sxs-lookup"><span data-stu-id="3c991-110">List top 100 received routes for a peering</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName
```

<span data-ttu-id="3c991-111">A beérkezett összes útvonal listázása egy társközi verzióban</span><span class="sxs-lookup"><span data-stu-id="3c991-111">Lists all of the received routes for a peering</span></span>

### <span data-ttu-id="3c991-112">Szűrés elérési út szerint</span><span class="sxs-lookup"><span data-stu-id="3c991-112">Filter by AS Path</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -AsPath "1234 5674 9834"
```

<span data-ttu-id="3c991-113">Az összes beérkezett útvonal felsorolása egy, a szűrővel rendelkező partnerhez</span><span class="sxs-lookup"><span data-stu-id="3c991-113">Lists all of the received routes for a peering with a filter on AS</span></span> 

### <span data-ttu-id="3c991-114">Szűrés RPKIValidationState szerint</span><span class="sxs-lookup"><span data-stu-id="3c991-114">Filter by RPKIValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -RPKIValidationState "Valid"
```

<span data-ttu-id="3c991-115">Az összes fogadott útvonal listája a RPKIValidationState szűrővel rendelkező partnerek számára</span><span class="sxs-lookup"><span data-stu-id="3c991-115">Lists all of the received routes for a peering with a filter on RPKIValidationState</span></span>

### <span data-ttu-id="3c991-116">Szűrés OriginAsValidationState szerint</span><span class="sxs-lookup"><span data-stu-id="3c991-116">Filter by OriginAsValidationState</span></span>
```powershell
PS C:\> Get-AzPeeringReceivedRoute -ResourceGroupName $resourceGroupName -Name $peeringName -OriginAsValidationState "Valid"
```

<span data-ttu-id="3c991-117">Az összes fogadott útvonal listája a OriginAsValidationState szűrővel rendelkező partnerek számára</span><span class="sxs-lookup"><span data-stu-id="3c991-117">Lists all of the received routes for a peering with a filter on OriginAsValidationState</span></span>

## <span data-ttu-id="3c991-118">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c991-118">PARAMETERS</span></span>

### <span data-ttu-id="3c991-119">-AsPath</span><span class="sxs-lookup"><span data-stu-id="3c991-119">-AsPath</span></span>
<span data-ttu-id="3c991-120">Szűrés útvonal szerint</span><span class="sxs-lookup"><span data-stu-id="3c991-120">Filter by AS Path.</span></span>
<span data-ttu-id="3c991-121">Példa: "9342 1234 4567"</span><span class="sxs-lookup"><span data-stu-id="3c991-121">Example: '9342 1234 4567'</span></span>

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

### <span data-ttu-id="3c991-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c991-122">-DefaultProfile</span></span>
<span data-ttu-id="3c991-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c991-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c991-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3c991-124">-Name</span></span>
<span data-ttu-id="3c991-125">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="3c991-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="3c991-126">-OriginAsValidationState</span><span class="sxs-lookup"><span data-stu-id="3c991-126">-OriginAsValidationState</span></span>
<span data-ttu-id="3c991-127">Szűrés eredet szerint érvényesítési állapotban</span><span class="sxs-lookup"><span data-stu-id="3c991-127">Filter by origin AS validation state.</span></span>

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

### <span data-ttu-id="3c991-128">-Prefix</span><span class="sxs-lookup"><span data-stu-id="3c991-128">-Prefix</span></span>
<span data-ttu-id="3c991-129">Szűrés előtag szerint</span><span class="sxs-lookup"><span data-stu-id="3c991-129">Filter by prefix.</span></span>

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

### <span data-ttu-id="3c991-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c991-130">-ResourceGroupName</span></span>
<span data-ttu-id="3c991-131">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="3c991-131">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="3c991-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c991-132">-ResourceId</span></span>
<span data-ttu-id="3c991-133">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="3c991-133">The resource id string name.</span></span>

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

### <span data-ttu-id="3c991-134">-RPKIValidationState</span><span class="sxs-lookup"><span data-stu-id="3c991-134">-RPKIValidationState</span></span>
<span data-ttu-id="3c991-135">Szűrés RPKI érvényesítési állapottal.</span><span class="sxs-lookup"><span data-stu-id="3c991-135">Filter by RPKI validation state.</span></span>

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

### <span data-ttu-id="3c991-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c991-136">CommonParameters</span></span>
<span data-ttu-id="3c991-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c991-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c991-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3c991-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c991-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c991-139">INPUTS</span></span>

### <span data-ttu-id="3c991-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3c991-140">System.String</span></span>

## <span data-ttu-id="3c991-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c991-141">OUTPUTS</span></span>

### <span data-ttu-id="3c991-142">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringReceivedRoute</span><span class="sxs-lookup"><span data-stu-id="3c991-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringReceivedRoute</span></span>

## <span data-ttu-id="3c991-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c991-143">NOTES</span></span>

## <span data-ttu-id="3c991-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c991-144">RELATED LINKS</span></span>
