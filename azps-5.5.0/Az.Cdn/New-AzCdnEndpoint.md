---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168058"
---
# <span data-ttu-id="09f3d-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09f3d-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="09f3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="09f3d-103">CDN-végpontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="09f3d-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="09f3d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="09f3d-104">SYNTAX</span></span>

### <span data-ttu-id="09f3d-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="09f3d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> -Location <String>
 [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09f3d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09f3d-106">ByObjectParameterSet</span></span>
```
New-AzCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultOriginGroup <String>] [-Priority <Int32>] [-Weight <Int32>] [-PrivateLinkApprovalMessage <String>]
 [-PrivateLinkLocation <String>] [-PrivateLinkResourceId <String>]
 [-OriginId <System.Collections.Generic.List`1[System.String]>] [-OriginGroupName <String>]
 [-OriginGroupProbeIntervalInSeconds <Int32>] [-OriginGroupProbePath <String>]
 [-OriginGroupProbeProtocol <String>] [-OriginGroupProbeRequestType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09f3d-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="09f3d-107">DESCRIPTION</span></span>
<span data-ttu-id="09f3d-108">A **New-AzCdnEndpoint** parancsmag létrehoz egy Azure Content Delivery Network (CDN) végpontot.</span><span class="sxs-lookup"><span data-stu-id="09f3d-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="09f3d-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="09f3d-109">EXAMPLES</span></span>

## <span data-ttu-id="09f3d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09f3d-110">PARAMETERS</span></span>

### <span data-ttu-id="09f3d-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="09f3d-111">-CdnProfile</span></span>
<span data-ttu-id="09f3d-112">Azt a CDN-profilobjektumot adja meg, amelyhez a végpontot hozzáadta.</span><span class="sxs-lookup"><span data-stu-id="09f3d-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="09f3d-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="09f3d-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="09f3d-114">A peremcsomópontról az ügyfélre tömöríteniandó tartalomtípusok tömbje.</span><span class="sxs-lookup"><span data-stu-id="09f3d-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="09f3d-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="09f3d-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="09f3d-116">Az alapértelmezett forráscsoport.</span><span class="sxs-lookup"><span data-stu-id="09f3d-116">The default origin group.</span></span>

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

### <span data-ttu-id="09f3d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f3d-117">-DefaultProfile</span></span>
<span data-ttu-id="09f3d-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="09f3d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09f3d-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="09f3d-119">-DeliveryPolicy</span></span>
<span data-ttu-id="09f3d-120">A végpont kézbesítési házirende.</span><span class="sxs-lookup"><span data-stu-id="09f3d-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="09f3d-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="09f3d-121">-EndpointName</span></span>
<span data-ttu-id="09f3d-122">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09f3d-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="09f3d-123">-GeoSzűrők</span><span class="sxs-lookup"><span data-stu-id="09f3d-123">-GeoFilters</span></span>
<span data-ttu-id="09f3d-124">Az erre a végpontra vonatkozó földrajzi szűrők listája.</span><span class="sxs-lookup"><span data-stu-id="09f3d-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="09f3d-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="09f3d-125">-HttpPort</span></span>
<span data-ttu-id="09f3d-126">Az originkiszolgáló HTTP-portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09f3d-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="09f3d-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="09f3d-127">-HttpsPort</span></span>
<span data-ttu-id="09f3d-128">Az originkiszolgáló HTTPS-portszámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="09f3d-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="09f3d-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="09f3d-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="09f3d-130">Azt jelzi, hogy engedélyezve van-e a tömörítés a végponthoz.</span><span class="sxs-lookup"><span data-stu-id="09f3d-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="09f3d-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="09f3d-131">-IsHttpAllowed</span></span>
<span data-ttu-id="09f3d-132">Azt jelzi, hogy a végpont engedélyezi-e a HTTP-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="09f3d-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="09f3d-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="09f3d-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="09f3d-134">Azt jelzi, hogy a végpont engedélyezi-e a HTTPS-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="09f3d-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="09f3d-135">-Location</span><span class="sxs-lookup"><span data-stu-id="09f3d-135">-Location</span></span>
<span data-ttu-id="09f3d-136">A végpont erőforrás-helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09f3d-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="09f3d-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="09f3d-137">-OptimizationType</span></span>
<span data-ttu-id="09f3d-138">A végpont esetleges optimalizálását adja meg.</span><span class="sxs-lookup"><span data-stu-id="09f3d-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="09f3d-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="09f3d-139">-OriginGroupName</span></span>
<span data-ttu-id="09f3d-140">A forráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="09f3d-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="09f3d-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="09f3d-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="09f3d-142">Az állapotok közti másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="09f3d-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="09f3d-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="09f3d-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="09f3d-144">A forrás állapotának meghatározásához használt forráshoz viszonyított elérési út.</span><span class="sxs-lookup"><span data-stu-id="09f3d-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="09f3d-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="09f3d-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="09f3d-146">Protokoll egészségügyi problémákhoz.</span><span class="sxs-lookup"><span data-stu-id="09f3d-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="09f3d-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="09f3d-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="09f3d-148">Az állapotkérés típusa.</span><span class="sxs-lookup"><span data-stu-id="09f3d-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="09f3d-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="09f3d-149">-OriginHostHeader</span></span>
<span data-ttu-id="09f3d-150">A végpont forrás gazdafejét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="09f3d-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="09f3d-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="09f3d-151">-OriginHostName</span></span>
<span data-ttu-id="09f3d-152">A forráskiszolgáló állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09f3d-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="09f3d-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="09f3d-153">-OriginId</span></span>
<span data-ttu-id="09f3d-154">Azure CDN-forráscsoport-azonosítók.</span><span class="sxs-lookup"><span data-stu-id="09f3d-154">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09f3d-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="09f3d-155">-OriginName</span></span>
<span data-ttu-id="09f3d-156">A forráskiszolgáló erőforrásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09f3d-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="09f3d-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="09f3d-157">-OriginPath</span></span>
<span data-ttu-id="09f3d-158">A forráskiszolgáló elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="09f3d-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="09f3d-159">-Priority</span><span class="sxs-lookup"><span data-stu-id="09f3d-159">-Priority</span></span>
<span data-ttu-id="09f3d-160">Azure CDN-forrás prioritása.</span><span class="sxs-lookup"><span data-stu-id="09f3d-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="09f3d-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="09f3d-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="09f3d-162">A személyes hivatkozáshoz való csatlakozáshoz a jóváhagyási kérelemben szerepelni fog egy egyéni üzenet.</span><span class="sxs-lookup"><span data-stu-id="09f3d-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="09f3d-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="09f3d-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="09f3d-164">Azure CDN-forrás privát hivatkozásának helye.</span><span class="sxs-lookup"><span data-stu-id="09f3d-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="09f3d-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="09f3d-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="09f3d-166">Azure CDN origin private link resource id.</span><span class="sxs-lookup"><span data-stu-id="09f3d-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="09f3d-167">-PathPath</span><span class="sxs-lookup"><span data-stu-id="09f3d-167">-ProbePath</span></span>
<span data-ttu-id="09f3d-168">A dinamikus webhely-gyorsítás elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="09f3d-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="09f3d-169">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="09f3d-169">-ProfileName</span></span>
<span data-ttu-id="09f3d-170">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="09f3d-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="09f3d-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="09f3d-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="09f3d-172">A CDN-végpont viselkedését határozza meg, amikor egy lekérdezési karakterlánc a kérés URL-címében található.</span><span class="sxs-lookup"><span data-stu-id="09f3d-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="09f3d-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09f3d-173">-ResourceGroupName</span></span>
<span data-ttu-id="09f3d-174">Annak az erőforráscsoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="09f3d-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="09f3d-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="09f3d-175">-Tag</span></span>
<span data-ttu-id="09f3d-176">Az Azure CDN-végponthoz társítva található címkék.</span><span class="sxs-lookup"><span data-stu-id="09f3d-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="09f3d-177">-Weight</span><span class="sxs-lookup"><span data-stu-id="09f3d-177">-Weight</span></span>
<span data-ttu-id="09f3d-178">Azure CDN origin weight.</span><span class="sxs-lookup"><span data-stu-id="09f3d-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="09f3d-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09f3d-179">-Confirm</span></span>
<span data-ttu-id="09f3d-180">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="09f3d-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09f3d-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09f3d-181">-WhatIf</span></span>
<span data-ttu-id="09f3d-182">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="09f3d-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09f3d-183">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="09f3d-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09f3d-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f3d-184">CommonParameters</span></span>
<span data-ttu-id="09f3d-185">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09f3d-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f3d-186">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09f3d-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f3d-187">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09f3d-187">INPUTS</span></span>

### <span data-ttu-id="09f3d-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="09f3d-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="09f3d-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="09f3d-189">OUTPUTS</span></span>

### <span data-ttu-id="09f3d-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="09f3d-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="09f3d-191">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="09f3d-191">NOTES</span></span>

## <span data-ttu-id="09f3d-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="09f3d-192">RELATED LINKS</span></span>

[<span data-ttu-id="09f3d-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09f3d-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="09f3d-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09f3d-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="09f3d-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09f3d-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="09f3d-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09f3d-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="09f3d-197">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="09f3d-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


