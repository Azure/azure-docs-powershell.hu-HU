---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: c3970b61d53b6afdd214aca5c4ca89c735377713
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836859"
---
# <span data-ttu-id="d2cb8-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d2cb8-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="d2cb8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d2cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="d2cb8-103">Tiltja az egyéni HTTPS-tartomány (elavult) beállítását.</span><span class="sxs-lookup"><span data-stu-id="d2cb8-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="d2cb8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d2cb8-104">SYNTAX</span></span>

### <span data-ttu-id="d2cb8-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d2cb8-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2cb8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2cb8-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2cb8-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d2cb8-107">DESCRIPTION</span></span>
<span data-ttu-id="d2cb8-108">A **disable-AzCdnCustomDomain** parancsmag letiltja a biztonságos HTTPS-kézbesítést egy CDN-beli egyéni tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="d2cb8-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="d2cb8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d2cb8-109">EXAMPLES</span></span>

### <span data-ttu-id="d2cb8-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d2cb8-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="d2cb8-111">Tiltsa le az egyéni tartomány HTTPS-kézbesítését.</span><span class="sxs-lookup"><span data-stu-id="d2cb8-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="d2cb8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d2cb8-112">PARAMETERS</span></span>

### <span data-ttu-id="d2cb8-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="d2cb8-113">-CustomDomainName</span></span>
<span data-ttu-id="d2cb8-114">Azure CDN egyéni tartomány megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="d2cb8-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="d2cb8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2cb8-115">-DefaultProfile</span></span>
<span data-ttu-id="d2cb8-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2cb8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2cb8-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d2cb8-117">-EndpointName</span></span>
<span data-ttu-id="d2cb8-118">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="d2cb8-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d2cb8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2cb8-119">-InputObject</span></span>
<span data-ttu-id="d2cb8-120">Az egyéni tartomány-objektum.</span><span class="sxs-lookup"><span data-stu-id="d2cb8-120">The custom domain object.</span></span>

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

### <span data-ttu-id="d2cb8-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2cb8-121">-PassThru</span></span>
<span data-ttu-id="d2cb8-122">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="d2cb8-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="d2cb8-123">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="d2cb8-123">-ProfileName</span></span>
<span data-ttu-id="d2cb8-124">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="d2cb8-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d2cb8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2cb8-125">-ResourceGroupName</span></span>
<span data-ttu-id="d2cb8-126">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="d2cb8-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="d2cb8-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="d2cb8-127">-Confirm</span></span>
<span data-ttu-id="d2cb8-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="d2cb8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2cb8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2cb8-129">-WhatIf</span></span>
<span data-ttu-id="d2cb8-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="d2cb8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2cb8-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2cb8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2cb8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2cb8-132">CommonParameters</span></span>
<span data-ttu-id="d2cb8-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d2cb8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2cb8-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2cb8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2cb8-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2cb8-135">INPUTS</span></span>

### <span data-ttu-id="d2cb8-136">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="d2cb8-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="d2cb8-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2cb8-137">OUTPUTS</span></span>

### <span data-ttu-id="d2cb8-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2cb8-138">System.Boolean</span></span>

## <span data-ttu-id="d2cb8-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d2cb8-139">NOTES</span></span>

## <span data-ttu-id="d2cb8-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2cb8-140">RELATED LINKS</span></span>
