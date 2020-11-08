---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184297"
---
# <span data-ttu-id="1ccd6-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="1ccd6-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="1ccd6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ccd6-102">SYNOPSIS</span></span>
<span data-ttu-id="1ccd6-103">Beolvassa a regisztrált ASN-t az internetes Exchange-kiszolgálók típusának egyszemélyes átirányításához.</span><span class="sxs-lookup"><span data-stu-id="1ccd6-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="1ccd6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ccd6-104">SYNTAX</span></span>

### <span data-ttu-id="1ccd6-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ccd6-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ccd6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1ccd6-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ccd6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ccd6-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ccd6-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ccd6-108">DESCRIPTION</span></span>
<span data-ttu-id="1ccd6-109">Regisztrált ASN beszerzése vagy listázása</span><span class="sxs-lookup"><span data-stu-id="1ccd6-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="1ccd6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1ccd6-110">EXAMPLES</span></span>

### <span data-ttu-id="1ccd6-111">A ASN regisztrált partnerek listája</span><span class="sxs-lookup"><span data-stu-id="1ccd6-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="1ccd6-112">Nyilvántartott ASN-es listák.</span><span class="sxs-lookup"><span data-stu-id="1ccd6-112">Lists registered asn.</span></span>

### <span data-ttu-id="1ccd6-113">Regisztrált ASN-t kap a partnerek számára név szerint</span><span class="sxs-lookup"><span data-stu-id="1ccd6-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="1ccd6-114">Az ASN-t regisztrált társközi kapja.</span><span class="sxs-lookup"><span data-stu-id="1ccd6-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="1ccd6-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ccd6-115">PARAMETERS</span></span>

### <span data-ttu-id="1ccd6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ccd6-116">-DefaultProfile</span></span>
<span data-ttu-id="1ccd6-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ccd6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ccd6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ccd6-118">-InputObject</span></span>
<span data-ttu-id="1ccd6-119">Get-AzPeering használata</span><span class="sxs-lookup"><span data-stu-id="1ccd6-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="1ccd6-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ccd6-120">-Name</span></span>
<span data-ttu-id="1ccd6-121">A regisztrált ASN-név</span><span class="sxs-lookup"><span data-stu-id="1ccd6-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="1ccd6-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="1ccd6-122">-PeeringName</span></span>
<span data-ttu-id="1ccd6-123">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="1ccd6-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="1ccd6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ccd6-124">-ResourceGroupName</span></span>
<span data-ttu-id="1ccd6-125">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="1ccd6-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="1ccd6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ccd6-126">-ResourceId</span></span>
<span data-ttu-id="1ccd6-127">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="1ccd6-127">The resource id string name.</span></span>

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

### <span data-ttu-id="1ccd6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ccd6-128">CommonParameters</span></span>
<span data-ttu-id="1ccd6-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ccd6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ccd6-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1ccd6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ccd6-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ccd6-131">INPUTS</span></span>

### <span data-ttu-id="1ccd6-132">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="1ccd6-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="1ccd6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1ccd6-133">System.String</span></span>

## <span data-ttu-id="1ccd6-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ccd6-134">OUTPUTS</span></span>

### <span data-ttu-id="1ccd6-135">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="1ccd6-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="1ccd6-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ccd6-136">NOTES</span></span>

## <span data-ttu-id="1ccd6-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ccd6-137">RELATED LINKS</span></span>
