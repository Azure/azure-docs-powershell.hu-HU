---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351665"
---
# <span data-ttu-id="1b51c-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1b51c-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="1b51c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b51c-102">SYNOPSIS</span></span>
<span data-ttu-id="1b51c-103">Letiltja az egyéni tartomány HTTPS-ét (elavult).</span><span class="sxs-lookup"><span data-stu-id="1b51c-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="1b51c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1b51c-104">SYNTAX</span></span>

### <span data-ttu-id="1b51c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1b51c-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b51c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b51c-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b51c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1b51c-107">DESCRIPTION</span></span>
<span data-ttu-id="1b51c-108">A **Disable-AzCdnCustomDomain** parancsmag letiltja egy egyéni CDN-tartomány biztonságos HTTPS-kézbesítését.</span><span class="sxs-lookup"><span data-stu-id="1b51c-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="1b51c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1b51c-109">EXAMPLES</span></span>

### <span data-ttu-id="1b51c-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="1b51c-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="1b51c-111">Tiltsa le az egyéni tartomány https-kézbesítését.</span><span class="sxs-lookup"><span data-stu-id="1b51c-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="1b51c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b51c-112">PARAMETERS</span></span>

### <span data-ttu-id="1b51c-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="1b51c-113">-CustomDomainName</span></span>
<span data-ttu-id="1b51c-114">Azure CDN egyéni tartomány megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="1b51c-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="1b51c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b51c-115">-DefaultProfile</span></span>
<span data-ttu-id="1b51c-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1b51c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b51c-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1b51c-117">-EndpointName</span></span>
<span data-ttu-id="1b51c-118">Azure CDN-végpont neve.</span><span class="sxs-lookup"><span data-stu-id="1b51c-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="1b51c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b51c-119">-InputObject</span></span>
<span data-ttu-id="1b51c-120">Az egyéni tartományobjektum.</span><span class="sxs-lookup"><span data-stu-id="1b51c-120">The custom domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b51c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b51c-121">-PassThru</span></span>
<span data-ttu-id="1b51c-122">Visszatérési objektum (ha meg van adva).</span><span class="sxs-lookup"><span data-stu-id="1b51c-122">Return object (if specified).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b51c-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1b51c-123">-ProfileName</span></span>
<span data-ttu-id="1b51c-124">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="1b51c-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="1b51c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b51c-125">-ResourceGroupName</span></span>
<span data-ttu-id="1b51c-126">Az Azure CDN-profil erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="1b51c-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="1b51c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b51c-127">-Confirm</span></span>
<span data-ttu-id="1b51c-128">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="1b51c-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b51c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b51c-129">-WhatIf</span></span>
<span data-ttu-id="1b51c-130">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="1b51c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b51c-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1b51c-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b51c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b51c-132">CommonParameters</span></span>
<span data-ttu-id="1b51c-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b51c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b51c-134">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b51c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b51c-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b51c-135">INPUTS</span></span>

### <span data-ttu-id="1b51c-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="1b51c-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="1b51c-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1b51c-137">OUTPUTS</span></span>

### <span data-ttu-id="1b51c-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1b51c-138">System.Boolean</span></span>

## <span data-ttu-id="1b51c-139">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1b51c-139">NOTES</span></span>

## <span data-ttu-id="1b51c-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1b51c-140">RELATED LINKS</span></span>
