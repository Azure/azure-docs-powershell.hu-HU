---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187644"
---
# <span data-ttu-id="a41da-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="a41da-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="a41da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a41da-102">SYNOPSIS</span></span>
<span data-ttu-id="a41da-103">Egy CDN-származási kiszolgáló frissítése</span><span class="sxs-lookup"><span data-stu-id="a41da-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="a41da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a41da-104">SYNTAX</span></span>

### <span data-ttu-id="a41da-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a41da-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a41da-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="a41da-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a41da-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a41da-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a41da-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a41da-108">DESCRIPTION</span></span>
<span data-ttu-id="a41da-109">A **set-AzCdnOrigin** parancsmag frissíti az Azure Content Delivery Network (CDN) Origin kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="a41da-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="a41da-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a41da-110">EXAMPLES</span></span>

## <span data-ttu-id="a41da-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a41da-111">PARAMETERS</span></span>

### <span data-ttu-id="a41da-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="a41da-112">-CdnOrigin</span></span>
<span data-ttu-id="a41da-113">A parancsmag által frissített forráskiszolgálón adja meg.</span><span class="sxs-lookup"><span data-stu-id="a41da-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="a41da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a41da-114">-DefaultProfile</span></span>
<span data-ttu-id="a41da-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a41da-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a41da-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a41da-116">-EndpointName</span></span>
<span data-ttu-id="a41da-117">Azure CDN végpont neve.</span><span class="sxs-lookup"><span data-stu-id="a41da-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="a41da-118">-HostName (állomásnév)</span><span class="sxs-lookup"><span data-stu-id="a41da-118">-HostName</span></span>
<span data-ttu-id="a41da-119">Azure CDN Origin Host Name (név)</span><span class="sxs-lookup"><span data-stu-id="a41da-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="a41da-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="a41da-120">-HttpPort</span></span>
<span data-ttu-id="a41da-121">Azure CDN Origin http-port.</span><span class="sxs-lookup"><span data-stu-id="a41da-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="a41da-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="a41da-122">-HttpsPort</span></span>
<span data-ttu-id="a41da-123">Azure CDN Origin HTTPS-port.</span><span class="sxs-lookup"><span data-stu-id="a41da-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="a41da-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="a41da-124">-OriginHostHeader</span></span>
<span data-ttu-id="a41da-125">Azure CDN Origin Host fejléc.</span><span class="sxs-lookup"><span data-stu-id="a41da-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="a41da-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="a41da-126">-OriginName</span></span>
<span data-ttu-id="a41da-127">Azure CDN Origin név.</span><span class="sxs-lookup"><span data-stu-id="a41da-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="a41da-128">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="a41da-128">-Priority</span></span>
<span data-ttu-id="a41da-129">Azure CDN-forrás prioritása.</span><span class="sxs-lookup"><span data-stu-id="a41da-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="a41da-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="a41da-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="a41da-131">A privát hivatkozáshoz való csatlakozáshoz a jóváhagyási kérelemben szerepeltetni kívánt egyéni üzenet.</span><span class="sxs-lookup"><span data-stu-id="a41da-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="a41da-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="a41da-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="a41da-133">Azure CDN Origin privát hivatkozás helye.</span><span class="sxs-lookup"><span data-stu-id="a41da-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="a41da-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="a41da-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="a41da-135">Azure CDN Origin Private link erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="a41da-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="a41da-136">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="a41da-136">-ProfileName</span></span>
<span data-ttu-id="a41da-137">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="a41da-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="a41da-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a41da-138">-ResourceGroupName</span></span>
<span data-ttu-id="a41da-139">Az Azure CDN-profil erőforrás csoportja.</span><span class="sxs-lookup"><span data-stu-id="a41da-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="a41da-140">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="a41da-140">-Weight</span></span>
<span data-ttu-id="a41da-141">Azure CDN származási súlya</span><span class="sxs-lookup"><span data-stu-id="a41da-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="a41da-142">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a41da-142">-Confirm</span></span>
<span data-ttu-id="a41da-143">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a41da-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a41da-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a41da-144">-WhatIf</span></span>
<span data-ttu-id="a41da-145">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a41da-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a41da-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a41da-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a41da-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a41da-147">CommonParameters</span></span>
<span data-ttu-id="a41da-148">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a41da-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a41da-149">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="a41da-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a41da-150">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a41da-150">INPUTS</span></span>

### <span data-ttu-id="a41da-151">Microsoft. Azure. Command. CDN. models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="a41da-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="a41da-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a41da-152">OUTPUTS</span></span>

### <span data-ttu-id="a41da-153">Microsoft. Azure. Command. CDN. models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="a41da-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="a41da-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a41da-154">NOTES</span></span>

## <span data-ttu-id="a41da-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a41da-155">RELATED LINKS</span></span>

[<span data-ttu-id="a41da-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="a41da-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


