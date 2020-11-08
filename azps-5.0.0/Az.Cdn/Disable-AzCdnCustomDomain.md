---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 3352991d73bcef2e4f5b6475c9c71d5f48eaa526
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194925"
---
# <span data-ttu-id="a1187-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a1187-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="a1187-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a1187-102">SYNOPSIS</span></span>
<span data-ttu-id="a1187-103">Tiltja az egyéni HTTPS-tartomány (elavult) beállítását.</span><span class="sxs-lookup"><span data-stu-id="a1187-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="a1187-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a1187-104">SYNTAX</span></span>

### <span data-ttu-id="a1187-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a1187-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1187-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1187-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1187-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a1187-107">DESCRIPTION</span></span>
<span data-ttu-id="a1187-108">A **disable-AzCdnCustomDomain** parancsmag letiltja a biztonságos HTTPS-kézbesítést egy CDN-beli egyéni tartományhoz.</span><span class="sxs-lookup"><span data-stu-id="a1187-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="a1187-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a1187-109">EXAMPLES</span></span>

### <span data-ttu-id="a1187-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="a1187-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="a1187-111">Tiltsa le az egyéni tartomány HTTPS-kézbesítését.</span><span class="sxs-lookup"><span data-stu-id="a1187-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="a1187-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a1187-112">PARAMETERS</span></span>

### <span data-ttu-id="a1187-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="a1187-113">-CustomDomainName</span></span>
<span data-ttu-id="a1187-114">Azure CDN egyéni tartomány megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="a1187-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="a1187-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1187-115">-DefaultProfile</span></span>
<span data-ttu-id="a1187-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a1187-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1187-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a1187-117">-EndpointName</span></span>
<span data-ttu-id="a1187-118">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="a1187-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="a1187-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1187-119">-InputObject</span></span>
<span data-ttu-id="a1187-120">Az egyéni tartomány-objektum.</span><span class="sxs-lookup"><span data-stu-id="a1187-120">The custom domain object.</span></span>

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

### <span data-ttu-id="a1187-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1187-121">-PassThru</span></span>
<span data-ttu-id="a1187-122">Visszatérési objektum (ha meg van adva)</span><span class="sxs-lookup"><span data-stu-id="a1187-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="a1187-123">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="a1187-123">-ProfileName</span></span>
<span data-ttu-id="a1187-124">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="a1187-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="a1187-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1187-125">-ResourceGroupName</span></span>
<span data-ttu-id="a1187-126">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="a1187-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="a1187-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a1187-127">-Confirm</span></span>
<span data-ttu-id="a1187-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a1187-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1187-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1187-129">-WhatIf</span></span>
<span data-ttu-id="a1187-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a1187-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1187-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a1187-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1187-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1187-132">CommonParameters</span></span>
<span data-ttu-id="a1187-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a1187-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1187-134">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a1187-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1187-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1187-135">INPUTS</span></span>

### <span data-ttu-id="a1187-136">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="a1187-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="a1187-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a1187-137">OUTPUTS</span></span>

### <span data-ttu-id="a1187-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1187-138">System.Boolean</span></span>

## <span data-ttu-id="a1187-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a1187-139">NOTES</span></span>

## <span data-ttu-id="a1187-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a1187-140">RELATED LINKS</span></span>