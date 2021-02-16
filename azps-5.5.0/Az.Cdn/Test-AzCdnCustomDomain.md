---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 8C4E824F-FB4A-4DE7-8FD9-3FDA3848F25C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/test-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Test-AzCdnCustomDomain.md
ms.openlocfilehash: 8ceb1fe02ba4a7d5cf4435ac79d404b331b58ea9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162371"
---
# <span data-ttu-id="32819-101">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="32819-101">Test-AzCdnCustomDomain</span></span>

## <span data-ttu-id="32819-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32819-102">SYNOPSIS</span></span>
<span data-ttu-id="32819-103">Annak ellenőrzése, hogy hozzáadható-e egy egyéni tartomány egy végponthoz.</span><span class="sxs-lookup"><span data-stu-id="32819-103">Checks whether a custom domain can be added to an endpoint.</span></span>

## <span data-ttu-id="32819-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="32819-104">SYNTAX</span></span>

### <span data-ttu-id="32819-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="32819-105">ByFieldsParameterSet (Default)</span></span>
```
Test-AzCdnCustomDomain -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -CustomDomainHostName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32819-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32819-106">ByObjectParameterSet</span></span>
```
Test-AzCdnCustomDomain -CdnEndpoint <PSEndpoint> -CustomDomainHostName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32819-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="32819-107">DESCRIPTION</span></span>
<span data-ttu-id="32819-108">A **Test-AzCdnCustomDomain** parancsmag ellenőrzi, hogy hozzáadható-e egy egyéni tartomány egy végponthoz a CName leképezés érvényességének igazolásával.</span><span class="sxs-lookup"><span data-stu-id="32819-108">The **Test-AzCdnCustomDomain** cmdlet checks whether a custom domain can be added to an endpoint by validating the CName mapping.</span></span>

## <span data-ttu-id="32819-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="32819-109">EXAMPLES</span></span>

## <span data-ttu-id="32819-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32819-110">PARAMETERS</span></span>

### <span data-ttu-id="32819-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="32819-111">-CdnEndpoint</span></span>
<span data-ttu-id="32819-112">Megadja azt a végpontot, amelyhez hozzá szeretné adni az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="32819-112">Specifies the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="32819-113">-CustomDomainHostName</span><span class="sxs-lookup"><span data-stu-id="32819-113">-CustomDomainHostName</span></span>
<span data-ttu-id="32819-114">Az egyéni tartomány állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32819-114">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="32819-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32819-115">-DefaultProfile</span></span>
<span data-ttu-id="32819-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="32819-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32819-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="32819-117">-EndpointName</span></span>
<span data-ttu-id="32819-118">Megadja annak a végpontnak a nevét, amelyhez hozzá szeretné adni az egyéni tartományt.</span><span class="sxs-lookup"><span data-stu-id="32819-118">Specifies the name of the endpoint to which you want to add the custom domain.</span></span>

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

### <span data-ttu-id="32819-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="32819-119">-ProfileName</span></span>
<span data-ttu-id="32819-120">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32819-120">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="32819-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32819-121">-ResourceGroupName</span></span>
<span data-ttu-id="32819-122">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="32819-122">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="32819-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32819-123">CommonParameters</span></span>
<span data-ttu-id="32819-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32819-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32819-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32819-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32819-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32819-126">INPUTS</span></span>

### <span data-ttu-id="32819-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="32819-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="32819-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32819-128">OUTPUTS</span></span>

### <span data-ttu-id="32819-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span><span class="sxs-lookup"><span data-stu-id="32819-129">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSValidateCustomDomainOutput</span></span>

## <span data-ttu-id="32819-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="32819-130">NOTES</span></span>

## <span data-ttu-id="32819-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32819-131">RELATED LINKS</span></span>

[<span data-ttu-id="32819-132">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="32819-132">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="32819-133">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="32819-133">New-AzCdnCustomDomain</span></span>](./New-AzCdnCustomDomain.md)

[<span data-ttu-id="32819-134">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="32819-134">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)


