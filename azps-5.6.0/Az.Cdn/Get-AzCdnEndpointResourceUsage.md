---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: d39bd2d3a10f1ff8512b54cdf45902fb10f6810d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015413"
---
# <span data-ttu-id="9fd8b-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="9fd8b-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="9fd8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fd8b-102">SYNOPSIS</span></span>
<span data-ttu-id="9fd8b-103">Egy CDN-végpont erőforrás-használatát használja.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="9fd8b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9fd8b-104">SYNTAX</span></span>

### <span data-ttu-id="9fd8b-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9fd8b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fd8b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fd8b-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fd8b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9fd8b-107">DESCRIPTION</span></span>
<span data-ttu-id="9fd8b-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="9fd8b-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="9fd8b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9fd8b-109">EXAMPLES</span></span>

### <span data-ttu-id="9fd8b-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="9fd8b-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9fd8b-111">{{ Adja meg itt a példa leírását }}</span><span class="sxs-lookup"><span data-stu-id="9fd8b-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="9fd8b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9fd8b-112">PARAMETERS</span></span>

### <span data-ttu-id="9fd8b-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fd8b-113">-CdnEndpoint</span></span>
<span data-ttu-id="9fd8b-114">A CDN végpontobjektuma.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="9fd8b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fd8b-115">-DefaultProfile</span></span>
<span data-ttu-id="9fd8b-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="9fd8b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fd8b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9fd8b-117">-EndpointName</span></span>
<span data-ttu-id="9fd8b-118">Azure CDN-végpont neve.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="9fd8b-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9fd8b-119">-ProfileName</span></span>
<span data-ttu-id="9fd8b-120">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="9fd8b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fd8b-121">-ResourceGroupName</span></span>
<span data-ttu-id="9fd8b-122">Az Azure CDN-profil erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="9fd8b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fd8b-123">CommonParameters</span></span>
<span data-ttu-id="9fd8b-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fd8b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fd8b-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9fd8b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fd8b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9fd8b-126">INPUTS</span></span>

### <span data-ttu-id="9fd8b-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fd8b-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="9fd8b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9fd8b-128">OUTPUTS</span></span>

### <span data-ttu-id="9fd8b-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="9fd8b-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="9fd8b-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9fd8b-130">NOTES</span></span>

## <span data-ttu-id="9fd8b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9fd8b-131">RELATED LINKS</span></span>
