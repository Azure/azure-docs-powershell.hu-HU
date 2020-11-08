---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024507"
---
# <span data-ttu-id="82ea7-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="82ea7-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="82ea7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82ea7-102">SYNOPSIS</span></span>
<span data-ttu-id="82ea7-103">Regisztrált ASN létrehozása a kortársak számára</span><span class="sxs-lookup"><span data-stu-id="82ea7-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="82ea7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82ea7-104">SYNTAX</span></span>

### <span data-ttu-id="82ea7-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="82ea7-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ea7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="82ea7-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82ea7-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="82ea7-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82ea7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="82ea7-108">DESCRIPTION</span></span>
<span data-ttu-id="82ea7-109">Hozzon létre regisztrált ASN a társközi objektumokhoz.</span><span class="sxs-lookup"><span data-stu-id="82ea7-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="82ea7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="82ea7-110">EXAMPLES</span></span>

### <span data-ttu-id="82ea7-111">A személyes használat és a regisztrált ASN létrehozása</span><span class="sxs-lookup"><span data-stu-id="82ea7-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="82ea7-112">Szerezzen be egy olyan munkatársat, aki regisztrált ASN-t szeretne felvenni.</span><span class="sxs-lookup"><span data-stu-id="82ea7-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="82ea7-113">Ezután adja át a parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="82ea7-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="82ea7-114">Regisztrált ASN-resourceId létrehozása a társközi használattal</span><span class="sxs-lookup"><span data-stu-id="82ea7-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="82ea7-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82ea7-115">PARAMETERS</span></span>

### <span data-ttu-id="82ea7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82ea7-116">-AsJob</span></span>
<span data-ttu-id="82ea7-117">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="82ea7-117">Run in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-118">-ASN</span><span class="sxs-lookup"><span data-stu-id="82ea7-118">-Asn</span></span>
<span data-ttu-id="82ea7-119">A regisztrálni kívánt ASN</span><span class="sxs-lookup"><span data-stu-id="82ea7-119">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82ea7-120">-DefaultProfile</span></span>
<span data-ttu-id="82ea7-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="82ea7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82ea7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82ea7-122">-InputObject</span></span>
<span data-ttu-id="82ea7-123">Get-AzPeering használata</span><span class="sxs-lookup"><span data-stu-id="82ea7-123">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="82ea7-124">-Name</span></span>
<span data-ttu-id="82ea7-125">A regisztrálni kívánt ASN</span><span class="sxs-lookup"><span data-stu-id="82ea7-125">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="82ea7-126">-PeeringName</span></span>
<span data-ttu-id="82ea7-127">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="82ea7-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82ea7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82ea7-128">-ResourceGroupName</span></span>
<span data-ttu-id="82ea7-129">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="82ea7-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="82ea7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82ea7-130">-ResourceId</span></span>
<span data-ttu-id="82ea7-131">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="82ea7-131">The resource id string name.</span></span>

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

### <span data-ttu-id="82ea7-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="82ea7-132">-Confirm</span></span>
<span data-ttu-id="82ea7-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="82ea7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82ea7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82ea7-134">-WhatIf</span></span>
<span data-ttu-id="82ea7-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="82ea7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82ea7-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="82ea7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82ea7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82ea7-137">CommonParameters</span></span>
<span data-ttu-id="82ea7-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82ea7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82ea7-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="82ea7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82ea7-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82ea7-140">INPUTS</span></span>

### <span data-ttu-id="82ea7-141">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="82ea7-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="82ea7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="82ea7-142">System.String</span></span>

## <span data-ttu-id="82ea7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82ea7-143">OUTPUTS</span></span>

### <span data-ttu-id="82ea7-144">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="82ea7-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="82ea7-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82ea7-145">NOTES</span></span>

## <span data-ttu-id="82ea7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82ea7-146">RELATED LINKS</span></span>
