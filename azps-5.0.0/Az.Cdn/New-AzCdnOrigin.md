---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186265"
---
# <span data-ttu-id="c74fa-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="c74fa-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="c74fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c74fa-102">SYNOPSIS</span></span>
<span data-ttu-id="c74fa-103">Új CDN-Origó létrehozása</span><span class="sxs-lookup"><span data-stu-id="c74fa-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="c74fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c74fa-104">SYNTAX</span></span>

### <span data-ttu-id="c74fa-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c74fa-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c74fa-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="c74fa-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c74fa-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c74fa-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c74fa-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c74fa-108">DESCRIPTION</span></span>
<span data-ttu-id="c74fa-109">A New-AzCdnOrigin új CDN-forrást fog létrehozni a megadott végponton belül.</span><span class="sxs-lookup"><span data-stu-id="c74fa-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="c74fa-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c74fa-110">EXAMPLES</span></span>

### <span data-ttu-id="c74fa-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="c74fa-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="c74fa-112">Ez a parancsmag új CDN-kezdőpontot hoz létre a megadott végponthoz.</span><span class="sxs-lookup"><span data-stu-id="c74fa-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="c74fa-113">A megadott állomásnevet a forrásként fogja használni.</span><span class="sxs-lookup"><span data-stu-id="c74fa-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="c74fa-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c74fa-114">PARAMETERS</span></span>

### <span data-ttu-id="c74fa-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="c74fa-115">-CdnOrigin</span></span>
<span data-ttu-id="c74fa-116">A CDN Origin objektuma.</span><span class="sxs-lookup"><span data-stu-id="c74fa-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c74fa-117">-DefaultProfile</span></span>
<span data-ttu-id="c74fa-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c74fa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c74fa-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c74fa-119">-EndpointName</span></span>
<span data-ttu-id="c74fa-120">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="c74fa-120">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-121">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="c74fa-121">-HostName</span></span>
<span data-ttu-id="c74fa-122">Azure CDN Origin Host Name (név)</span><span class="sxs-lookup"><span data-stu-id="c74fa-122">Azure CDN origin host name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="c74fa-123">-HttpPort</span></span>
<span data-ttu-id="c74fa-124">Azure CDN Origin http-port.</span><span class="sxs-lookup"><span data-stu-id="c74fa-124">Azure CDN origin http port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="c74fa-125">-HttpsPort</span></span>
<span data-ttu-id="c74fa-126">Azure CDN Origin HTTPS-port.</span><span class="sxs-lookup"><span data-stu-id="c74fa-126">Azure CDN origin https port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="c74fa-127">-OriginHostHeader</span></span>
<span data-ttu-id="c74fa-128">Azure CDN Origin Host fejléc.</span><span class="sxs-lookup"><span data-stu-id="c74fa-128">Azure CDN origin host header.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="c74fa-129">-OriginName</span></span>
<span data-ttu-id="c74fa-130">Azure CDN Origin név.</span><span class="sxs-lookup"><span data-stu-id="c74fa-130">Azure CDN origin name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-131">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="c74fa-131">-Priority</span></span>
<span data-ttu-id="c74fa-132">Azure CDN-forrás prioritása.</span><span class="sxs-lookup"><span data-stu-id="c74fa-132">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="c74fa-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="c74fa-134">A privát hivatkozáshoz való csatlakozáshoz a jóváhagyási kérelemben szerepeltetni kívánt egyéni üzenet.</span><span class="sxs-lookup"><span data-stu-id="c74fa-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="c74fa-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="c74fa-136">Azure CDN Origin privát hivatkozás helye.</span><span class="sxs-lookup"><span data-stu-id="c74fa-136">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="c74fa-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="c74fa-138">Azure CDN Origin Private link erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c74fa-138">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-139">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="c74fa-139">-ProfileName</span></span>
<span data-ttu-id="c74fa-140">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="c74fa-140">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c74fa-141">-ResourceGroupName</span></span>
<span data-ttu-id="c74fa-142">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="c74fa-142">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-143">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="c74fa-143">-Weight</span></span>
<span data-ttu-id="c74fa-144">Azure CDN származási súlya</span><span class="sxs-lookup"><span data-stu-id="c74fa-144">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74fa-145">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="c74fa-145">-Confirm</span></span>
<span data-ttu-id="c74fa-146">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="c74fa-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c74fa-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c74fa-147">-WhatIf</span></span>
<span data-ttu-id="c74fa-148">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="c74fa-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c74fa-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="c74fa-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c74fa-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c74fa-150">CommonParameters</span></span>
<span data-ttu-id="c74fa-151">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c74fa-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c74fa-152">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c74fa-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c74fa-153">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c74fa-153">INPUTS</span></span>

### <span data-ttu-id="c74fa-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="c74fa-154">None</span></span>

## <span data-ttu-id="c74fa-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c74fa-155">OUTPUTS</span></span>

### <span data-ttu-id="c74fa-156">Microsoft. Azure. Command. CDN. models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="c74fa-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="c74fa-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c74fa-157">NOTES</span></span>

## <span data-ttu-id="c74fa-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c74fa-158">RELATED LINKS</span></span>
