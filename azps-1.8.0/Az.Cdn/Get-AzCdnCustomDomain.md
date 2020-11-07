---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 53246003-D1E9-4863-94E9-8E0BF1272134
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnCustomDomain.md
ms.openlocfilehash: 9f97b088fd0c60c290d9c9e6d559b6e8a091fba8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671423"
---
# <span data-ttu-id="bcc44-101">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bcc44-101">Get-AzCdnCustomDomain</span></span>

## <span data-ttu-id="bcc44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bcc44-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc44-103">Bekerül egy CDN egyéni tartományba.</span><span class="sxs-lookup"><span data-stu-id="bcc44-103">Gets a CDN custom domain.</span></span>

## <span data-ttu-id="bcc44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bcc44-104">SYNTAX</span></span>

### <span data-ttu-id="bcc44-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bcc44-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcc44-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcc44-106">ByObjectParameterSet</span></span>
```
Get-AzCdnCustomDomain [-CustomDomainName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcc44-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bcc44-107">DESCRIPTION</span></span>
<span data-ttu-id="bcc44-108">A **Get-AzCdnCustomDomain** parancsmag az Azure Content Delivery Network (CDN) egyéni tartományát és a hozzá kapcsolódó beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bcc44-108">The **Get-AzCdnCustomDomain** cmdlet gets an Azure Content Delivery Network (CDN) custom domain and its related settings.</span></span>

## <span data-ttu-id="bcc44-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bcc44-109">EXAMPLES</span></span>

## <span data-ttu-id="bcc44-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bcc44-110">PARAMETERS</span></span>

### <span data-ttu-id="bcc44-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="bcc44-111">-CdnEndpoint</span></span>
<span data-ttu-id="bcc44-112">Annak a CDN végpont-objektumnak a meghatározása, amelynek az egyéni tartománya a tag.</span><span class="sxs-lookup"><span data-stu-id="bcc44-112">Specifies the CDN endpoint object of which the custom domain is a member.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc44-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="bcc44-113">-CustomDomainName</span></span>
<span data-ttu-id="bcc44-114">Az egyéni tartomány nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bcc44-114">Specifies the name of the custom domain.</span></span>
<span data-ttu-id="bcc44-115">Az egyéni tartomány neve eltér az egyéni tartomány állomásnevét.</span><span class="sxs-lookup"><span data-stu-id="bcc44-115">The name of the custom domain differs from the host name of the custom domain.</span></span>

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

### <span data-ttu-id="bcc44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc44-116">-DefaultProfile</span></span>
<span data-ttu-id="bcc44-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bcc44-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcc44-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bcc44-118">-EndpointName</span></span>
<span data-ttu-id="bcc44-119">Annak a végpontnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="bcc44-119">Specifies the name of the endpoint to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="bcc44-120">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="bcc44-120">-ProfileName</span></span>
<span data-ttu-id="bcc44-121">Annak a profilnak a neve, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="bcc44-121">Specifies the name of the Profile to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="bcc44-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc44-122">-ResourceGroupName</span></span>
<span data-ttu-id="bcc44-123">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez az egyéni tartomány tartozik.</span><span class="sxs-lookup"><span data-stu-id="bcc44-123">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="bcc44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc44-124">CommonParameters</span></span>
<span data-ttu-id="bcc44-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bcc44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc44-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcc44-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc44-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcc44-127">INPUTS</span></span>

### <span data-ttu-id="bcc44-128">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="bcc44-128">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="bcc44-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcc44-129">OUTPUTS</span></span>

### <span data-ttu-id="bcc44-130">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bcc44-130">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="bcc44-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bcc44-131">NOTES</span></span>

## <span data-ttu-id="bcc44-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcc44-132">RELATED LINKS</span></span>

[<span data-ttu-id="bcc44-133">Új – AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bcc44-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="bcc44-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="bcc44-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


