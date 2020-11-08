---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184719"
---
# <span data-ttu-id="db687-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="db687-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="db687-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="db687-102">SYNOPSIS</span></span>
<span data-ttu-id="db687-103">Nyilvántartott ASN-et állít be vagy frissít a fölérendelt társközi erőforrásból.</span><span class="sxs-lookup"><span data-stu-id="db687-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="db687-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="db687-104">SYNTAX</span></span>

### <span data-ttu-id="db687-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="db687-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db687-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="db687-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db687-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="db687-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db687-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="db687-108">DESCRIPTION</span></span>
<span data-ttu-id="db687-109">Lehetővé teszi a bejegyzett ASN-nek a fölérendelt társközi erőforrásból való frissítését.</span><span class="sxs-lookup"><span data-stu-id="db687-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="db687-110">Példák</span><span class="sxs-lookup"><span data-stu-id="db687-110">EXAMPLES</span></span>

### <span data-ttu-id="db687-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="db687-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="db687-112">Frissíti az ASN-t erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="db687-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="db687-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="db687-113">PARAMETERS</span></span>

### <span data-ttu-id="db687-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db687-114">-AsJob</span></span>
<span data-ttu-id="db687-115">Fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="db687-115">Run in the background.</span></span>

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

### <span data-ttu-id="db687-116">-ASN</span><span class="sxs-lookup"><span data-stu-id="db687-116">-Asn</span></span>
<span data-ttu-id="db687-117">A regisztrálni kívánt ASN</span><span class="sxs-lookup"><span data-stu-id="db687-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="db687-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db687-118">-DefaultProfile</span></span>
<span data-ttu-id="db687-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="db687-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db687-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db687-120">-InputObject</span></span>
<span data-ttu-id="db687-121">Get-AzPeering használata</span><span class="sxs-lookup"><span data-stu-id="db687-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="db687-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="db687-122">-Name</span></span>
<span data-ttu-id="db687-123">A regisztrálni kívánt ASN</span><span class="sxs-lookup"><span data-stu-id="db687-123">The ASN to be registered</span></span>

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

### <span data-ttu-id="db687-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="db687-124">-PeeringName</span></span>
<span data-ttu-id="db687-125">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="db687-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="db687-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db687-126">-ResourceGroupName</span></span>
<span data-ttu-id="db687-127">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="db687-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="db687-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db687-128">-ResourceId</span></span>
<span data-ttu-id="db687-129">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="db687-129">The resource id string name.</span></span>

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

### <span data-ttu-id="db687-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="db687-130">-Confirm</span></span>
<span data-ttu-id="db687-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="db687-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db687-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db687-132">-WhatIf</span></span>
<span data-ttu-id="db687-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="db687-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db687-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="db687-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db687-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db687-135">CommonParameters</span></span>
<span data-ttu-id="db687-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="db687-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db687-137">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="db687-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db687-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="db687-138">INPUTS</span></span>

### <span data-ttu-id="db687-139">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="db687-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="db687-140">System. String</span><span class="sxs-lookup"><span data-stu-id="db687-140">System.String</span></span>

## <span data-ttu-id="db687-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="db687-141">OUTPUTS</span></span>

### <span data-ttu-id="db687-142">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="db687-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="db687-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="db687-143">NOTES</span></span>

## <span data-ttu-id="db687-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="db687-144">RELATED LINKS</span></span>
