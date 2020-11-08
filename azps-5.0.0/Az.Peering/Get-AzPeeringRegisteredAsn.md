---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186381"
---
# <span data-ttu-id="cf32b-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="cf32b-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="cf32b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf32b-102">SYNOPSIS</span></span>
<span data-ttu-id="cf32b-103">Beolvassa a regisztrált ASN-t az internetes Exchange-kiszolgálók típusának egyszemélyes átirányításához.</span><span class="sxs-lookup"><span data-stu-id="cf32b-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="cf32b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf32b-104">SYNTAX</span></span>

### <span data-ttu-id="cf32b-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf32b-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf32b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cf32b-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf32b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf32b-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cf32b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf32b-108">DESCRIPTION</span></span>
<span data-ttu-id="cf32b-109">Regisztrált ASN beszerzése vagy listázása</span><span class="sxs-lookup"><span data-stu-id="cf32b-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="cf32b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cf32b-110">EXAMPLES</span></span>

### <span data-ttu-id="cf32b-111">A ASN regisztrált partnerek listája</span><span class="sxs-lookup"><span data-stu-id="cf32b-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="cf32b-112">Nyilvántartott ASN-es listák.</span><span class="sxs-lookup"><span data-stu-id="cf32b-112">Lists registered asn.</span></span>

### <span data-ttu-id="cf32b-113">Regisztrált ASN-t kap a partnerek számára név szerint</span><span class="sxs-lookup"><span data-stu-id="cf32b-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="cf32b-114">Az ASN-t regisztrált társközi kapja.</span><span class="sxs-lookup"><span data-stu-id="cf32b-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="cf32b-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf32b-115">PARAMETERS</span></span>

### <span data-ttu-id="cf32b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf32b-116">-DefaultProfile</span></span>
<span data-ttu-id="cf32b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf32b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf32b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf32b-118">-InputObject</span></span>
<span data-ttu-id="cf32b-119">Get-AzPeering használata</span><span class="sxs-lookup"><span data-stu-id="cf32b-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf32b-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf32b-120">-Name</span></span>
<span data-ttu-id="cf32b-121">A regisztrált ASN-név</span><span class="sxs-lookup"><span data-stu-id="cf32b-121">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf32b-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="cf32b-122">-PeeringName</span></span>
<span data-ttu-id="cf32b-123">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="cf32b-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="cf32b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf32b-124">-ResourceGroupName</span></span>
<span data-ttu-id="cf32b-125">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="cf32b-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="cf32b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf32b-126">-ResourceId</span></span>
<span data-ttu-id="cf32b-127">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="cf32b-127">The resource id string name.</span></span>

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

### <span data-ttu-id="cf32b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf32b-128">CommonParameters</span></span>
<span data-ttu-id="cf32b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf32b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf32b-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cf32b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf32b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf32b-131">INPUTS</span></span>

### <span data-ttu-id="cf32b-132">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="cf32b-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="cf32b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cf32b-133">System.String</span></span>

## <span data-ttu-id="cf32b-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf32b-134">OUTPUTS</span></span>

### <span data-ttu-id="cf32b-135">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="cf32b-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="cf32b-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf32b-136">NOTES</span></span>

## <span data-ttu-id="cf32b-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf32b-137">RELATED LINKS</span></span>
