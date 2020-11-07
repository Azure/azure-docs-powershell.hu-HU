---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 58ad23747583162643ee3a1ee7b0547311adcadf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671426"
---
# <span data-ttu-id="abd45-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="abd45-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="abd45-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="abd45-102">SYNOPSIS</span></span>
<span data-ttu-id="abd45-103">Letiltja az egyéni tartomány HTTPS-tartományát.</span><span class="sxs-lookup"><span data-stu-id="abd45-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="abd45-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="abd45-104">SYNTAX</span></span>

### <span data-ttu-id="abd45-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="abd45-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abd45-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abd45-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abd45-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abd45-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abd45-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="abd45-108">DESCRIPTION</span></span>
<span data-ttu-id="abd45-109">A **disable-AzCdnCustomDomainHttps** parancsmag letiltja a biztonságos HTTPS-kézbesítést egy CDN-beli egyéni tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="abd45-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="abd45-110">Példák</span><span class="sxs-lookup"><span data-stu-id="abd45-110">EXAMPLES</span></span>

### <span data-ttu-id="abd45-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="abd45-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="abd45-112">Tiltsa le az egyéni tartomány biztonságos kézbesítését.</span><span class="sxs-lookup"><span data-stu-id="abd45-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="abd45-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="abd45-113">PARAMETERS</span></span>

### <span data-ttu-id="abd45-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="abd45-114">-CustomDomainName</span></span>
<span data-ttu-id="abd45-115">Azure CDN egyéni tartomány megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="abd45-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="abd45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd45-116">-DefaultProfile</span></span>
<span data-ttu-id="abd45-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="abd45-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abd45-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="abd45-118">-EndpointName</span></span>
<span data-ttu-id="abd45-119">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="abd45-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="abd45-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abd45-120">-InputObject</span></span>
<span data-ttu-id="abd45-121">Az egyéni tartomány-objektum.</span><span class="sxs-lookup"><span data-stu-id="abd45-121">The custom domain object.</span></span>

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

### <span data-ttu-id="abd45-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abd45-122">-PassThru</span></span>
<span data-ttu-id="abd45-123">Ha meg van adva a visszatérési objektum</span><span class="sxs-lookup"><span data-stu-id="abd45-123">Return object if specified.</span></span>

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

### <span data-ttu-id="abd45-124">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="abd45-124">-ProfileName</span></span>
<span data-ttu-id="abd45-125">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="abd45-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="abd45-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abd45-126">-ResourceGroupName</span></span>
<span data-ttu-id="abd45-127">Az Azure CDN-profil erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="abd45-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="abd45-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abd45-128">-ResourceId</span></span>
<span data-ttu-id="abd45-129">Az egyéni tartomány ResourceId</span><span class="sxs-lookup"><span data-stu-id="abd45-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="abd45-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="abd45-130">-Confirm</span></span>
<span data-ttu-id="abd45-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="abd45-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abd45-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abd45-132">-WhatIf</span></span>
<span data-ttu-id="abd45-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="abd45-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abd45-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="abd45-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abd45-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd45-135">CommonParameters</span></span>
<span data-ttu-id="abd45-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="abd45-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd45-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abd45-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd45-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="abd45-138">INPUTS</span></span>

### <span data-ttu-id="abd45-139">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="abd45-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="abd45-140">System. String</span><span class="sxs-lookup"><span data-stu-id="abd45-140">System.String</span></span>

## <span data-ttu-id="abd45-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="abd45-141">OUTPUTS</span></span>

### <span data-ttu-id="abd45-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="abd45-142">System.Boolean</span></span>

## <span data-ttu-id="abd45-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="abd45-143">NOTES</span></span>

## <span data-ttu-id="abd45-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="abd45-144">RELATED LINKS</span></span>
