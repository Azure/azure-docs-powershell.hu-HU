---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 6a0a90657ee76401117971a29dc03a78a7330afc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94014909"
---
# <span data-ttu-id="7d1d1-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7d1d1-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="7d1d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7d1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1d1-103">Egyéni tartományt hoz létre a CDN-végponthoz.</span><span class="sxs-lookup"><span data-stu-id="7d1d1-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="7d1d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7d1d1-104">SYNTAX</span></span>

### <span data-ttu-id="7d1d1-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7d1d1-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1d1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1d1-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d1d1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7d1d1-107">DESCRIPTION</span></span>
<span data-ttu-id="7d1d1-108">A **New-AzCdnCustomDomain** parancsmag létrehoz egy egyéni tartományt az Azure Content Delivery Network (CDN) végponthoz.</span><span class="sxs-lookup"><span data-stu-id="7d1d1-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7d1d1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7d1d1-109">EXAMPLES</span></span>

## <span data-ttu-id="7d1d1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7d1d1-110">PARAMETERS</span></span>

### <span data-ttu-id="7d1d1-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d1d1-111">-CdnEndpoint</span></span>
<span data-ttu-id="7d1d1-112">Annak a CDN-végpont-objektumnak a megadása, amelyhez az egyéni tartomány hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="7d1d1-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="7d1d1-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7d1d1-113">-CustomDomainName</span></span>
<span data-ttu-id="7d1d1-114">Az egyéni tartomány erőforrásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d1d1-114">Specifies the resource name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1d1-115">-DefaultProfile</span></span>
<span data-ttu-id="7d1d1-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7d1d1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d1d1-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7d1d1-117">-EndpointName</span></span>
<span data-ttu-id="7d1d1-118">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d1d1-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="7d1d1-119">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="7d1d1-119">-HostName</span></span>
<span data-ttu-id="7d1d1-120">Az egyéni tartomány állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d1d1-120">Specifies the host name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1d1-121">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="7d1d1-121">-ProfileName</span></span>
<span data-ttu-id="7d1d1-122">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7d1d1-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="7d1d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d1d1-124">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="7d1d1-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="7d1d1-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7d1d1-125">-Confirm</span></span>
<span data-ttu-id="7d1d1-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7d1d1-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1d1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1d1-127">-WhatIf</span></span>
<span data-ttu-id="7d1d1-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7d1d1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d1d1-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7d1d1-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1d1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1d1-130">CommonParameters</span></span>
<span data-ttu-id="7d1d1-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7d1d1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1d1-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7d1d1-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1d1-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d1d1-133">INPUTS</span></span>

### <span data-ttu-id="7d1d1-134">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7d1d1-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7d1d1-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7d1d1-135">OUTPUTS</span></span>

### <span data-ttu-id="7d1d1-136">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7d1d1-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="7d1d1-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7d1d1-137">NOTES</span></span>

## <span data-ttu-id="7d1d1-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7d1d1-138">RELATED LINKS</span></span>

[<span data-ttu-id="7d1d1-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7d1d1-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="7d1d1-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7d1d1-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="7d1d1-141">Teszt-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7d1d1-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


