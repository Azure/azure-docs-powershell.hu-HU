---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: F93D9D7C-AC2A-4D83-87EC-4A54CD45272B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpoint.md
ms.openlocfilehash: d3e33e8bf6dea2e06e8ee72199e040a563d0d974
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493234"
---
# <span data-ttu-id="baf1d-101">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="baf1d-101">Get-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="baf1d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="baf1d-102">SYNOPSIS</span></span>
<span data-ttu-id="baf1d-103">Kap egy CDN-végpontot.</span><span class="sxs-lookup"><span data-stu-id="baf1d-103">Gets a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baf1d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="baf1d-104">SYNTAX</span></span>

### <span data-ttu-id="baf1d-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="baf1d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baf1d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="baf1d-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnEndpoint [-EndpointName <String>] -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baf1d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="baf1d-107">DESCRIPTION</span></span>
<span data-ttu-id="baf1d-108">A **Get-AzureRMCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját és a hozzá tartozó konfigurációs adatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="baf1d-108">The **Get-AzureRMCdnEndpoint** cmdlet gets an Azure Content Delivery Network (CDN) endpoint and its associated configuration data.</span></span>

## <span data-ttu-id="baf1d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="baf1d-109">EXAMPLES</span></span>

## <span data-ttu-id="baf1d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="baf1d-110">PARAMETERS</span></span>

### <span data-ttu-id="baf1d-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="baf1d-111">-CdnProfile</span></span>
<span data-ttu-id="baf1d-112">Annak a CDN-profil objektumnak a megadása, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="baf1d-112">Specifies the CDN profile object to which the endpoint belongs.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baf1d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf1d-113">-DefaultProfile</span></span>
<span data-ttu-id="baf1d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="baf1d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf1d-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="baf1d-115">-EndpointName</span></span>
<span data-ttu-id="baf1d-116">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="baf1d-116">Specifies the name of the endpoint.</span></span>
<span data-ttu-id="baf1d-117">A végpont neve nem a végpont állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="baf1d-117">The name of the endpoint is not the host name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf1d-118">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="baf1d-118">-ProfileName</span></span>
<span data-ttu-id="baf1d-119">Annak a profilnak a neve, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="baf1d-119">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf1d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baf1d-120">-ResourceGroupName</span></span>
<span data-ttu-id="baf1d-121">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="baf1d-121">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf1d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf1d-122">CommonParameters</span></span>
<span data-ttu-id="baf1d-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="baf1d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf1d-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baf1d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf1d-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="baf1d-125">INPUTS</span></span>

### <span data-ttu-id="baf1d-126">PSProfile</span><span class="sxs-lookup"><span data-stu-id="baf1d-126">PSProfile</span></span>
<span data-ttu-id="baf1d-127">A ' CdnProfile ' paraméter az "PSProfile" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="baf1d-127">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="baf1d-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="baf1d-128">OUTPUTS</span></span>

###  
<span data-ttu-id="baf1d-129">Ez a parancsmag végpont-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="baf1d-129">This cmdlet returns an endpoint object.</span></span>

## <span data-ttu-id="baf1d-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="baf1d-130">NOTES</span></span>

## <span data-ttu-id="baf1d-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="baf1d-131">RELATED LINKS</span></span>

[<span data-ttu-id="baf1d-132">Új – AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="baf1d-132">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="baf1d-133">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="baf1d-133">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="baf1d-134">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="baf1d-134">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="baf1d-135">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="baf1d-135">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="baf1d-136">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="baf1d-136">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


