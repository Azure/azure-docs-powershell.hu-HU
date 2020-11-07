---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: b4800b77441a82fc0e9966be16f91c9d81a2214a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672171"
---
# <span data-ttu-id="423db-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="423db-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="423db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="423db-102">SYNOPSIS</span></span>
<span data-ttu-id="423db-103">Bekapja a CDN-származási kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="423db-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="423db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="423db-104">SYNTAX</span></span>

### <span data-ttu-id="423db-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="423db-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="423db-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="423db-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="423db-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="423db-107">DESCRIPTION</span></span>
<span data-ttu-id="423db-108">A **Get-AzureRmCdnOrigin** parancsmag Azure Content Delivery Network (CDN) Origin Servert és a hozzá tartozó konfigurációs adatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="423db-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="423db-109">Példák</span><span class="sxs-lookup"><span data-stu-id="423db-109">EXAMPLES</span></span>

## <span data-ttu-id="423db-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="423db-110">PARAMETERS</span></span>

### <span data-ttu-id="423db-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="423db-111">-CdnEndpoint</span></span>
<span data-ttu-id="423db-112">Annak a CDN-végpont objektumnak a megadása, amelyhez a származás tartozik.</span><span class="sxs-lookup"><span data-stu-id="423db-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="423db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="423db-113">-DefaultProfile</span></span>
<span data-ttu-id="423db-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="423db-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="423db-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="423db-115">-EndpointName</span></span>
<span data-ttu-id="423db-116">Annak a végpontnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="423db-116">Specifies the name of the endpoint to which the origin server belongs.</span></span>

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

### <span data-ttu-id="423db-117">-OriginName</span><span class="sxs-lookup"><span data-stu-id="423db-117">-OriginName</span></span>
<span data-ttu-id="423db-118">A forráskiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="423db-118">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="423db-119">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="423db-119">-ProfileName</span></span>
<span data-ttu-id="423db-120">Annak a profilnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="423db-120">Specifies the name of the profile to which the origin server belongs.</span></span>

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

### <span data-ttu-id="423db-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="423db-121">-ResourceGroupName</span></span>
<span data-ttu-id="423db-122">Annak az erőforrás-csoportnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="423db-122">Specifies the name of the resource group to which the origin server belongs.</span></span>

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

### <span data-ttu-id="423db-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="423db-123">CommonParameters</span></span>
<span data-ttu-id="423db-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="423db-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="423db-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="423db-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="423db-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="423db-126">INPUTS</span></span>

### <span data-ttu-id="423db-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="423db-127">PSEndpoint</span></span>
<span data-ttu-id="423db-128">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="423db-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="423db-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="423db-129">OUTPUTS</span></span>

###  
<span data-ttu-id="423db-130">Ez a parancsmag a Origin Server-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="423db-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="423db-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="423db-131">NOTES</span></span>

## <span data-ttu-id="423db-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="423db-132">RELATED LINKS</span></span>

[<span data-ttu-id="423db-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="423db-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


