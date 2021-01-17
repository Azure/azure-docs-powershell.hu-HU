---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477970"
---
# <span data-ttu-id="75c2b-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="75c2b-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="75c2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="75c2b-103">Frissíti a CDN-forráskiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="75c2b-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="75c2b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="75c2b-104">SYNTAX</span></span>

### <span data-ttu-id="75c2b-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="75c2b-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75c2b-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="75c2b-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75c2b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="75c2b-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75c2b-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="75c2b-108">DESCRIPTION</span></span>
<span data-ttu-id="75c2b-109">A **Set-AzCdnOrigin** parancsmag frissíti az Azure Content Delivery Network (CDN) forráskiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="75c2b-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="75c2b-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="75c2b-110">EXAMPLES</span></span>

## <span data-ttu-id="75c2b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75c2b-111">PARAMETERS</span></span>

### <span data-ttu-id="75c2b-112">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="75c2b-112">-CdnOrigin</span></span>
<span data-ttu-id="75c2b-113">Azt a forráskiszolgálót adja meg, amely a parancsmagot frissíti.</span><span class="sxs-lookup"><span data-stu-id="75c2b-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="75c2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c2b-114">-DefaultProfile</span></span>
<span data-ttu-id="75c2b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="75c2b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75c2b-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="75c2b-116">-EndpointName</span></span>
<span data-ttu-id="75c2b-117">Azure CDN-végpont neve.</span><span class="sxs-lookup"><span data-stu-id="75c2b-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="75c2b-118">-HostName</span><span class="sxs-lookup"><span data-stu-id="75c2b-118">-HostName</span></span>
<span data-ttu-id="75c2b-119">Azure CDN-forrás állomásneve.</span><span class="sxs-lookup"><span data-stu-id="75c2b-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="75c2b-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="75c2b-120">-HttpPort</span></span>
<span data-ttu-id="75c2b-121">Azure CDN-forrás http-port.</span><span class="sxs-lookup"><span data-stu-id="75c2b-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="75c2b-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="75c2b-122">-HttpsPort</span></span>
<span data-ttu-id="75c2b-123">Azure CDN origin https port.</span><span class="sxs-lookup"><span data-stu-id="75c2b-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="75c2b-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="75c2b-124">-OriginHostHeader</span></span>
<span data-ttu-id="75c2b-125">Azure CDN-forrás gazdafejléce.</span><span class="sxs-lookup"><span data-stu-id="75c2b-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="75c2b-126">-OriginName</span><span class="sxs-lookup"><span data-stu-id="75c2b-126">-OriginName</span></span>
<span data-ttu-id="75c2b-127">Azure CDN-forrás neve.</span><span class="sxs-lookup"><span data-stu-id="75c2b-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="75c2b-128">-Priority</span><span class="sxs-lookup"><span data-stu-id="75c2b-128">-Priority</span></span>
<span data-ttu-id="75c2b-129">Azure CDN-forrás prioritása.</span><span class="sxs-lookup"><span data-stu-id="75c2b-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="75c2b-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="75c2b-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="75c2b-131">Egy egyéni üzenet, amely szerepelni fog a jóváhagyási kérelemben a privát hivatkozáshoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="75c2b-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="75c2b-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="75c2b-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="75c2b-133">Azure CDN-forrás privát hivatkozásának helye.</span><span class="sxs-lookup"><span data-stu-id="75c2b-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="75c2b-134">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="75c2b-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="75c2b-135">Azure CDN-forrás privát hivatkozáserőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="75c2b-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="75c2b-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="75c2b-136">-ProfileName</span></span>
<span data-ttu-id="75c2b-137">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="75c2b-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="75c2b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75c2b-138">-ResourceGroupName</span></span>
<span data-ttu-id="75c2b-139">Az Azure CDN-profil erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="75c2b-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="75c2b-140">-Weight</span><span class="sxs-lookup"><span data-stu-id="75c2b-140">-Weight</span></span>
<span data-ttu-id="75c2b-141">Azure CDN origin weight.</span><span class="sxs-lookup"><span data-stu-id="75c2b-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="75c2b-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75c2b-142">-Confirm</span></span>
<span data-ttu-id="75c2b-143">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="75c2b-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75c2b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75c2b-144">-WhatIf</span></span>
<span data-ttu-id="75c2b-145">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="75c2b-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75c2b-146">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="75c2b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75c2b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c2b-147">CommonParameters</span></span>
<span data-ttu-id="75c2b-148">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75c2b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c2b-149">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="75c2b-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c2b-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75c2b-150">INPUTS</span></span>

### <span data-ttu-id="75c2b-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="75c2b-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="75c2b-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="75c2b-152">OUTPUTS</span></span>

### <span data-ttu-id="75c2b-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="75c2b-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="75c2b-154">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="75c2b-154">NOTES</span></span>

## <span data-ttu-id="75c2b-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="75c2b-155">RELATED LINKS</span></span>

[<span data-ttu-id="75c2b-156">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="75c2b-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


