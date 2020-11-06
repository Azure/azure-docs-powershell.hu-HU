---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnCustomDomain.md
ms.openlocfilehash: dcfa0968ac70f7a0abc14ee61ee615bee3aee5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500932"
---
# <span data-ttu-id="dfd79-101">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="dfd79-101">Get-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="dfd79-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfd79-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd79-103">Bekerül egy CDN egyéni tartományba.</span><span class="sxs-lookup"><span data-stu-id="dfd79-103">Gets a CDN custom domain.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfd79-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfd79-104">SYNTAX</span></span>

### <span data-ttu-id="dfd79-105">Paraméterérték a mezők paramétereinek beállításához (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="dfd79-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfd79-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="dfd79-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfd79-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfd79-107">DESCRIPTION</span></span>
<span data-ttu-id="dfd79-108">A **Get-AzureRmCdnCustomDomain** parancsmag az Azure Content Delivery Network (CDN) egyéni tartományát és a hozzá kapcsolódó beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="dfd79-108">The **Get-AzureRmCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="dfd79-109">Példák</span><span class="sxs-lookup"><span data-stu-id="dfd79-109">EXAMPLES</span></span>

## <span data-ttu-id="dfd79-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfd79-110">PARAMETERS</span></span>

### <span data-ttu-id="dfd79-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="dfd79-111">-CdnEndpoint</span></span>
<span data-ttu-id="dfd79-112">Annak a CDN végpont-objektumnak a meghatározása, amelynek az egyéni tartománya a tag.</span><span class="sxs-lookup"><span data-stu-id="dfd79-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

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

### <span data-ttu-id="dfd79-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="dfd79-113">-CustomDomainName</span></span>
<span data-ttu-id="dfd79-114">Az egyéni tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dfd79-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="dfd79-115">Az egyéni tartomány neve eltér az egyéni tartomány állomásnevét.</span><span class="sxs-lookup"><span data-stu-id="dfd79-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="dfd79-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dfd79-116">-EndpointName</span></span>
<span data-ttu-id="dfd79-117">Annak a végpontnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="dfd79-117">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="dfd79-118">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="dfd79-118">-ProfileName</span></span>
<span data-ttu-id="dfd79-119">Annak a profilnak a neve, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="dfd79-119">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="dfd79-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfd79-120">-ResourceGroupName</span></span>
<span data-ttu-id="dfd79-121">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="dfd79-121">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="dfd79-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd79-122">-DefaultProfile</span></span>
<span data-ttu-id="dfd79-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dfd79-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfd79-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd79-124">CommonParameters</span></span>
<span data-ttu-id="dfd79-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfd79-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd79-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfd79-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd79-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfd79-127">INPUTS</span></span>

### <span data-ttu-id="dfd79-128">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="dfd79-128">PSEndpoint</span></span>
<span data-ttu-id="dfd79-129">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dfd79-129">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="dfd79-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfd79-130">OUTPUTS</span></span>

###  
<span data-ttu-id="dfd79-131">Ez a parancsmag egy egyéni tartomány-objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="dfd79-131">This cmdlet returns a custom domain object.</span></span>

## <span data-ttu-id="dfd79-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfd79-132">NOTES</span></span>

## <span data-ttu-id="dfd79-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfd79-133">RELATED LINKS</span></span>

[<span data-ttu-id="dfd79-134">Új – AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="dfd79-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="dfd79-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="dfd79-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


