---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186380"
---
# <span data-ttu-id="91c92-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="91c92-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="91c92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="91c92-102">SYNOPSIS</span></span>
<span data-ttu-id="91c92-103">A levelezéshez regisztrált előtagot kapja vagy sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="91c92-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="91c92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="91c92-104">SYNTAX</span></span>

### <span data-ttu-id="91c92-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="91c92-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91c92-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="91c92-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91c92-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91c92-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91c92-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="91c92-108">DESCRIPTION</span></span>
<span data-ttu-id="91c92-109">A levelezéshez regisztrált előtagot kapja vagy sorolja fel.</span><span class="sxs-lookup"><span data-stu-id="91c92-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="91c92-110">Példák</span><span class="sxs-lookup"><span data-stu-id="91c92-110">EXAMPLES</span></span>

### <span data-ttu-id="91c92-111">A ASN regisztrált partnerek listája</span><span class="sxs-lookup"><span data-stu-id="91c92-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="91c92-112">Nyilvántartott ASN-es listák.</span><span class="sxs-lookup"><span data-stu-id="91c92-112">Lists registered asn.</span></span>

### <span data-ttu-id="91c92-113">Regisztrált ASN-t kap a partnerek számára név szerint</span><span class="sxs-lookup"><span data-stu-id="91c92-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="91c92-114">Az ASN-t regisztrált társközi kapja.</span><span class="sxs-lookup"><span data-stu-id="91c92-114">Gets registered peering asn.</span></span>

<span data-ttu-id="91c92-115">{{A példa leírása itt}}</span><span class="sxs-lookup"><span data-stu-id="91c92-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="91c92-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="91c92-116">PARAMETERS</span></span>

### <span data-ttu-id="91c92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c92-117">-DefaultProfile</span></span>
<span data-ttu-id="91c92-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="91c92-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91c92-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91c92-119">-InputObject</span></span>
<span data-ttu-id="91c92-120">Get-AzPeering használata</span><span class="sxs-lookup"><span data-stu-id="91c92-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="91c92-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="91c92-121">-Name</span></span>
<span data-ttu-id="91c92-122">Az előtag neve.</span><span class="sxs-lookup"><span data-stu-id="91c92-122">The name of prefix.</span></span>

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

### <span data-ttu-id="91c92-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="91c92-123">-PeeringName</span></span>
<span data-ttu-id="91c92-124">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="91c92-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="91c92-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c92-125">-ResourceGroupName</span></span>
<span data-ttu-id="91c92-126">A meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="91c92-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="91c92-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91c92-127">-ResourceId</span></span>
<span data-ttu-id="91c92-128">Az erőforrás-azonosító karakterlánc neve.</span><span class="sxs-lookup"><span data-stu-id="91c92-128">The resource id string name.</span></span>

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

### <span data-ttu-id="91c92-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c92-129">CommonParameters</span></span>
<span data-ttu-id="91c92-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="91c92-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c92-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="91c92-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c92-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="91c92-132">INPUTS</span></span>

### <span data-ttu-id="91c92-133">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="91c92-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="91c92-134">System. String</span><span class="sxs-lookup"><span data-stu-id="91c92-134">System.String</span></span>

## <span data-ttu-id="91c92-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="91c92-135">OUTPUTS</span></span>

### <span data-ttu-id="91c92-136">Microsoft. Azure. PowerShell. parancsmagok. társközi. models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="91c92-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="91c92-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="91c92-137">NOTES</span></span>

## <span data-ttu-id="91c92-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="91c92-138">RELATED LINKS</span></span>