---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010803"
---
# <span data-ttu-id="11c92-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="11c92-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="11c92-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11c92-102">SYNOPSIS</span></span>
<span data-ttu-id="11c92-103">Bekerül egy CDN egyéni tartományba.</span><span class="sxs-lookup"><span data-stu-id="11c92-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="11c92-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11c92-104">SYNTAX</span></span>

### <span data-ttu-id="11c92-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="11c92-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11c92-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11c92-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11c92-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="11c92-107">DESCRIPTION</span></span>
<span data-ttu-id="11c92-108">A **Get-AzCdnCustomDomain** parancsmag az Azure Content Delivery Network (CDN) egyéni tartományát és a hozzá kapcsolódó beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="11c92-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="11c92-109">Példák</span><span class="sxs-lookup"><span data-stu-id="11c92-109">EXAMPLES</span></span>

## <span data-ttu-id="11c92-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11c92-110">PARAMETERS</span></span>

### <span data-ttu-id="11c92-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="11c92-111">-CdnEndpoint</span></span>
<span data-ttu-id="11c92-112">Annak a CDN végpont-objektumnak a meghatározása, amelynek az egyéni tartománya a tag.</span><span class="sxs-lookup"><span data-stu-id="11c92-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="11c92-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="11c92-113">-CustomDomainName</span></span>
<span data-ttu-id="11c92-114">Az egyéni tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="11c92-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="11c92-115">Az egyéni tartomány neve eltér az egyéni tartomány állomásnevét.</span><span class="sxs-lookup"><span data-stu-id="11c92-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="11c92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c92-116">-DefaultProfile</span></span>
<span data-ttu-id="11c92-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="11c92-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11c92-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="11c92-118">-EndpointName</span></span>
<span data-ttu-id="11c92-119">Annak a végpontnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="11c92-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="11c92-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="11c92-120">-ProfileName</span></span>
<span data-ttu-id="11c92-121">Annak a profilnak a neve, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="11c92-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="11c92-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c92-122">-ResourceGroupName</span></span>
<span data-ttu-id="11c92-123">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="11c92-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="11c92-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c92-124">CommonParameters</span></span>
<span data-ttu-id="11c92-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11c92-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c92-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="11c92-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c92-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11c92-127">INPUTS</span></span>

### <span data-ttu-id="11c92-128">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="11c92-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="11c92-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11c92-129">OUTPUTS</span></span>

### <span data-ttu-id="11c92-130">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="11c92-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="11c92-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11c92-131">NOTES</span></span>

## <span data-ttu-id="11c92-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11c92-132">RELATED LINKS</span></span>

[<span data-ttu-id="11c92-133">Új – AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="11c92-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="11c92-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="11c92-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


