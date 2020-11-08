---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: f648d347e45b6394776a25735efbb06157cc5611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012124"
---
# <span data-ttu-id="b60fb-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b60fb-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="b60fb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b60fb-102">SYNOPSIS</span></span>
<span data-ttu-id="b60fb-103">Bekapja a CDN-származási kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="b60fb-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="b60fb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b60fb-104">SYNTAX</span></span>

### <span data-ttu-id="b60fb-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b60fb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b60fb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b60fb-106">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b60fb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b60fb-107">DESCRIPTION</span></span>
<span data-ttu-id="b60fb-108">A **Get-AzCdnOrigin** parancsmag Azure Content Delivery Network (CDN) Origin Servert és a hozzá tartozó konfigurációs adatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b60fb-108">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="b60fb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="b60fb-109">EXAMPLES</span></span>

## <span data-ttu-id="b60fb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b60fb-110">PARAMETERS</span></span>

### <span data-ttu-id="b60fb-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="b60fb-111">-CdnEndpoint</span></span>
<span data-ttu-id="b60fb-112">Annak a CDN-végpont objektumnak a megadása, amelyhez a származás tartozik.</span><span class="sxs-lookup"><span data-stu-id="b60fb-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="b60fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60fb-113">-DefaultProfile</span></span>
<span data-ttu-id="b60fb-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b60fb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b60fb-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="b60fb-115">-EndpointName</span></span>
<span data-ttu-id="b60fb-116">Annak a végpontnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="b60fb-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="b60fb-117">-OriginName</span><span class="sxs-lookup"><span data-stu-id="b60fb-117">-OriginName</span></span>
<span data-ttu-id="b60fb-118">A forráskiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b60fb-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="b60fb-119">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="b60fb-119">-ProfileName</span></span>
<span data-ttu-id="b60fb-120">Annak a profilnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="b60fb-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="b60fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="b60fb-122">Annak az erőforrás-csoportnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="b60fb-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="b60fb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60fb-123">CommonParameters</span></span>
<span data-ttu-id="b60fb-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b60fb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60fb-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b60fb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60fb-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b60fb-126">INPUTS</span></span>

### <span data-ttu-id="b60fb-127">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="b60fb-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="b60fb-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b60fb-128">OUTPUTS</span></span>

### <span data-ttu-id="b60fb-129">Microsoft. Azure. Command. CDN. models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="b60fb-129">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="b60fb-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b60fb-130">NOTES</span></span>

## <span data-ttu-id="b60fb-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b60fb-131">RELATED LINKS</span></span>

[<span data-ttu-id="b60fb-132">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b60fb-132">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


