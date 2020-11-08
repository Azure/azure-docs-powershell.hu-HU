---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002785"
---
# <span data-ttu-id="c0679-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c0679-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="c0679-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c0679-102">SYNOPSIS</span></span>
<span data-ttu-id="c0679-103">Annak vizsgálata, hogy egy egyéni tartomány hozzáadható-e egy végponthoz.</span><span class="sxs-lookup"><span data-stu-id="c0679-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="c0679-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c0679-104">SYNTAX</span></span>

### <span data-ttu-id="c0679-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c0679-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0679-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0679-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0679-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c0679-107">DESCRIPTION</span></span>
<span data-ttu-id="c0679-108">A **AzCdnCustomDomain-** parancsmag ellenőrzi, hogy egy egyéni tartomány hozzáadható-e egy végponthoz a CNAME megfeleltetés ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="c0679-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="c0679-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c0679-109">EXAMPLES</span></span>

## <span data-ttu-id="c0679-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c0679-110">PARAMETERS</span></span>

### <span data-ttu-id="c0679-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0679-111">-CdnEndpoint</span></span>
<span data-ttu-id="c0679-112">Azt a végpontot adja meg, amelyhez hozzá szeretné adni az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="c0679-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="c0679-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="c0679-113">-CustomDomainHostName</span></span>
<span data-ttu-id="c0679-114">Az egyéni tartomány állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0679-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="c0679-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0679-115">-DefaultProfile</span></span>
<span data-ttu-id="c0679-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="c0679-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0679-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c0679-117">-EndpointName</span></span>
<span data-ttu-id="c0679-118">Annak a végpontnak a nevét adja meg, amelyhez hozzá szeretné adni az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="c0679-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="c0679-119">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="c0679-119">-ProfileName</span></span>
<span data-ttu-id="c0679-120">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0679-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="c0679-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0679-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0679-122">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c0679-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c0679-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0679-123">CommonParameters</span></span>
<span data-ttu-id="c0679-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c0679-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0679-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c0679-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0679-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0679-126">INPUTS</span></span>

### <span data-ttu-id="c0679-127">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c0679-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c0679-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c0679-128">OUTPUTS</span></span>

### <span data-ttu-id="c0679-129">Microsoft. Azure. Command. CDN. models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="c0679-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="c0679-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c0679-130">NOTES</span></span>

## <span data-ttu-id="c0679-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c0679-131">RELATED LINKS</span></span>

[<span data-ttu-id="c0679-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c0679-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="c0679-133">Új – AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c0679-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="c0679-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="c0679-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


