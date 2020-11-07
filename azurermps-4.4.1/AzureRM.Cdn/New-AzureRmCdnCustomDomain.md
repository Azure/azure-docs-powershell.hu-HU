---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnCustomDomain.md
ms.openlocfilehash: ec15b97aa87c5e581069606a425f25b71dd495dd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679113"
---
# <span data-ttu-id="99dfb-101">New-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="99dfb-101">New-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="99dfb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="99dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="99dfb-103">Egyéni tartományt hoz létre a CDN-végponthoz.</span><span class="sxs-lookup"><span data-stu-id="99dfb-103">Creates a custom domain for a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99dfb-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="99dfb-104">SYNTAX</span></span>

### <span data-ttu-id="99dfb-105">Paraméterérték a mezők paramétereinek beállításához (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="99dfb-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99dfb-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="99dfb-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99dfb-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="99dfb-107">DESCRIPTION</span></span>
<span data-ttu-id="99dfb-108">A **New-AzureRmCdnCustomDomain** parancsmag létrehoz egy egyéni tartományt az Azure Content Delivery Network (CDN) végponthoz.</span><span class="sxs-lookup"><span data-stu-id="99dfb-108">The **New-AzureRmCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="99dfb-109">Példák</span><span class="sxs-lookup"><span data-stu-id="99dfb-109">EXAMPLES</span></span>

## <span data-ttu-id="99dfb-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="99dfb-110">PARAMETERS</span></span>

### <span data-ttu-id="99dfb-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="99dfb-111">-CdnEndpoint</span></span>
<span data-ttu-id="99dfb-112">Annak a CDN-végpont-objektumnak a megadása, amelyhez az egyéni tartomány hozzá lett adva.</span><span class="sxs-lookup"><span data-stu-id="99dfb-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="99dfb-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="99dfb-113">-CustomDomainName</span></span>
<span data-ttu-id="99dfb-114">Az egyéni tartomány erőforrásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99dfb-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="99dfb-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="99dfb-115">-EndpointName</span></span>
<span data-ttu-id="99dfb-116">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99dfb-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="99dfb-117">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="99dfb-117">-HostName</span></span>
<span data-ttu-id="99dfb-118">Az egyéni tartomány állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99dfb-118">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="99dfb-119">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="99dfb-119">-ProfileName</span></span>
<span data-ttu-id="99dfb-120">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="99dfb-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="99dfb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99dfb-121">-ResourceGroupName</span></span>
<span data-ttu-id="99dfb-122">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="99dfb-122">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="99dfb-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="99dfb-123">-Confirm</span></span>
<span data-ttu-id="99dfb-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="99dfb-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99dfb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99dfb-125">-WhatIf</span></span>
<span data-ttu-id="99dfb-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="99dfb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99dfb-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="99dfb-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99dfb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99dfb-128">-DefaultProfile</span></span>
<span data-ttu-id="99dfb-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="99dfb-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99dfb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99dfb-130">CommonParameters</span></span>
<span data-ttu-id="99dfb-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="99dfb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99dfb-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99dfb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99dfb-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="99dfb-133">INPUTS</span></span>

### <span data-ttu-id="99dfb-134">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="99dfb-134">PSEndpoint</span></span>
<span data-ttu-id="99dfb-135">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="99dfb-135">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="99dfb-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="99dfb-136">OUTPUTS</span></span>

### <span data-ttu-id="99dfb-137">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="99dfb-137">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="99dfb-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="99dfb-138">NOTES</span></span>

## <span data-ttu-id="99dfb-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="99dfb-139">RELATED LINKS</span></span>

[<span data-ttu-id="99dfb-140">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="99dfb-140">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="99dfb-141">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="99dfb-141">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="99dfb-142">Teszt-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="99dfb-142">Test-AzureRmCdnCustomDomain</span></span>](./Test-AzureRmCdnCustomDomain.md)


