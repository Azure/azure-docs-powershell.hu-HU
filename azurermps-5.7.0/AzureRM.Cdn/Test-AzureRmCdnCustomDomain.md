---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/test-azurermcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Test-AzureRmCdnCustomDomain.md
ms.openlocfilehash: 93f2013612a872288f95fba2cbf577002c7a9ace
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497760"
---
# <span data-ttu-id="7372d-101">Test-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7372d-101">Test-AzureRmCdnCustomDomain</span></span>

## <span data-ttu-id="7372d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7372d-102">SYNOPSIS</span></span>
<span data-ttu-id="7372d-103">Annak vizsgálata, hogy egy egyéni tartomány hozzáadható-e egy végponthoz.</span><span class="sxs-lookup"><span data-stu-id="7372d-103">Checks whether a custom domain can be added to an endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7372d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7372d-104">SYNTAX</span></span>

### <span data-ttu-id="7372d-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7372d-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzureRmCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7372d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7372d-106">ByObjectParameterSet</span></span>
```
Test-AzureRmCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7372d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7372d-107">DESCRIPTION</span></span>
<span data-ttu-id="7372d-108">A **AzureRmCdnCustomDomain-** parancsmag ellenőrzi, hogy egy egyéni tartomány hozzáadható-e egy végponthoz a CNAME megfeleltetés ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="7372d-108">The **Test-AzureRmCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="7372d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7372d-109">EXAMPLES</span></span>

## <span data-ttu-id="7372d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7372d-110">PARAMETERS</span></span>

### <span data-ttu-id="7372d-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7372d-111">-CdnEndpoint</span></span>
<span data-ttu-id="7372d-112">Azt a végpontot adja meg, amelyhez hozzá szeretné adni az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="7372d-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="7372d-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="7372d-113">-CustomDomainHostName</span></span>
<span data-ttu-id="7372d-114">Az egyéni tartomány állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7372d-114">Specifies the host name of the custom domain.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7372d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7372d-115">-DefaultProfile</span></span>
<span data-ttu-id="7372d-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7372d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7372d-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7372d-117">-EndpointName</span></span>
<span data-ttu-id="7372d-118">Annak a végpontnak a nevét adja meg, amelyhez hozzá szeretné adni az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="7372d-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="7372d-119">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="7372d-119">-ProfileName</span></span>
<span data-ttu-id="7372d-120">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7372d-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="7372d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7372d-121">-ResourceGroupName</span></span>
<span data-ttu-id="7372d-122">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7372d-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7372d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7372d-123">CommonParameters</span></span>
<span data-ttu-id="7372d-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7372d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7372d-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7372d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7372d-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7372d-126">INPUTS</span></span>

### <span data-ttu-id="7372d-127">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7372d-127">PSEndpoint</span></span>
<span data-ttu-id="7372d-128">A ' CdnEndpoint ' paraméter az "PSEndpoint" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="7372d-128">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="7372d-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7372d-129">OUTPUTS</span></span>

### <span data-ttu-id="7372d-130">Microsoft. Azure. Command. CDN. models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="7372d-130">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="7372d-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7372d-131">NOTES</span></span>

## <span data-ttu-id="7372d-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7372d-132">RELATED LINKS</span></span>

[<span data-ttu-id="7372d-133">Get-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7372d-133">Get-AzureRmCdnCustomDomain</span></span>](./Get-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="7372d-134">Új – AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7372d-134">New-AzureRmCdnCustomDomain</span></span>](./New-AzureRmCdnCustomDomain.md)

[<span data-ttu-id="7372d-135">Remove-AzureRmCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7372d-135">Remove-AzureRmCdnCustomDomain</span></span>](./Remove-AzureRmCdnCustomDomain.md)


