---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: ba06dcabe874161c9f801841a5be8b0337614799
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012845"
---
# <span data-ttu-id="831ec-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="831ec-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="831ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="831ec-102">SYNOPSIS</span></span>
<span data-ttu-id="831ec-103">CDN-végpontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="831ec-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="831ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="831ec-104">SYNTAX</span></span>

### <span data-ttu-id="831ec-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="831ec-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="831ec-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="831ec-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="831ec-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="831ec-107">DESCRIPTION</span></span>
<span data-ttu-id="831ec-108">A **New-AzCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="831ec-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="831ec-109">Példák</span><span class="sxs-lookup"><span data-stu-id="831ec-109">EXAMPLES</span></span>

## <span data-ttu-id="831ec-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="831ec-110">PARAMETERS</span></span>

### <span data-ttu-id="831ec-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="831ec-111">-CdnProfile</span></span>
<span data-ttu-id="831ec-112">Annak a CDN-profil objektumnak a megadása, amelyhez a végpont hozzá van adva.</span><span class="sxs-lookup"><span data-stu-id="831ec-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="831ec-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="831ec-114">Itt adhatja meg, hogy milyen tartalomtípusokat tömörít az Edge csomópontról az ügyfélre.</span><span class="sxs-lookup"><span data-stu-id="831ec-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="831ec-115">-DefaultProfile</span></span>
<span data-ttu-id="831ec-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="831ec-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="831ec-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="831ec-117">-DeliveryPolicy</span></span>
<span data-ttu-id="831ec-118">A végpont kézbesítési házirendje.</span><span class="sxs-lookup"><span data-stu-id="831ec-118">The delivery policy for this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="831ec-119">-EndpointName</span></span>
<span data-ttu-id="831ec-120">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="831ec-120">Specifies the name of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-121">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="831ec-121">-GeoFilters</span></span>
<span data-ttu-id="831ec-122">A végpontra érvényes geo-szűrők listája.</span><span class="sxs-lookup"><span data-stu-id="831ec-122">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="831ec-123">-HttpPort</span></span>
<span data-ttu-id="831ec-124">A HTTP-portszámot adja meg a forrás kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="831ec-124">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="831ec-125">-HttpsPort</span></span>
<span data-ttu-id="831ec-126">A forráskiszolgálón a HTTPS-portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="831ec-126">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="831ec-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="831ec-128">Azt jelzi, hogy a végponthoz engedélyezve van-e a tömörítés.</span><span class="sxs-lookup"><span data-stu-id="831ec-128">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="831ec-129">-IsHttpAllowed</span></span>
<span data-ttu-id="831ec-130">Azt jelzi, hogy a végpont engedélyezi-e a HTTP-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="831ec-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="831ec-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="831ec-132">Azt jelzi, hogy a végpont engedélyezi-e a HTTPS-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="831ec-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-133">-Hely</span><span class="sxs-lookup"><span data-stu-id="831ec-133">-Location</span></span>
<span data-ttu-id="831ec-134">A végpont erőforrás-helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="831ec-134">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="831ec-135">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="831ec-135">-OptimizationType</span></span>
<span data-ttu-id="831ec-136">A végpont optimalizálását adja meg.</span><span class="sxs-lookup"><span data-stu-id="831ec-136">Specifies any optimization this endpoint has.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="831ec-137">-OriginHostHeader</span></span>
<span data-ttu-id="831ec-138">A végpont kezdőpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="831ec-138">Specifies the origin host head of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="831ec-139">-OriginHostName</span></span>
<span data-ttu-id="831ec-140">A forráskiszolgáló állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="831ec-140">Specifies the host name of the origin server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-141">-OriginName</span><span class="sxs-lookup"><span data-stu-id="831ec-141">-OriginName</span></span>
<span data-ttu-id="831ec-142">A forráskiszolgáló erőforrásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="831ec-142">Specifies the resource name of the origin server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="831ec-143">-OriginPath</span></span>
<span data-ttu-id="831ec-144">A származási kiszolgáló elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="831ec-144">Specifies the path of the origin server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="831ec-145">-ProbePath</span></span>
<span data-ttu-id="831ec-146">A dinamikus webhely-gyorsításhoz tartozó szonda elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="831ec-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-147">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="831ec-147">-ProfileName</span></span>
<span data-ttu-id="831ec-148">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="831ec-148">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="831ec-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="831ec-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="831ec-150">A CDN-végpont működését adja meg, ha egy lekérdezési karakterlánc a kérés URL-címében szerepel.</span><span class="sxs-lookup"><span data-stu-id="831ec-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSQueryStringCachingBehavior]
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="831ec-151">-ResourceGroupName</span></span>
<span data-ttu-id="831ec-152">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="831ec-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="831ec-153">-Címke</span><span class="sxs-lookup"><span data-stu-id="831ec-153">-Tag</span></span>
<span data-ttu-id="831ec-154">Az Azure CDN-végponttal társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="831ec-154">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="831ec-155">-Confirm</span></span>
<span data-ttu-id="831ec-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="831ec-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="831ec-157">-WhatIf</span></span>
<span data-ttu-id="831ec-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="831ec-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="831ec-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="831ec-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="831ec-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="831ec-160">CommonParameters</span></span>
<span data-ttu-id="831ec-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="831ec-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="831ec-162">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="831ec-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="831ec-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="831ec-163">INPUTS</span></span>

### <span data-ttu-id="831ec-164">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="831ec-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="831ec-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="831ec-165">OUTPUTS</span></span>

### <span data-ttu-id="831ec-166">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="831ec-166">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="831ec-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="831ec-167">NOTES</span></span>

## <span data-ttu-id="831ec-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="831ec-168">RELATED LINKS</span></span>

[<span data-ttu-id="831ec-169">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="831ec-169">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="831ec-170">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="831ec-170">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="831ec-171">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="831ec-171">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="831ec-172">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="831ec-172">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="831ec-173">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="831ec-173">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


