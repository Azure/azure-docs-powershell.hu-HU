---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 5d2bfdf2bf5f87ccb0213c006de8612b5eaf0730
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500915"
---
# <span data-ttu-id="4f585-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f585-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="4f585-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4f585-102">SYNOPSIS</span></span>
<span data-ttu-id="4f585-103">CDN-végpontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="4f585-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f585-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4f585-104">SYNTAX</span></span>

### <span data-ttu-id="4f585-105">Paraméterérték a mezők paramétereinek beállításához (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4f585-105">Parameter Set for fields parameters (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f585-106">Az objektum paramétereinek beállítása paraméter</span><span class="sxs-lookup"><span data-stu-id="4f585-106">Parameter Set for object parameters</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f585-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4f585-107">DESCRIPTION</span></span>
<span data-ttu-id="4f585-108">A **New-AzureRmCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="4f585-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="4f585-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4f585-109">EXAMPLES</span></span>

## <span data-ttu-id="4f585-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4f585-110">PARAMETERS</span></span>

### <span data-ttu-id="4f585-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="4f585-111">-CdnProfile</span></span>
<span data-ttu-id="4f585-112">Annak a CDN-profil objektumnak a megadása, amelyhez a végpont hozzá van adva.</span><span class="sxs-lookup"><span data-stu-id="4f585-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f585-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="4f585-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="4f585-114">Itt adhatja meg, hogy milyen tartalomtípusokat tömörít az Edge csomópontról az ügyfélre.</span><span class="sxs-lookup"><span data-stu-id="4f585-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="4f585-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4f585-115">-EndpointName</span></span>
<span data-ttu-id="4f585-116">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f585-116">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="4f585-117">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="4f585-117">-GeoFilters</span></span>
<span data-ttu-id="4f585-118">A végpontra érvényes geo-szűrők listája.</span><span class="sxs-lookup"><span data-stu-id="4f585-118">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="4f585-119">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="4f585-119">-HttpPort</span></span>
<span data-ttu-id="4f585-120">A HTTP-portszámot adja meg a forrás kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="4f585-120">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="4f585-121">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="4f585-121">-HttpsPort</span></span>
<span data-ttu-id="4f585-122">A forráskiszolgálón a HTTPS-portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f585-122">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="4f585-123">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="4f585-123">-IsCompressionEnabled</span></span>
<span data-ttu-id="4f585-124">Azt jelzi, hogy a végponthoz engedélyezve van-e a tömörítés.</span><span class="sxs-lookup"><span data-stu-id="4f585-124">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="4f585-125">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="4f585-125">-IsHttpAllowed</span></span>
<span data-ttu-id="4f585-126">Azt jelzi, hogy a végpont engedélyezi-e a HTTP-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="4f585-126">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="4f585-127">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="4f585-127">-IsHttpsAllowed</span></span>
<span data-ttu-id="4f585-128">Azt jelzi, hogy a végpont engedélyezi-e a HTTPS-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="4f585-128">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="4f585-129">-Hely</span><span class="sxs-lookup"><span data-stu-id="4f585-129">-Location</span></span>
<span data-ttu-id="4f585-130">A végpont erőforrás-helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f585-130">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f585-131">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="4f585-131">-OptimizationType</span></span>
<span data-ttu-id="4f585-132">A végpont optimalizálását adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f585-132">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="4f585-133">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="4f585-133">-OriginHostHeader</span></span>
<span data-ttu-id="4f585-134">A végpont kezdőpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f585-134">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="4f585-135">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="4f585-135">-OriginHostName</span></span>
<span data-ttu-id="4f585-136">A forráskiszolgáló állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f585-136">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="4f585-137">-OriginName</span><span class="sxs-lookup"><span data-stu-id="4f585-137">-OriginName</span></span>
<span data-ttu-id="4f585-138">A forráskiszolgáló erőforrásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f585-138">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="4f585-139">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="4f585-139">-OriginPath</span></span>
<span data-ttu-id="4f585-140">A származási kiszolgáló elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f585-140">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="4f585-141">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="4f585-141">-ProfileName</span></span>
<span data-ttu-id="4f585-142">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f585-142">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f585-143">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="4f585-143">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="4f585-144">A CDN-végpont működését adja meg, ha egy lekérdezési karakterlánc a kérés URL-címében szerepel.</span><span class="sxs-lookup"><span data-stu-id="4f585-144">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="4f585-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f585-145">-ResourceGroupName</span></span>
<span data-ttu-id="4f585-146">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="4f585-146">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f585-147">-Címkék</span><span class="sxs-lookup"><span data-stu-id="4f585-147">-Tags</span></span>
<span data-ttu-id="4f585-148">Az erőforráshoz társított címkék ujjlenyomat-táblázatát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4f585-148">Specifies a hash table of the tags that associated with this resource.</span></span>

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

### <span data-ttu-id="4f585-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4f585-149">-Confirm</span></span>
<span data-ttu-id="4f585-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4f585-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f585-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f585-151">-WhatIf</span></span>
<span data-ttu-id="4f585-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4f585-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f585-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4f585-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f585-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f585-154">-DefaultProfile</span></span>
<span data-ttu-id="4f585-155">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4f585-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f585-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f585-156">CommonParameters</span></span>
<span data-ttu-id="4f585-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4f585-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f585-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f585-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f585-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f585-159">INPUTS</span></span>

### <span data-ttu-id="4f585-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="4f585-160">PSProfile</span></span>
<span data-ttu-id="4f585-161">A ' CdnProfile ' paraméter az "PSProfile" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4f585-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="4f585-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4f585-162">OUTPUTS</span></span>

### <span data-ttu-id="4f585-163">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f585-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="4f585-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4f585-164">NOTES</span></span>

## <span data-ttu-id="4f585-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4f585-165">RELATED LINKS</span></span>

[<span data-ttu-id="4f585-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f585-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="4f585-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f585-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="4f585-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f585-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="4f585-169">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f585-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="4f585-170">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="4f585-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


