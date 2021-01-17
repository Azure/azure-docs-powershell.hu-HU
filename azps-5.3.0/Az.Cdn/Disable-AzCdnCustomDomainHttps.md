---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: be3e4d0437e24a282c1933cf82e1818dd9f88221
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480960"
---
# <span data-ttu-id="66aff-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="66aff-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="66aff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66aff-102">SYNOPSIS</span></span>
<span data-ttu-id="66aff-103">Letiltja az egyéni tartomány HTTPS-ét.</span><span class="sxs-lookup"><span data-stu-id="66aff-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="66aff-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="66aff-104">SYNTAX</span></span>

### <span data-ttu-id="66aff-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="66aff-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66aff-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66aff-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66aff-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66aff-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66aff-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="66aff-108">DESCRIPTION</span></span>
<span data-ttu-id="66aff-109">A **Disable-AzCdnCustomDomainHttps** parancsmag letiltja egy egyéni CDN-tartomány biztonságos HTTPS-kézbesítését.</span><span class="sxs-lookup"><span data-stu-id="66aff-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="66aff-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="66aff-110">EXAMPLES</span></span>

### <span data-ttu-id="66aff-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="66aff-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="66aff-112">Tiltsa le az egyéni tartomány biztonságos kézbesítését.</span><span class="sxs-lookup"><span data-stu-id="66aff-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="66aff-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66aff-113">PARAMETERS</span></span>

### <span data-ttu-id="66aff-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="66aff-114">-CustomDomainName</span></span>
<span data-ttu-id="66aff-115">Azure CDN egyéni tartomány megjelenítendő neve.</span><span class="sxs-lookup"><span data-stu-id="66aff-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="66aff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66aff-116">-DefaultProfile</span></span>
<span data-ttu-id="66aff-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66aff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66aff-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="66aff-118">-EndpointName</span></span>
<span data-ttu-id="66aff-119">Azure CDN-végpont neve.</span><span class="sxs-lookup"><span data-stu-id="66aff-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="66aff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66aff-120">-InputObject</span></span>
<span data-ttu-id="66aff-121">Az egyéni tartományobjektum.</span><span class="sxs-lookup"><span data-stu-id="66aff-121">The custom domain object.</span></span>

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

### <span data-ttu-id="66aff-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66aff-122">-PassThru</span></span>
<span data-ttu-id="66aff-123">Visszatérési objektum, ha meg van adva.</span><span class="sxs-lookup"><span data-stu-id="66aff-123">Return object if specified.</span></span>

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

### <span data-ttu-id="66aff-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="66aff-124">-ProfileName</span></span>
<span data-ttu-id="66aff-125">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="66aff-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="66aff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66aff-126">-ResourceGroupName</span></span>
<span data-ttu-id="66aff-127">Az Azure CDN-profil erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="66aff-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="66aff-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66aff-128">-ResourceId</span></span>
<span data-ttu-id="66aff-129">Az egyéni tartomány Erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="66aff-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="66aff-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66aff-130">-Confirm</span></span>
<span data-ttu-id="66aff-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="66aff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66aff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66aff-132">-WhatIf</span></span>
<span data-ttu-id="66aff-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="66aff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66aff-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="66aff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66aff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66aff-135">CommonParameters</span></span>
<span data-ttu-id="66aff-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66aff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66aff-137">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66aff-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66aff-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="66aff-138">INPUTS</span></span>

### <span data-ttu-id="66aff-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="66aff-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="66aff-140">System.String</span><span class="sxs-lookup"><span data-stu-id="66aff-140">System.String</span></span>

## <span data-ttu-id="66aff-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66aff-141">OUTPUTS</span></span>

### <span data-ttu-id="66aff-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="66aff-142">System.Boolean</span></span>

## <span data-ttu-id="66aff-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="66aff-143">NOTES</span></span>

## <span data-ttu-id="66aff-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66aff-144">RELATED LINKS</span></span>
