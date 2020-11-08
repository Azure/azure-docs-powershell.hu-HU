---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194920"
---
# <span data-ttu-id="efc53-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="efc53-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="efc53-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="efc53-102">SYNOPSIS</span></span>
<span data-ttu-id="efc53-103">Annak vizsgálata, hogy egy egyéni tartomány hozzáadható-e egy végponthoz.</span><span class="sxs-lookup"><span data-stu-id="efc53-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="efc53-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="efc53-104">SYNTAX</span></span>

### <span data-ttu-id="efc53-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="efc53-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efc53-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efc53-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efc53-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="efc53-107">DESCRIPTION</span></span>
<span data-ttu-id="efc53-108">A **AzCdnCustomDomain-** parancsmag ellenőrzi, hogy egy egyéni tartomány hozzáadható-e egy végponthoz a CNAME megfeleltetés ellenőrzésével.</span><span class="sxs-lookup"><span data-stu-id="efc53-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="efc53-109">Példák</span><span class="sxs-lookup"><span data-stu-id="efc53-109">EXAMPLES</span></span>

## <span data-ttu-id="efc53-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="efc53-110">PARAMETERS</span></span>

### <span data-ttu-id="efc53-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="efc53-111">-CdnEndpoint</span></span>
<span data-ttu-id="efc53-112">Azt a végpontot adja meg, amelyhez hozzá szeretné adni az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="efc53-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="efc53-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="efc53-113">-CustomDomainHostName</span></span>
<span data-ttu-id="efc53-114">Az egyéni tartomány állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="efc53-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="efc53-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc53-115">-DefaultProfile</span></span>
<span data-ttu-id="efc53-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="efc53-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efc53-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="efc53-117">-EndpointName</span></span>
<span data-ttu-id="efc53-118">Annak a végpontnak a nevét adja meg, amelyhez hozzá szeretné adni az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="efc53-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="efc53-119">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="efc53-119">-ProfileName</span></span>
<span data-ttu-id="efc53-120">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="efc53-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="efc53-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc53-121">-ResourceGroupName</span></span>
<span data-ttu-id="efc53-122">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="efc53-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="efc53-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc53-123">CommonParameters</span></span>
<span data-ttu-id="efc53-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="efc53-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc53-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="efc53-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc53-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="efc53-126">INPUTS</span></span>

### <span data-ttu-id="efc53-127">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="efc53-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="efc53-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efc53-128">OUTPUTS</span></span>

### <span data-ttu-id="efc53-129">Microsoft. Azure. Command. CDN. models. Endpoint. PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="efc53-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="efc53-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="efc53-130">NOTES</span></span>

## <span data-ttu-id="efc53-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efc53-131">RELATED LINKS</span></span>

[<span data-ttu-id="efc53-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="efc53-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="efc53-133">Új – AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="efc53-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="efc53-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="efc53-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


