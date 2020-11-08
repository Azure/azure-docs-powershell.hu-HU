---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnEndpoint.md
ms.openlocfilehash: 9e0b8ee74ff89f4a5903df1c73dc7b289b0371c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186266"
---
# <span data-ttu-id="f960c-101">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f960c-101">New-AzCdnEndpoint</span></span>

## <span data-ttu-id="f960c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f960c-102">SYNOPSIS</span></span>
<span data-ttu-id="f960c-103">CDN-végpontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="f960c-103">Creates a CDN endpoint.</span></span>

## <span data-ttu-id="f960c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f960c-104">SYNTAX</span></span>

### <span data-ttu-id="f960c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f960c-105">ByFieldsParameterSet (Default)</span></span>
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

### <span data-ttu-id="f960c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f960c-106">ByObjectParameterSet</span></span>
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

## <span data-ttu-id="f960c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f960c-107">DESCRIPTION</span></span>
<span data-ttu-id="f960c-108">A **New-AzCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="f960c-108">The **New-AzCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f960c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f960c-109">EXAMPLES</span></span>

## <span data-ttu-id="f960c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f960c-110">PARAMETERS</span></span>

### <span data-ttu-id="f960c-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="f960c-111">-CdnProfile</span></span>
<span data-ttu-id="f960c-112">Annak a CDN-profil objektumnak a megadása, amelyhez a végpont hozzá van adva.</span><span class="sxs-lookup"><span data-stu-id="f960c-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="f960c-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="f960c-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="f960c-114">Itt adhatja meg, hogy milyen tartalomtípusokat tömörít az Edge csomópontról az ügyfélre.</span><span class="sxs-lookup"><span data-stu-id="f960c-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="f960c-115">-DefaultOriginGroup</span><span class="sxs-lookup"><span data-stu-id="f960c-115">-DefaultOriginGroup</span></span>
<span data-ttu-id="f960c-116">Az alapértelmezett Origó csoport.</span><span class="sxs-lookup"><span data-stu-id="f960c-116">The default origin group.</span></span>

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

### <span data-ttu-id="f960c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f960c-117">-DefaultProfile</span></span>
<span data-ttu-id="f960c-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f960c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f960c-119">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="f960c-119">-DeliveryPolicy</span></span>
<span data-ttu-id="f960c-120">A végpont kézbesítési házirendje.</span><span class="sxs-lookup"><span data-stu-id="f960c-120">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="f960c-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f960c-121">-EndpointName</span></span>
<span data-ttu-id="f960c-122">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f960c-122">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="f960c-123">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="f960c-123">-GeoFilters</span></span>
<span data-ttu-id="f960c-124">A végpontra érvényes geo-szűrők listája.</span><span class="sxs-lookup"><span data-stu-id="f960c-124">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="f960c-125">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="f960c-125">-HttpPort</span></span>
<span data-ttu-id="f960c-126">A HTTP-portszámot adja meg a forrás kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="f960c-126">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="f960c-127">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="f960c-127">-HttpsPort</span></span>
<span data-ttu-id="f960c-128">A forráskiszolgálón a HTTPS-portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="f960c-128">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="f960c-129">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="f960c-129">-IsCompressionEnabled</span></span>
<span data-ttu-id="f960c-130">Azt jelzi, hogy a végponthoz engedélyezve van-e a tömörítés.</span><span class="sxs-lookup"><span data-stu-id="f960c-130">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="f960c-131">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="f960c-131">-IsHttpAllowed</span></span>
<span data-ttu-id="f960c-132">Azt jelzi, hogy a végpont engedélyezi-e a HTTP-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="f960c-132">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="f960c-133">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="f960c-133">-IsHttpsAllowed</span></span>
<span data-ttu-id="f960c-134">Azt jelzi, hogy a végpont engedélyezi-e a HTTPS-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="f960c-134">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="f960c-135">-Hely</span><span class="sxs-lookup"><span data-stu-id="f960c-135">-Location</span></span>
<span data-ttu-id="f960c-136">A végpont erőforrás-helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f960c-136">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="f960c-137">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="f960c-137">-OptimizationType</span></span>
<span data-ttu-id="f960c-138">A végpont optimalizálását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f960c-138">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="f960c-139">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="f960c-139">-OriginGroupName</span></span>
<span data-ttu-id="f960c-140">A származási csoport neve.</span><span class="sxs-lookup"><span data-stu-id="f960c-140">The name of the origin group.</span></span>

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

