---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302675"
---
# <span data-ttu-id="fe18f-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="fe18f-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="fe18f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe18f-102">SYNOPSIS</span></span>
<span data-ttu-id="fe18f-103">Nyilvántartott ASN-et állít be vagy frissít a fölérendelt társközi erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="fe18f-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="fe18f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe18f-104">SYNTAX</span></span>

### <span data-ttu-id="fe18f-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fe18f-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe18f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fe18f-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe18f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fe18f-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe18f-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe18f-108">DESCRIPTION</span></span>
<span data-ttu-id="fe18f-109">Lehetővé teszi a bejegyzett ASN-nek a fölérendelt társközi erőforrásból való frissítését.</span><span class="sxs-lookup"><span data-stu-id="fe18f-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="fe18f-110">Példák</span><span class="sxs-lookup"><span data-stu-id="fe18f-110">EXAMPLES</span></span>

### <span data-ttu-id="fe18f-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fe18f-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="fe18f-112">Frissíti az ASN-t erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="fe18f-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="fe18f-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe18f-113">PARAMETERS</span></span>

### <span data-ttu-id="fe18f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe18f-114">-AsJob</span></span>
<span data-ttu-id="fe18f-115">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="fe18f-115">Run in the background.</span></span>

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

### <span data-ttu-id="fe18f-116">-ASN</span><span class="sxs-lookup"><span data-stu-id="fe18f-116">-Asn</span></span>
<span data-ttu-id="fe18f-117">A regisztrálni kívánt ASN</span><span class="sxs-lookup"><span data-stu-id="fe18f-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="fe18f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe18f-118">-DefaultProfile</span></span>
<span data-ttu-id="fe18f-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fe18f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe18f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe18f-120">-InputObject</span></span>
<span data-ttu-id="fe18f-121">Get-AzPeering használata</span><span class="sxs-lookup"><span data-stu-id="fe18f-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe18f-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fe18f-122">-Name</span></span>
<span data-ttu-id="fe18f-123">A regisztrálni kívánt ASN</span><span class="sxs-lookup"><span data-stu-id="fe18f-123">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe18f-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="fe18f-124">-PeeringName</span></span>
<span data-ttu-id="fe18f-125">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="fe18f-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="fe18f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe18f-126">-ResourceGroupName</span></span>
<span data-ttu-id="fe18f-127">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="fe18f-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="fe18f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe18f-128">-ResourceId</span></span>
<span data-ttu-id="fe18f-129">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="fe18f-129">The resource id string name.</span></span>

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

### <span data-ttu-id="fe18f-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fe18f-130">-Confirm</span></span>
<span data-ttu-id="fe18f-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fe18f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe18f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe18f-132">-WhatIf</span></span>
<span data-ttu-id="fe18f-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fe18f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe18f-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fe18f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe18f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe18f-135">CommonParameters</span></span>
<span data-ttu-id="fe18f-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe18f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe18f-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fe18f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe18f-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe18f-138">INPUTS</span></span>

### <span data-ttu-id="fe18f-139">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="fe18f-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="fe18f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fe18f-140">System.String</span></span>

## <span data-ttu-id="fe18f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe18f-141">OUTPUTS</span></span>

### <span data-ttu-id="fe18f-142">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="fe18f-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="fe18f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe18f-143">NOTES</span></span>

## <span data-ttu-id="fe18f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe18f-144">RELATED LINKS</span></span>
