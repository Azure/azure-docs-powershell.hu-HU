---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d23a034b2c51f37116c605d786393ba504da3f26
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169522"
---
# <span data-ttu-id="6e6bb-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="6e6bb-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="6e6bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="6e6bb-103">Az internetes exchange-útválasztási kiszolgáló típusú társviszonyok regisztrált ASN-ét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6e6bb-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="6e6bb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6e6bb-104">SYNTAX</span></span>

### <span data-ttu-id="6e6bb-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6e6bb-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e6bb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6e6bb-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e6bb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e6bb-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e6bb-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6e6bb-108">DESCRIPTION</span></span>
<span data-ttu-id="6e6bb-109">Regisztrált asn-név be- vagy felsorolása.</span><span class="sxs-lookup"><span data-stu-id="6e6bb-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="6e6bb-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6e6bb-110">EXAMPLES</span></span>

### <span data-ttu-id="6e6bb-111">Regisztrált ASN-ek listája társviszonyhoz</span><span class="sxs-lookup"><span data-stu-id="6e6bb-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="6e6bb-112">A regisztrált asn listák.</span><span class="sxs-lookup"><span data-stu-id="6e6bb-112">Lists registered asn.</span></span>

### <span data-ttu-id="6e6bb-113">Név szerint regisztrált ASN-t kap a társviszonyhoz</span><span class="sxs-lookup"><span data-stu-id="6e6bb-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="6e6bb-114">Regisztrálja a társviszony-létesítés asn-ját.</span><span class="sxs-lookup"><span data-stu-id="6e6bb-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="6e6bb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e6bb-115">PARAMETERS</span></span>

### <span data-ttu-id="6e6bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e6bb-116">-DefaultProfile</span></span>
<span data-ttu-id="6e6bb-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e6bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e6bb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e6bb-118">-InputObject</span></span>
<span data-ttu-id="6e6bb-119">A Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="6e6bb-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="6e6bb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6e6bb-120">-Name</span></span>
<span data-ttu-id="6e6bb-121">A regisztrált ASN neve</span><span class="sxs-lookup"><span data-stu-id="6e6bb-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="6e6bb-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="6e6bb-122">-PeeringName</span></span>
<span data-ttu-id="6e6bb-123">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="6e6bb-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="6e6bb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e6bb-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e6bb-125">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="6e6bb-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="6e6bb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e6bb-126">-ResourceId</span></span>
<span data-ttu-id="6e6bb-127">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="6e6bb-127">The resource id string name.</span></span>

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

### <span data-ttu-id="6e6bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e6bb-128">CommonParameters</span></span>
<span data-ttu-id="6e6bb-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e6bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e6bb-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e6bb-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e6bb-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e6bb-131">INPUTS</span></span>

### <span data-ttu-id="6e6bb-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="6e6bb-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="6e6bb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6e6bb-133">System.String</span></span>

## <span data-ttu-id="6e6bb-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e6bb-134">OUTPUTS</span></span>

### <span data-ttu-id="6e6bb-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="6e6bb-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="6e6bb-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6e6bb-136">NOTES</span></span>

## <span data-ttu-id="6e6bb-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e6bb-137">RELATED LINKS</span></span>