### <span data-ttu-id="f960c-141">-OriginGroupProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f960c-141">-OriginGroupProbeIntervalInSeconds</span></span>
<span data-ttu-id="f960c-142">Az egészségügyi Szondák közötti másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="f960c-142">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="f960c-143">-OriginGroupProbePath</span><span class="sxs-lookup"><span data-stu-id="f960c-143">-OriginGroupProbePath</span></span>
<span data-ttu-id="f960c-144">A származási állapot meghatározásához használt kezdőponthoz viszonyított útvonal.</span><span class="sxs-lookup"><span data-stu-id="f960c-144">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="f960c-145">-OriginGroupProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="f960c-145">-OriginGroupProbeProtocol</span></span>
<span data-ttu-id="f960c-146">Az egészségi szondához használandó protokoll.</span><span class="sxs-lookup"><span data-stu-id="f960c-146">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="f960c-147">-OriginGroupProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="f960c-147">-OriginGroupProbeRequestType</span></span>
<span data-ttu-id="f960c-148">Az elvégzett állapottanúsítvány-kérés típusa.</span><span class="sxs-lookup"><span data-stu-id="f960c-148">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="f960c-149">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="f960c-149">-OriginHostHeader</span></span>
<span data-ttu-id="f960c-150">A végpont kezdőpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f960c-150">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="f960c-151">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="f960c-151">-OriginHostName</span></span>
<span data-ttu-id="f960c-152">A forráskiszolgáló állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f960c-152">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="f960c-153">-OriginId</span><span class="sxs-lookup"><span data-stu-id="f960c-153">-OriginId</span></span>
<span data-ttu-id="f960c-154">Azure CDN Origin Group azonosítók.</span><span class="sxs-lookup"><span data-stu-id="f960c-154">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="f960c-155">-OriginName</span><span class="sxs-lookup"><span data-stu-id="f960c-155">-OriginName</span></span>
<span data-ttu-id="f960c-156">A forráskiszolgáló erőforrásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f960c-156">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="f960c-157">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="f960c-157">-OriginPath</span></span>
<span data-ttu-id="f960c-158">A származási kiszolgáló elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f960c-158">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="f960c-159">– Prioritás</span><span class="sxs-lookup"><span data-stu-id="f960c-159">-Priority</span></span>
<span data-ttu-id="f960c-160">Azure CDN-forrás prioritása.</span><span class="sxs-lookup"><span data-stu-id="f960c-160">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="f960c-161">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="f960c-161">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="f960c-162">A privát hivatkozáshoz való csatlakozáshoz a jóváhagyási kérelemben szerepeltetni kívánt egyéni üzenet.</span><span class="sxs-lookup"><span data-stu-id="f960c-162">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="f960c-163">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="f960c-163">-PrivateLinkLocation</span></span>
<span data-ttu-id="f960c-164">Azure CDN Origin privát hivatkozás helye.</span><span class="sxs-lookup"><span data-stu-id="f960c-164">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="f960c-165">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="f960c-165">-PrivateLinkResourceId</span></span>
<span data-ttu-id="f960c-166">Azure CDN Origin Private link erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f960c-166">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="f960c-167">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="f960c-167">-ProbePath</span></span>
<span data-ttu-id="f960c-168">A dinamikus webhely-gyorsításhoz tartozó szonda elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f960c-168">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="f960c-169">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="f960c-169">-ProfileName</span></span>
<span data-ttu-id="f960c-170">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f960c-170">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="f960c-171">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="f960c-171">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="f960c-172">A CDN-végpont működését adja meg, ha egy lekérdezési karakterlánc a kérés URL-címében szerepel.</span><span class="sxs-lookup"><span data-stu-id="f960c-172">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="f960c-173">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f960c-173">-ResourceGroupName</span></span>
<span data-ttu-id="f960c-174">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="f960c-174">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="f960c-175">-Címke</span><span class="sxs-lookup"><span data-stu-id="f960c-175">-Tag</span></span>
<span data-ttu-id="f960c-176">Az Azure CDN-végponttal társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="f960c-176">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="f960c-177">-Weight (súly)</span><span class="sxs-lookup"><span data-stu-id="f960c-177">-Weight</span></span>
<span data-ttu-id="f960c-178">Azure CDN származási súlya</span><span class="sxs-lookup"><span data-stu-id="f960c-178">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="f960c-179">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f960c-179">-Confirm</span></span>
<span data-ttu-id="f960c-180">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f960c-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f960c-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f960c-181">-WhatIf</span></span>
<span data-ttu-id="f960c-182">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f960c-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f960c-183">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f960c-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f960c-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f960c-184">CommonParameters</span></span>
<span data-ttu-id="f960c-185">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f960c-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f960c-186">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f960c-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f960c-187">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f960c-187">INPUTS</span></span>

### <span data-ttu-id="f960c-188">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="f960c-188">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="f960c-189">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f960c-189">OUTPUTS</span></span>

### <span data-ttu-id="f960c-190">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f960c-190">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="f960c-191">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f960c-191">NOTES</span></span>

## <span data-ttu-id="f960c-192">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f960c-192">RELATED LINKS</span></span>

[<span data-ttu-id="f960c-193">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f960c-193">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="f960c-194">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f960c-194">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="f960c-195">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f960c-195">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="f960c-196">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f960c-196">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="f960c-197">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f960c-197">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


