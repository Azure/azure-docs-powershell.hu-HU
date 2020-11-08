---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOrigin.md
ms.openlocfilehash: e5e27dba4519d16ebc304f3d6cca99f32f23e341
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195247"
---
# <span data-ttu-id="5f1e5-101">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5f1e5-101">Get-AzCdnOrigin</span></span>

## <span data-ttu-id="5f1e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f1e5-102">SYNOPSIS</span></span>
<span data-ttu-id="5f1e5-103">Bekapja a CDN-származási kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-103">Gets a CDN origin server.</span></span>

## <span data-ttu-id="5f1e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f1e5-104">SYNTAX</span></span>

### <span data-ttu-id="5f1e5-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5f1e5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f1e5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f1e5-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f1e5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f1e5-107">ByObjectParameterSet</span></span>
```
Get-AzCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f1e5-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f1e5-108">DESCRIPTION</span></span>
<span data-ttu-id="5f1e5-109">A **Get-AzCdnOrigin** parancsmag Azure Content Delivery Network (CDN) Origin Servert és a hozzá tartozó konfigurációs adatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-109">The **Get-AzCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="5f1e5-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5f1e5-110">EXAMPLES</span></span>

## <span data-ttu-id="5f1e5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f1e5-111">PARAMETERS</span></span>

### <span data-ttu-id="5f1e5-112">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f1e5-112">-CdnEndpoint</span></span>
<span data-ttu-id="5f1e5-113">Annak a CDN-végpont objektumnak a megadása, amelyhez a származás tartozik.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-113">Specifies the CDN endpoint object to which the origin belongs.</span></span>

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

### <span data-ttu-id="5f1e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f1e5-114">-DefaultProfile</span></span>
<span data-ttu-id="5f1e5-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5f1e5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f1e5-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5f1e5-116">-EndpointName</span></span>
<span data-ttu-id="5f1e5-117">Annak a végpontnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-117">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="5f1e5-118">-OriginName</span><span class="sxs-lookup"><span data-stu-id="5f1e5-118">-OriginName</span></span>
<span data-ttu-id="5f1e5-119">A forráskiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-119">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="5f1e5-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="5f1e5-120">-ProfileName</span></span>
<span data-ttu-id="5f1e5-121">Annak a profilnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-121">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="5f1e5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f1e5-122">-ResourceGroupName</span></span>
<span data-ttu-id="5f1e5-123">Annak az erőforrás-csoportnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-123">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="5f1e5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f1e5-124">-ResourceId</span></span>
<span data-ttu-id="5f1e5-125">Az Azure CDN kezdőpontjának erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-125">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="5f1e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f1e5-126">CommonParameters</span></span>
<span data-ttu-id="5f1e5-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f1e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f1e5-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5f1e5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f1e5-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f1e5-129">INPUTS</span></span>

### <span data-ttu-id="5f1e5-130">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f1e5-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="5f1e5-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f1e5-131">OUTPUTS</span></span>

### <span data-ttu-id="5f1e5-132">Microsoft. Azure. Command. CDN. models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="5f1e5-132">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="5f1e5-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f1e5-133">NOTES</span></span>

## <span data-ttu-id="5f1e5-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f1e5-134">RELATED LINKS</span></span>

[<span data-ttu-id="5f1e5-135">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5f1e5-135">Set-AzCdnOrigin</span></span>](./Set-AzCdnOrigin.md)


