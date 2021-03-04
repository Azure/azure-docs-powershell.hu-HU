---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredAsn.md
ms.openlocfilehash: 4218dd5441c4f580c89d770556f2d5c329cfd06c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937777"
---
# <span data-ttu-id="c1268-101">Get-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="c1268-101">Get-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="c1268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1268-102">SYNOPSIS</span></span>
<span data-ttu-id="c1268-103">Az internetes exchange-útválasztási kiszolgáló típusú társviszonyok regisztrált ASN-ét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c1268-103">Gets the registered ASN for internet exchange route server type peerings.</span></span>

## <span data-ttu-id="c1268-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c1268-104">SYNTAX</span></span>

### <span data-ttu-id="c1268-105">ByResourceGroupAndName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c1268-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1268-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c1268-106">InputObject</span></span>
```
Get-AzPeeringRegisteredAsn [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1268-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1268-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredAsn [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1268-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c1268-108">DESCRIPTION</span></span>
<span data-ttu-id="c1268-109">Regisztrált asn-név be- vagy felsorolása.</span><span class="sxs-lookup"><span data-stu-id="c1268-109">Get or list a registered ASN.</span></span>

## <span data-ttu-id="c1268-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c1268-110">EXAMPLES</span></span>

### <span data-ttu-id="c1268-111">Regisztrált ASN-ek listája társviszonyhoz</span><span class="sxs-lookup"><span data-stu-id="c1268-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="c1268-112">A regisztrált asn listák.</span><span class="sxs-lookup"><span data-stu-id="c1268-112">Lists registered asn.</span></span>

### <span data-ttu-id="c1268-113">Név szerint regisztrált ASN-t kap a társviszonyhoz</span><span class="sxs-lookup"><span data-stu-id="c1268-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredAsn -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredAsnName
```

<span data-ttu-id="c1268-114">Regisztrálja a társviszony-létesítés asn-ját.</span><span class="sxs-lookup"><span data-stu-id="c1268-114">Gets registered peering asn.</span></span>

## <span data-ttu-id="c1268-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1268-115">PARAMETERS</span></span>

### <span data-ttu-id="c1268-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1268-116">-DefaultProfile</span></span>
<span data-ttu-id="c1268-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c1268-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1268-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1268-118">-InputObject</span></span>
<span data-ttu-id="c1268-119">A Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="c1268-119">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="c1268-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c1268-120">-Name</span></span>
<span data-ttu-id="c1268-121">A regisztrált ASN neve</span><span class="sxs-lookup"><span data-stu-id="c1268-121">The name of the registered ASN</span></span>

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

### <span data-ttu-id="c1268-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="c1268-122">-PeeringName</span></span>
<span data-ttu-id="c1268-123">A PSPeering egyedi neve.</span><span class="sxs-lookup"><span data-stu-id="c1268-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="c1268-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1268-124">-ResourceGroupName</span></span>
<span data-ttu-id="c1268-125">Meglévő erőforráscsoport nevének létrehozása vagy használata.</span><span class="sxs-lookup"><span data-stu-id="c1268-125">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="c1268-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1268-126">-ResourceId</span></span>
<span data-ttu-id="c1268-127">Az erőforrás-azonosító karakterláncának neve.</span><span class="sxs-lookup"><span data-stu-id="c1268-127">The resource id string name.</span></span>

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

### <span data-ttu-id="c1268-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1268-128">CommonParameters</span></span>
<span data-ttu-id="c1268-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1268-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1268-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1268-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1268-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1268-131">INPUTS</span></span>

### <span data-ttu-id="c1268-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="c1268-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="c1268-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c1268-133">System.String</span></span>

## <span data-ttu-id="c1268-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c1268-134">OUTPUTS</span></span>

### <span data-ttu-id="c1268-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="c1268-135">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="c1268-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c1268-136">NOTES</span></span>

## <span data-ttu-id="c1268-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c1268-137">RELATED LINKS</span></span>
