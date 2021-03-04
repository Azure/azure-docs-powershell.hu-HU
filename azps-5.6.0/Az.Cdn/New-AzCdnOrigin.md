---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: cc7350fb76091d3bf2f8bdab5c037a5afbe8b57a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934322"
---
# <span data-ttu-id="5f291-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5f291-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="5f291-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f291-102">SYNOPSIS</span></span>
<span data-ttu-id="5f291-103">Új CDN-forrás létrehozása</span><span class="sxs-lookup"><span data-stu-id="5f291-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="5f291-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5f291-104">SYNTAX</span></span>

### <span data-ttu-id="5f291-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5f291-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f291-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f291-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f291-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f291-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f291-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5f291-108">DESCRIPTION</span></span>
<span data-ttu-id="5f291-109">A New-AzCdnOrigin létre fog hozni egy új CDN-forrást a megadott végponton belül.</span><span class="sxs-lookup"><span data-stu-id="5f291-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="5f291-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5f291-110">EXAMPLES</span></span>

### <span data-ttu-id="5f291-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="5f291-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="5f291-112">Ez a parancsmag új CDN-forrást hoz létre a megadott végponthoz.</span><span class="sxs-lookup"><span data-stu-id="5f291-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="5f291-113">Forrásként a megadott állomásnevet fogja használni.</span><span class="sxs-lookup"><span data-stu-id="5f291-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="5f291-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f291-114">PARAMETERS</span></span>

### <span data-ttu-id="5f291-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5f291-115">-CdnOrigin</span></span>
<span data-ttu-id="5f291-116">A CDN-forrásobjektum.</span><span class="sxs-lookup"><span data-stu-id="5f291-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="5f291-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f291-117">-DefaultProfile</span></span>
<span data-ttu-id="5f291-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5f291-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f291-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5f291-119">-EndpointName</span></span>
<span data-ttu-id="5f291-120">Azure CDN-végpont neve.</span><span class="sxs-lookup"><span data-stu-id="5f291-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="5f291-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="5f291-121">-HostName</span></span>
<span data-ttu-id="5f291-122">Azure CDN-forrás állomásneve.</span><span class="sxs-lookup"><span data-stu-id="5f291-122">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="5f291-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="5f291-123">-HttpPort</span></span>
<span data-ttu-id="5f291-124">Azure CDN-forrás http-port.</span><span class="sxs-lookup"><span data-stu-id="5f291-124">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="5f291-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="5f291-125">-HttpsPort</span></span>
<span data-ttu-id="5f291-126">Azure CDN origin https port.</span><span class="sxs-lookup"><span data-stu-id="5f291-126">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="5f291-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="5f291-127">-OriginHostHeader</span></span>
<span data-ttu-id="5f291-128">Azure CDN-forrás gazdafejléce.</span><span class="sxs-lookup"><span data-stu-id="5f291-128">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="5f291-129">-OriginName</span><span class="sxs-lookup"><span data-stu-id="5f291-129">-OriginName</span></span>
<span data-ttu-id="5f291-130">Azure CDN-forrás neve.</span><span class="sxs-lookup"><span data-stu-id="5f291-130">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="5f291-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="5f291-131">-Priority</span></span>
<span data-ttu-id="5f291-132">Azure CDN-forrás prioritása.</span><span class="sxs-lookup"><span data-stu-id="5f291-132">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="5f291-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="5f291-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="5f291-134">Egy egyéni üzenet, amely szerepelni fog a jóváhagyási kérelemben a privát hivatkozáshoz való csatlakozáshoz.</span><span class="sxs-lookup"><span data-stu-id="5f291-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="5f291-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="5f291-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="5f291-136">Azure CDN-forrás privát hivatkozásának helye.</span><span class="sxs-lookup"><span data-stu-id="5f291-136">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="5f291-137">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="5f291-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="5f291-138">Azure CDN-forrás privát hivatkozáserőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="5f291-138">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="5f291-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5f291-139">-ProfileName</span></span>
<span data-ttu-id="5f291-140">Azure CDN-profil neve.</span><span class="sxs-lookup"><span data-stu-id="5f291-140">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="5f291-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f291-141">-ResourceGroupName</span></span>
<span data-ttu-id="5f291-142">Az Azure CDN-profil erőforráscsoportja.</span><span class="sxs-lookup"><span data-stu-id="5f291-142">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="5f291-143">-Weight</span><span class="sxs-lookup"><span data-stu-id="5f291-143">-Weight</span></span>
<span data-ttu-id="5f291-144">Azure CDN origin weight.</span><span class="sxs-lookup"><span data-stu-id="5f291-144">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="5f291-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f291-145">-Confirm</span></span>
<span data-ttu-id="5f291-146">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="5f291-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f291-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f291-147">-WhatIf</span></span>
<span data-ttu-id="5f291-148">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="5f291-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5f291-149">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5f291-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f291-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f291-150">CommonParameters</span></span>
<span data-ttu-id="5f291-151">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f291-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f291-152">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f291-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f291-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f291-153">INPUTS</span></span>

### <span data-ttu-id="5f291-154">Nincs</span><span class="sxs-lookup"><span data-stu-id="5f291-154">None</span></span>

## <span data-ttu-id="5f291-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f291-155">OUTPUTS</span></span>

### <span data-ttu-id="5f291-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span><span class="sxs-lookup"><span data-stu-id="5f291-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="5f291-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5f291-157">NOTES</span></span>

## <span data-ttu-id="5f291-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f291-158">RELATED LINKS</span></span>
