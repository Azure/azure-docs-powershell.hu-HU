---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 09439fd202d01d6cf5ffc8be614940cdf39ad1ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667612"
---
# <span data-ttu-id="7051c-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7051c-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="7051c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7051c-102">SYNOPSIS</span></span>
<span data-ttu-id="7051c-103">Kap egy CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="7051c-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="7051c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7051c-104">SYNTAX</span></span>

### <span data-ttu-id="7051c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7051c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7051c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7051c-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7051c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7051c-107">DESCRIPTION</span></span>
<span data-ttu-id="7051c-108">A **Get-AzCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját és a hozzá tartozó konfigurációs adatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="7051c-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="7051c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7051c-109">EXAMPLES</span></span>

## <span data-ttu-id="7051c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7051c-110">PARAMETERS</span></span>

### <span data-ttu-id="7051c-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="7051c-111">-CdnProfile</span></span>
<span data-ttu-id="7051c-112">Annak a CDN-profil objektumnak a megadása, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="7051c-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="7051c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7051c-113">-DefaultProfile</span></span>
<span data-ttu-id="7051c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7051c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7051c-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7051c-115">-EndpointName</span></span>
<span data-ttu-id="7051c-116">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7051c-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="7051c-117">A végpont neve nem a végpont állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7051c-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="7051c-118">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="7051c-118">-ProfileName</span></span>
<span data-ttu-id="7051c-119">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="7051c-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="7051c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7051c-120">-ResourceGroupName</span></span>
<span data-ttu-id="7051c-121">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="7051c-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="7051c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7051c-122">CommonParameters</span></span>
<span data-ttu-id="7051c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7051c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7051c-124">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="7051c-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7051c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7051c-125">INPUTS</span></span>

### <span data-ttu-id="7051c-126">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="7051c-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="7051c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7051c-127">OUTPUTS</span></span>

### <span data-ttu-id="7051c-128">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7051c-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7051c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7051c-129">NOTES</span></span>

## <span data-ttu-id="7051c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7051c-130">RELATED LINKS</span></span>

[<span data-ttu-id="7051c-131">Új – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7051c-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="7051c-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7051c-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="7051c-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7051c-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="7051c-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7051c-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="7051c-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7051c-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


