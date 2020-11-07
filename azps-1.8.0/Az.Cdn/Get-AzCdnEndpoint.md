---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpoint.md
ms.openlocfilehash: 69375f53db47988d7ef2e5ca383c90a5de270931
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671419"
---
# <span data-ttu-id="4d602-101">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d602-101">Get-AzCdnEndpoint</span></span>

## <span data-ttu-id="4d602-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d602-102">SYNOPSIS</span></span>
<span data-ttu-id="4d602-103">Kap egy CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="4d602-103">Gets a CDN endpoint.</span></span>

## <span data-ttu-id="4d602-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d602-104">SYNTAX</span></span>

### <span data-ttu-id="4d602-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4d602-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d602-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d602-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d602-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d602-107">DESCRIPTION</span></span>
<span data-ttu-id="4d602-108">A **Get-AzCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját és a hozzá tartozó konfigurációs adatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4d602-108">The **Get-AzCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="4d602-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4d602-109">EXAMPLES</span></span>

## <span data-ttu-id="4d602-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d602-110">PARAMETERS</span></span>

### <span data-ttu-id="4d602-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="4d602-111">-CdnProfile</span></span>
<span data-ttu-id="4d602-112">Annak a CDN-profil objektumnak a megadása, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="4d602-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="4d602-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d602-113">-DefaultProfile</span></span>
<span data-ttu-id="4d602-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4d602-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d602-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4d602-115">-EndpointName</span></span>
<span data-ttu-id="4d602-116">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d602-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="4d602-117">A végpont neve nem a végpont állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d602-117">The name of the endpoint is not the host name of the endpoint.</span></span>

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

### <span data-ttu-id="4d602-118">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="4d602-118">-ProfileName</span></span>
<span data-ttu-id="4d602-119">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="4d602-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="4d602-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d602-120">-ResourceGroupName</span></span>
<span data-ttu-id="4d602-121">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="4d602-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="4d602-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d602-122">CommonParameters</span></span>
<span data-ttu-id="4d602-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d602-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d602-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d602-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d602-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d602-125">INPUTS</span></span>

### <span data-ttu-id="4d602-126">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="4d602-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="4d602-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d602-127">OUTPUTS</span></span>

### <span data-ttu-id="4d602-128">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d602-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="4d602-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d602-129">NOTES</span></span>

## <span data-ttu-id="4d602-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d602-130">RELATED LINKS</span></span>

[<span data-ttu-id="4d602-131">Új – AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d602-131">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="4d602-132">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d602-132">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="4d602-133">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d602-133">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="4d602-134">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d602-134">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="4d602-135">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d602-135">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


