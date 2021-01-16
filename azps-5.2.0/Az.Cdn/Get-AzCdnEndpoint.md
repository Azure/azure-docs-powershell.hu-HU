---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 5f137543d694ee9d470a1e24d1ba6d52b22cd2e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347250"
---
# <span data-ttu-id="ebc28-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebc28-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="ebc28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebc28-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc28-103">CDN-végpontot kap.</span><span class="sxs-lookup"><span data-stu-id="ebc28-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="ebc28-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ebc28-104">SYNTAX</span></span>

### <span data-ttu-id="ebc28-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ebc28-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebc28-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebc28-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebc28-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ebc28-107">DESCRIPTION</span></span>
<span data-ttu-id="ebc28-108">A **Get-AzCdnEndpoint** parancsmag megkapja az Azure Content Delivery Network (CDN) végpontot és a hozzá tartozó konfigurációs adatokat.</span><span class="sxs-lookup"><span data-stu-id="ebc28-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="ebc28-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ebc28-109">EXAMPLES</span></span>

## <span data-ttu-id="ebc28-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebc28-110">PARAMETERS</span></span>

### <span data-ttu-id="ebc28-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="ebc28-111">-CdnProfile</span></span>
<span data-ttu-id="ebc28-112">Azt a CDN-profilobjektumot adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="ebc28-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebc28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc28-113">-DefaultProfile</span></span>
<span data-ttu-id="ebc28-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ebc28-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ebc28-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ebc28-115">-EndpointName</span></span>
<span data-ttu-id="ebc28-116">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ebc28-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="ebc28-117">A végpont neve nem a végpont állomásneve.</span><span class="sxs-lookup"><span data-stu-id="ebc28-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="ebc28-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ebc28-118">-ProfileName</span></span>
<span data-ttu-id="ebc28-119">Annak a profilnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="ebc28-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="ebc28-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc28-120">-ResourceGroupName</span></span>
<span data-ttu-id="ebc28-121">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="ebc28-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="ebc28-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc28-122">CommonParameters</span></span>
<span data-ttu-id="ebc28-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebc28-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc28-124">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebc28-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc28-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebc28-125">INPUTS</span></span>

### <span data-ttu-id="ebc28-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="ebc28-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="ebc28-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ebc28-127">OUTPUTS</span></span>

### <span data-ttu-id="ebc28-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebc28-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="ebc28-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ebc28-129">NOTES</span></span>

## <span data-ttu-id="ebc28-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ebc28-130">RELATED LINKS</span></span>

[<span data-ttu-id="ebc28-131">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebc28-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="ebc28-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebc28-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="ebc28-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebc28-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="ebc28-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebc28-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="ebc28-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="ebc28-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


