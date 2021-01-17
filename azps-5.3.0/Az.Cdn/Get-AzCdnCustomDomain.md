---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: c98ec2ebee71188ddbc5760dbbd3d1528da3c770
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478034"
---
# <span data-ttu-id="39b8e-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="39b8e-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="39b8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39b8e-102">SYNOPSIS</span></span>
<span data-ttu-id="39b8e-103">Egyéni CDN-tartományt kap.</span><span class="sxs-lookup"><span data-stu-id="39b8e-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="39b8e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="39b8e-104">SYNTAX</span></span>

### <span data-ttu-id="39b8e-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="39b8e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39b8e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39b8e-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39b8e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="39b8e-107">DESCRIPTION</span></span>
<span data-ttu-id="39b8e-108">A **Get-AzCdnCustomDomain** parancsmag egyéni tartományt kap az Azure Content Delivery Network (CDN) szolgáltatáshoz, valamint annak kapcsolódó beállításait.</span><span class="sxs-lookup"><span data-stu-id="39b8e-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="39b8e-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="39b8e-109">EXAMPLES</span></span>

## <span data-ttu-id="39b8e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39b8e-110">PARAMETERS</span></span>

### <span data-ttu-id="39b8e-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="39b8e-111">-CdnEndpoint</span></span>
<span data-ttu-id="39b8e-112">Azt a CDN-végpontobjektumot adja meg, amelynek az egyéni tartomány tagja.</span><span class="sxs-lookup"><span data-stu-id="39b8e-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="39b8e-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="39b8e-113">-CustomDomainName</span></span>
<span data-ttu-id="39b8e-114">Az egyéni tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="39b8e-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="39b8e-115">Az egyéni tartomány neve eltér az egyéni tartomány állomásnevének nevétől.</span><span class="sxs-lookup"><span data-stu-id="39b8e-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="39b8e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b8e-116">-DefaultProfile</span></span>
<span data-ttu-id="39b8e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="39b8e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39b8e-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="39b8e-118">-EndpointName</span></span>
<span data-ttu-id="39b8e-119">Annak a végpontnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="39b8e-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="39b8e-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="39b8e-120">-ProfileName</span></span>
<span data-ttu-id="39b8e-121">Annak a profilnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="39b8e-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="39b8e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39b8e-122">-ResourceGroupName</span></span>
<span data-ttu-id="39b8e-123">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="39b8e-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="39b8e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b8e-124">CommonParameters</span></span>
<span data-ttu-id="39b8e-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39b8e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b8e-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39b8e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b8e-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39b8e-127">INPUTS</span></span>

### <span data-ttu-id="39b8e-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="39b8e-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="39b8e-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39b8e-129">OUTPUTS</span></span>

### <span data-ttu-id="39b8e-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="39b8e-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="39b8e-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="39b8e-131">NOTES</span></span>

## <span data-ttu-id="39b8e-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39b8e-132">RELATED LINKS</span></span>

[<span data-ttu-id="39b8e-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="39b8e-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="39b8e-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="39b8e-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


