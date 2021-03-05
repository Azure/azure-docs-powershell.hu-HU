---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: 5c2aa677bd2f197cfae262ed54372d5172fe2a4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009269"
---
# <span data-ttu-id="22c16-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="22c16-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="22c16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22c16-102">SYNOPSIS</span></span>
<span data-ttu-id="22c16-103">CDN-forráskiszolgálót kap.</span><span class="sxs-lookup"><span data-stu-id="22c16-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="22c16-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="22c16-104">SYNTAX</span></span>

### <span data-ttu-id="22c16-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="22c16-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22c16-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22c16-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22c16-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22c16-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22c16-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="22c16-108">DESCRIPTION</span></span>
<span data-ttu-id="22c16-109">A **Get-AzCdnOrigin** parancsmag kap egy Azure Content Delivery Network (CDN) forráskiszolgálót és konfigurációs adatait.</span><span class="sxs-lookup"><span data-stu-id="22c16-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="22c16-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="22c16-110">EXAMPLES</span></span>

## <span data-ttu-id="22c16-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22c16-111">PARAMETERS</span></span>

### <span data-ttu-id="22c16-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="22c16-112">-CdnEndpoint</span></span>
<span data-ttu-id="22c16-113">Azt a CDN-végpontobjektumot adja meg, amelyhez a forrás tartozik.</span><span class="sxs-lookup"><span data-stu-id="22c16-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22c16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c16-114">-DefaultProfile</span></span>
<span data-ttu-id="22c16-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="22c16-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22c16-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="22c16-116">-EndpointName</span></span>
<span data-ttu-id="22c16-117">Annak a végpontnak a nevét adja meg, amelyhez az originkiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="22c16-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c16-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="22c16-118">-OriginName</span></span>
<span data-ttu-id="22c16-119">A forráskiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="22c16-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="22c16-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="22c16-120">-ProfileName</span></span>
<span data-ttu-id="22c16-121">Annak a profilnak a nevét adja meg, amelyhez az originkiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="22c16-121">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c16-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22c16-122">-ResourceGroupName</span></span>
<span data-ttu-id="22c16-123">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az originkiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="22c16-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c16-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22c16-124">-ResourceId</span></span>
<span data-ttu-id="22c16-125">Az Azure CDN-forrás erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="22c16-125">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22c16-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c16-126">CommonParameters</span></span>
<span data-ttu-id="22c16-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c16-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c16-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22c16-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c16-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22c16-129">INPUTS</span></span>

### <span data-ttu-id="22c16-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="22c16-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="22c16-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="22c16-131">OUTPUTS</span></span>

### <span data-ttu-id="22c16-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="22c16-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="22c16-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="22c16-133">NOTES</span></span>

## <span data-ttu-id="22c16-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="22c16-134">RELATED LINKS</span></span>

[<span data-ttu-id="22c16-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="22c16-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


