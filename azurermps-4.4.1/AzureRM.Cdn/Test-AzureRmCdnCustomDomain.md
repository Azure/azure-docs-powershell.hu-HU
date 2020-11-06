---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: df871dff0f59bc9c1e319e1470bbaa37750542e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497851"
---
# <span data-ttu-id="f7744-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f7744-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="f7744-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7744-102">SYNOPSIS</span></span>
<span data-ttu-id="f7744-103">Annak vizsgálata, hogy egy egyéni tartomány hozzáadható-e egy végponthoz.</span><span class="sxs-lookup"><span data-stu-id="f7744-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7744-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7744-104">SYNTAX</span></span>

### <span data-ttu-id="f7744-105">Paraméterérték a mezők paramétereinek beállításához (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7744-105">Parameter Set for fields parameters (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7744-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="f7744-106">Parameter Set for object parameters</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7744-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7744-107">DESCRIPTION</span></span>
<span data-ttu-id="f7744-108">A **AzureRmCdnCustomDomain-** parancsmag ellenőrzi, hogy egy egyéni tartomány hozzáadható-e egy végponthoz a CNAME megfeleltetés ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="f7744-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="f7744-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f7744-109">EXAMPLES</span></span>

## <span data-ttu-id="f7744-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7744-110">PARAMETERS</span></span>

### <span data-ttu-id="f7744-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7744-111">-CdnEndpoint</span></span>
<span data-ttu-id="f7744-112">Azt a végpontot adja meg, amelyhez hozzá szeretné adni az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="f7744-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="f7744-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="f7744-113">-CustomDomainHostName</span></span>
<span data-ttu-id="f7744-114">Az egyéni tartomány állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7744-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="f7744-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f7744-115">-EndpointName</span></span>
<span data-ttu-id="f7744-116">Annak a végpontnak a nevét adja meg, amelyhez hozzá szeretné adni az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="f7744-116">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="f7744-117">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="f7744-117">-ProfileName</span></span>
<span data-ttu-id="f7744-118">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7744-118">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="f7744-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7744-119">-ResourceGroupName</span></span>
<span data-ttu-id="f7744-120">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f7744-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="f7744-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7744-121">-DefaultProfile</span></span>
<span data-ttu-id="f7744-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7744-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7744-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7744-123">CommonParameters</span></span>
<span data-ttu-id="f7744-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7744-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7744-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7744-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7744-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7744-126">INPUTS</span></span>

### <span data-ttu-id="f7744-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7744-127">PSEndpoint</span></span>
<span data-ttu-id="f7744-128">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f7744-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="f7744-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7744-129">OUTPUTS</span></span>

### <span data-ttu-id="f7744-130">Microsoft. Azure. Command. CDN. models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="f7744-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="f7744-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7744-131">NOTES</span></span>

## <span data-ttu-id="f7744-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7744-132">RELATED LINKS</span></span>

[<span data-ttu-id="f7744-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f7744-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="f7744-134">Új – AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f7744-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="f7744-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="f7744-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


