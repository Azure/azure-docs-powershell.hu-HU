---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: be3e4d0437e24a282c1933cf82e1818dd9f88221
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351618"
---
# <span data-ttu-id="890b4-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="890b4-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="890b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="890b4-102">SYNOPSIS</span></span>
<span data-ttu-id="890b4-103">Letiltja az egyéni tartomány HTTPS-ét.</span><span class="sxs-lookup"><span data-stu-id="890b4-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="890b4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="890b4-104">SYNTAX</span></span>

### <span data-ttu-id="890b4-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="890b4-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="890b4-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="890b4-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="890b4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="890b4-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="890b4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="890b4-108">DESCRIPTION</span></span>
<span data-ttu-id="890b4-109">A **Disable-AzCdnCustomDomainHttps** parancsmag letiltja egy egyéni CDN-tartomány biztonságos HTTPS-kézbesítését.</span><span class="sxs-lookup"><span data-stu-id="890b4-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="890b4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="890b4-110">EXAMPLES</span></span>

### <span data-ttu-id="890b4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="890b4-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="890b4-112">Tiltsa le az egyéni tartomány biztonságos kézbesítését.</span><span class="sxs-lookup"><span data-stu-id="890b4-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="890b4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="890b4-113">PARAMETERS</span></span>

### <span data-ttu-id="890b4-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="890b4-114">-CustomDomainName</span></span>
<span data-ttu-id="890b4-115">Azure CDN egyéni tartomány megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="890b4-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="890b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="890b4-116">-DefaultProfile</span></span>
<span data-ttu-id="890b4-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="890b4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="890b4-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="890b4-118">-EndpointName</span></span>
<span data-ttu-id="890b4-119">Azure CDN-végpont neve.</span><span class="sxs-lookup"><span data-stu-id="890b4-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="890b4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="890b4-120">-InputObject</span></span>
<span data-ttu-id="890b4-121">Az egyéni tartományobjektum.</span><span class="sxs-lookup"><span data-stu-id="890b4-121">The custom domain object.</span></span>

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

### <span data-ttu-id="890b4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="890b4-122">-PassThru</span></span>
<span data-ttu-id="890b4-123">Visszatérési objektum, ha meg van adva.</span><span class="sxs-lookup"><span data-stu-id="890b4-123">Return object if specified.</span></span>

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

### <span data-ttu-id="890b4-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="890b4-124">-ProfileName</span></span>
<span data-ttu-id="890b4-125">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="890b4-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="890b4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="890b4-126">-ResourceGroupName</span></span>
<span data-ttu-id="890b4-127">Az Azure CDN-profil erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="890b4-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="890b4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="890b4-128">-ResourceId</span></span>
<span data-ttu-id="890b4-129">Az egyéni tartomány Erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="890b4-129">ResourceId of the Custom Domain</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="890b4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="890b4-130">-Confirm</span></span>
<span data-ttu-id="890b4-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="890b4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="890b4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="890b4-132">-WhatIf</span></span>
<span data-ttu-id="890b4-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="890b4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="890b4-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="890b4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="890b4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="890b4-135">CommonParameters</span></span>
<span data-ttu-id="890b4-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="890b4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="890b4-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="890b4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="890b4-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="890b4-138">INPUTS</span></span>

### <span data-ttu-id="890b4-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="890b4-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="890b4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="890b4-140">System.String</span></span>

## <span data-ttu-id="890b4-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="890b4-141">OUTPUTS</span></span>

### <span data-ttu-id="890b4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="890b4-142">System.Boolean</span></span>

## <span data-ttu-id="890b4-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="890b4-143">NOTES</span></span>

## <span data-ttu-id="890b4-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="890b4-144">RELATED LINKS</span></span>
