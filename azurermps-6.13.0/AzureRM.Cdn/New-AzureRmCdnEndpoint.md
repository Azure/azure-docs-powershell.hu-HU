---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 62a4859b5a64003956a4975411f809176f2917e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499712"
---
# <span data-ttu-id="7891a-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7891a-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="7891a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7891a-102">SYNOPSIS</span></span>
<span data-ttu-id="7891a-103">CDN-végpontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7891a-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7891a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7891a-104">SYNTAX</span></span>

### <span data-ttu-id="7891a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7891a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7891a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7891a-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-ProbePath <String>]
 [-GeoFilters <PSGeoFilter[]>] [-DeliveryPolicy <PSDeliveryPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7891a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7891a-107">DESCRIPTION</span></span>
<span data-ttu-id="7891a-108">A **New-AzureRmCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="7891a-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="7891a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7891a-109">EXAMPLES</span></span>

## <span data-ttu-id="7891a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7891a-110">PARAMETERS</span></span>

### <span data-ttu-id="7891a-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="7891a-111">-CdnProfile</span></span>
<span data-ttu-id="7891a-112">Annak a CDN-profil objektumnak a megadása, amelyhez a végpont hozzá van adva.</span><span class="sxs-lookup"><span data-stu-id="7891a-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

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

### <span data-ttu-id="7891a-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="7891a-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="7891a-114">Itt adhatja meg, hogy milyen tartalomtípusokat tömörít az Edge csomópontról az ügyfélre.</span><span class="sxs-lookup"><span data-stu-id="7891a-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

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

### <span data-ttu-id="7891a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7891a-115">-DefaultProfile</span></span>
<span data-ttu-id="7891a-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7891a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7891a-117">-DeliveryPolicy</span><span class="sxs-lookup"><span data-stu-id="7891a-117">-DeliveryPolicy</span></span>
<span data-ttu-id="7891a-118">A végpont kézbesítési házirendje.</span><span class="sxs-lookup"><span data-stu-id="7891a-118">The delivery policy for this endpoint.</span></span>

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

### <span data-ttu-id="7891a-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7891a-119">-EndpointName</span></span>
<span data-ttu-id="7891a-120">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7891a-120">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="7891a-121">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="7891a-121">-GeoFilters</span></span>
<span data-ttu-id="7891a-122">A végpontra érvényes geo-szűrők listája.</span><span class="sxs-lookup"><span data-stu-id="7891a-122">The list of geo filters that applies to this endpoint.</span></span>

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

### <span data-ttu-id="7891a-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="7891a-123">-HttpPort</span></span>
<span data-ttu-id="7891a-124">A HTTP-portszámot adja meg a forrás kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="7891a-124">Specifies the HTTP port number on the origin server.</span></span>

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

### <span data-ttu-id="7891a-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="7891a-125">-HttpsPort</span></span>
<span data-ttu-id="7891a-126">A forráskiszolgálón a HTTPS-portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="7891a-126">Specifies the HTTPS port number on the origin server.</span></span>

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

### <span data-ttu-id="7891a-127">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="7891a-127">-IsCompressionEnabled</span></span>
<span data-ttu-id="7891a-128">Azt jelzi, hogy a végponthoz engedélyezve van-e a tömörítés.</span><span class="sxs-lookup"><span data-stu-id="7891a-128">Indicates whether compression is enabled for the endpoint.</span></span>

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

### <span data-ttu-id="7891a-129">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="7891a-129">-IsHttpAllowed</span></span>
<span data-ttu-id="7891a-130">Azt jelzi, hogy a végpont engedélyezi-e a HTTP-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="7891a-130">Indicates whether the endpoint enables HTTP traffic.</span></span>

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

### <span data-ttu-id="7891a-131">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="7891a-131">-IsHttpsAllowed</span></span>
<span data-ttu-id="7891a-132">Azt jelzi, hogy a végpont engedélyezi-e a HTTPS-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="7891a-132">Indicates whether the endpoint enables HTTPS traffic.</span></span>

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

### <span data-ttu-id="7891a-133">-Hely</span><span class="sxs-lookup"><span data-stu-id="7891a-133">-Location</span></span>
<span data-ttu-id="7891a-134">A végpont erőforrás-helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7891a-134">Specifies the resource location of the endpoint.</span></span>

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

### <span data-ttu-id="7891a-135">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="7891a-135">-OptimizationType</span></span>
<span data-ttu-id="7891a-136">A végpont optimalizálását adja meg.</span><span class="sxs-lookup"><span data-stu-id="7891a-136">Specifies any optimization this endpoint has.</span></span>

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

### <span data-ttu-id="7891a-137">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="7891a-137">-OriginHostHeader</span></span>
<span data-ttu-id="7891a-138">A végpont kezdőpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7891a-138">Specifies the origin host head of the endpoint.</span></span>

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

### <span data-ttu-id="7891a-139">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="7891a-139">-OriginHostName</span></span>
<span data-ttu-id="7891a-140">A forráskiszolgáló állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7891a-140">Specifies the host name of the origin server.</span></span>

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

### <span data-ttu-id="7891a-141">-OriginName</span><span class="sxs-lookup"><span data-stu-id="7891a-141">-OriginName</span></span>
<span data-ttu-id="7891a-142">A forráskiszolgáló erőforrásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7891a-142">Specifies the resource name of the origin server.</span></span>

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

### <span data-ttu-id="7891a-143">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="7891a-143">-OriginPath</span></span>
<span data-ttu-id="7891a-144">A származási kiszolgáló elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7891a-144">Specifies the path of the origin server.</span></span>

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

### <span data-ttu-id="7891a-145">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="7891a-145">-ProbePath</span></span>
<span data-ttu-id="7891a-146">A dinamikus webhely-gyorsításhoz tartozó szonda elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7891a-146">Specifies the probe path for Dynamic Site Acceleration</span></span>

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

### <span data-ttu-id="7891a-147">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="7891a-147">-ProfileName</span></span>
<span data-ttu-id="7891a-148">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7891a-148">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="7891a-149">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="7891a-149">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="7891a-150">A CDN-végpont működését adja meg, ha egy lekérdezési karakterlánc a kérés URL-címében szerepel.</span><span class="sxs-lookup"><span data-stu-id="7891a-150">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

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

### <span data-ttu-id="7891a-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7891a-151">-ResourceGroupName</span></span>
<span data-ttu-id="7891a-152">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="7891a-152">Specifies the name of the resource group to which this endpoint belongs.</span></span>

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

### <span data-ttu-id="7891a-153">-Címke</span><span class="sxs-lookup"><span data-stu-id="7891a-153">-Tag</span></span>
<span data-ttu-id="7891a-154">Az Azure CDN-végponttal társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="7891a-154">The tags to associate with the Azure CDN endpoint.</span></span>

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

### <span data-ttu-id="7891a-155">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7891a-155">-Confirm</span></span>
<span data-ttu-id="7891a-156">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7891a-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7891a-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7891a-157">-WhatIf</span></span>
<span data-ttu-id="7891a-158">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7891a-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7891a-159">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7891a-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7891a-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7891a-160">CommonParameters</span></span>
<span data-ttu-id="7891a-161">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7891a-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7891a-162">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7891a-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7891a-163">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7891a-163">INPUTS</span></span>

### <span data-ttu-id="7891a-164">Microsoft. Azure. Command. CDN. models. profil. PSProfile</span><span class="sxs-lookup"><span data-stu-id="7891a-164">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="7891a-165">Paraméterek: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7891a-165">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="7891a-166">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7891a-166">OUTPUTS</span></span>

### <span data-ttu-id="7891a-167">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="7891a-167">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="7891a-168">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7891a-168">NOTES</span></span>

## <span data-ttu-id="7891a-169">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7891a-169">RELATED LINKS</span></span>

[<span data-ttu-id="7891a-170">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7891a-170">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="7891a-171">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7891a-171">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="7891a-172">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7891a-172">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="7891a-173">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7891a-173">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="7891a-174">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="7891a-174">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


