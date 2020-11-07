---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 87c6928b6b1a8863bdde7126b782d07d4c496207
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671424"
---
# <span data-ttu-id="7114b-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="7114b-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="7114b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7114b-102">SYNOPSIS</span></span>
<span data-ttu-id="7114b-103">Engedélyezi az egyéni HTTPS-t.</span><span class="sxs-lookup"><span data-stu-id="7114b-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="7114b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7114b-104">SYNTAX</span></span>

### <span data-ttu-id="7114b-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7114b-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7114b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7114b-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7114b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7114b-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7114b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7114b-108">DESCRIPTION</span></span>
<span data-ttu-id="7114b-109">Az **enable-AzCdnCustomDomainHttps** parancsmag lehetővé teszi a biztonságos HTTPS-kézbesítést a CDN egyéni tartományában.</span><span class="sxs-lookup"><span data-stu-id="7114b-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="7114b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="7114b-110">EXAMPLES</span></span>

### <span data-ttu-id="7114b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="7114b-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="7114b-112">Engedélyezze az egyéni tartomány biztonságos kézbesítését.</span><span class="sxs-lookup"><span data-stu-id="7114b-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="7114b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7114b-113">PARAMETERS</span></span>

### <span data-ttu-id="7114b-114">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="7114b-114">-CustomDomainName</span></span>
<span data-ttu-id="7114b-115">Azure CDN egyéni tartomány megjelenítendő neve</span><span class="sxs-lookup"><span data-stu-id="7114b-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="7114b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7114b-116">-DefaultProfile</span></span>
<span data-ttu-id="7114b-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7114b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7114b-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7114b-118">-EndpointName</span></span>
<span data-ttu-id="7114b-119">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="7114b-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="7114b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7114b-120">-InputObject</span></span>
<span data-ttu-id="7114b-121">Az egyéni tartomány-objektum.</span><span class="sxs-lookup"><span data-stu-id="7114b-121">The custom domain object.</span></span>

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

### <span data-ttu-id="7114b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7114b-122">-PassThru</span></span>
<span data-ttu-id="7114b-123">Ha meg van adva a visszatérési objektum</span><span class="sxs-lookup"><span data-stu-id="7114b-123">Return object if specified.</span></span>

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

### <span data-ttu-id="7114b-124">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="7114b-124">-ProfileName</span></span>
<span data-ttu-id="7114b-125">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="7114b-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="7114b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7114b-126">-ResourceGroupName</span></span>
<span data-ttu-id="7114b-127">Az Azure CDN-profil erőforrás csoportja</span><span class="sxs-lookup"><span data-stu-id="7114b-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="7114b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7114b-128">-ResourceId</span></span>
<span data-ttu-id="7114b-129">Az egyéni tartomány ResourceId</span><span class="sxs-lookup"><span data-stu-id="7114b-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="7114b-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7114b-130">-Confirm</span></span>
<span data-ttu-id="7114b-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7114b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7114b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7114b-132">-WhatIf</span></span>
<span data-ttu-id="7114b-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7114b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7114b-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7114b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7114b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7114b-135">CommonParameters</span></span>
<span data-ttu-id="7114b-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7114b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7114b-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7114b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7114b-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7114b-138">INPUTS</span></span>

### <span data-ttu-id="7114b-139">Microsoft. Azure. Command. CDN. models. CustomDomain. PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="7114b-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="7114b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7114b-140">System.String</span></span>

## <span data-ttu-id="7114b-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7114b-141">OUTPUTS</span></span>

### <span data-ttu-id="7114b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7114b-142">System.Boolean</span></span>

## <span data-ttu-id="7114b-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7114b-143">NOTES</span></span>

## <span data-ttu-id="7114b-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7114b-144">RELATED LINKS</span></span>
