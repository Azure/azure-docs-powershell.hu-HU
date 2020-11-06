---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 91919242-59ED-4938-A3A3-23A66F85FBC1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnOrigin.md
ms.openlocfilehash: aba554d2c81e4fce438e9bd6e10a8dfec63da465
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505643"
---
# <span data-ttu-id="e778b-101">Get-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e778b-101">Get-AzureRmCdnOrigin</span></span>

## <span data-ttu-id="e778b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e778b-102">SYNOPSIS</span></span>
<span data-ttu-id="e778b-103">Bekapja a CDN-származási kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="e778b-103">Gets a CDN origin server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e778b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e778b-104">SYNTAX</span></span>

### <span data-ttu-id="e778b-105">Paraméterérték a mezők paramétereinek beállításához (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e778b-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e778b-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="e778b-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnOrigin [-OriginName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e778b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="e778b-107">DESCRIPTION</span></span>
<span data-ttu-id="e778b-108">A **Get-AzureRmCdnOrigin** parancsmag Azure Content Delivery Network (CDN) Origin Servert és a hozzá tartozó konfigurációs adatokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e778b-108">The **Get-AzureRmCdnOrigin** cmdlet gets an Azure Content Delivery Network (CDN) origin server and its configuration data.</span></span>

## <span data-ttu-id="e778b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="e778b-109">EXAMPLES</span></span>

## <span data-ttu-id="e778b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e778b-110">PARAMETERS</span></span>

### <span data-ttu-id="e778b-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e778b-111">-CdnEndpoint</span></span>
<span data-ttu-id="e778b-112">Annak a CDN-végpont objektumnak a megadása, amelyhez a származás tartozik.</span><span class="sxs-lookup"><span data-stu-id="e778b-112">Specifies the CDN endpoint object to which the origin belongs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e778b-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e778b-113">-EndpointName</span></span>
<span data-ttu-id="e778b-114">Annak a végpontnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="e778b-114">Specifies the name of the endpoint to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e778b-115">-OriginName</span><span class="sxs-lookup"><span data-stu-id="e778b-115">-OriginName</span></span>
<span data-ttu-id="e778b-116">A forráskiszolgáló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e778b-116">Specifies the name of the origin server.</span></span>

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

### <span data-ttu-id="e778b-117">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="e778b-117">-ProfileName</span></span>
<span data-ttu-id="e778b-118">Annak a profilnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="e778b-118">Specifies the name of the profile to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e778b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e778b-119">-ResourceGroupName</span></span>
<span data-ttu-id="e778b-120">Annak az erőforrás-csoportnak a neve, amelyhez a származási kiszolgáló tartozik.</span><span class="sxs-lookup"><span data-stu-id="e778b-120">Specifies the name of the resource group to which the origin server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e778b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e778b-121">-DefaultProfile</span></span>
<span data-ttu-id="e778b-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e778b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e778b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e778b-123">CommonParameters</span></span>
<span data-ttu-id="e778b-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e778b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e778b-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e778b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e778b-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e778b-126">INPUTS</span></span>

### <span data-ttu-id="e778b-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e778b-127">PSEndpoint</span></span>
<span data-ttu-id="e778b-128">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e778b-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="e778b-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e778b-129">OUTPUTS</span></span>

###  
<span data-ttu-id="e778b-130">Ez a parancsmag a Origin Server-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="e778b-130">This cmdlet returns an origin server object.</span></span>

## <span data-ttu-id="e778b-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e778b-131">NOTES</span></span>

## <span data-ttu-id="e778b-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e778b-132">RELATED LINKS</span></span>

[<span data-ttu-id="e778b-133">Set-AzureRmCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="e778b-133">Set-AzureRmCdnOrigin</span></span>](./Set-AzureRmCdnOrigin.md)


