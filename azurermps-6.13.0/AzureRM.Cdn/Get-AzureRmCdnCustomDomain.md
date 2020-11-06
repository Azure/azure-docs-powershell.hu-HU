---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: e0c1d2e49cce4798499506352811d1e341bf47e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504499"
---
# <span data-ttu-id="ab7d1-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ab7d1-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="ab7d1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab7d1-102">SYNOPSIS</span></span>
<span data-ttu-id="ab7d1-103">Bekerül egy CDN egyéni tartományba.</span><span class="sxs-lookup"><span data-stu-id="ab7d1-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab7d1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab7d1-104">SYNTAX</span></span>

### <span data-ttu-id="ab7d1-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ab7d1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab7d1-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab7d1-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab7d1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab7d1-107">DESCRIPTION</span></span>
<span data-ttu-id="ab7d1-108">A **Get-AzureRmCdnCustomDomain** parancsmag az Azure Content Delivery Network (CDN) egyéni tartományát és a hozzá kapcsolódó beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ab7d1-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="ab7d1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ab7d1-109">EXAMPLES</span></span>

## <span data-ttu-id="ab7d1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab7d1-110">PARAMETERS</span></span>

### <span data-ttu-id="ab7d1-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab7d1-111">-CdnEndpoint</span></span>
<span data-ttu-id="ab7d1-112">Annak a CDN végpont-objektumnak a meghatározása, amelynek az egyéni tartománya a tag.</span><span class="sxs-lookup"><span data-stu-id="ab7d1-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="ab7d1-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="ab7d1-113">-CustomDomainName</span></span>
<span data-ttu-id="ab7d1-114">Az egyéni tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab7d1-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="ab7d1-115">Az egyéni tartomány neve eltér az egyéni tartomány állomásnevét.</span><span class="sxs-lookup"><span data-stu-id="ab7d1-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="ab7d1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab7d1-116">-DefaultProfile</span></span>
<span data-ttu-id="ab7d1-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ab7d1-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7d1-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ab7d1-118">-EndpointName</span></span>
<span data-ttu-id="ab7d1-119">Annak a végpontnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="ab7d1-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ab7d1-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="ab7d1-120">-ProfileName</span></span>
<span data-ttu-id="ab7d1-121">Annak a profilnak a neve, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="ab7d1-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ab7d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab7d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="ab7d1-123">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="ab7d1-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="ab7d1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab7d1-124">CommonParameters</span></span>
<span data-ttu-id="ab7d1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab7d1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab7d1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab7d1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab7d1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab7d1-127">INPUTS</span></span>

### <span data-ttu-id="ab7d1-128">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab7d1-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>
<span data-ttu-id="ab7d1-129">Paraméterek: CdnEndpoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab7d1-129">Parameters: CdnEndpoint (ByValue)</span></span>

## <span data-ttu-id="ab7d1-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab7d1-130">OUTPUTS</span></span>

### <span data-ttu-id="ab7d1-131">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ab7d1-131">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="ab7d1-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab7d1-132">NOTES</span></span>

## <span data-ttu-id="ab7d1-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab7d1-133">RELATED LINKS</span></span>

[<span data-ttu-id="ab7d1-134">Új – AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ab7d1-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="ab7d1-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="ab7d1-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


