---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: A8C6F3BC-EE93-49A4-BF7B-8420967EEB7B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/new-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/New-AzureRmCdnEndpoint.md
ms.openlocfilehash: 682c12270608f9c75e86cea742fd411e0eb657a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493226"
---
# <span data-ttu-id="1ac99-101">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ac99-101">New-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="1ac99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ac99-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac99-103">CDN-végpontot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1ac99-103">Creates a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ac99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ac99-104">SYNTAX</span></span>

### <span data-ttu-id="1ac99-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ac99-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -Location <String> [-OriginHostHeader <String>] [-OriginPath <String>] [-ContentTypesToCompress <String[]>]
 [-IsCompressionEnabled <Boolean>] [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ac99-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ac99-106">ByObjectParameterSet</span></span>
```
New-AzureRmCdnEndpoint -EndpointName <String> -CdnProfile <PSProfile> [-OriginHostHeader <String>]
 [-OriginPath <String>] [-ContentTypesToCompress <String[]>] [-IsCompressionEnabled <Boolean>]
 [-IsHttpAllowed <Boolean>] [-IsHttpsAllowed <Boolean>]
 [-QueryStringCachingBehavior <PSQueryStringCachingBehavior>] -OriginName <String> -OriginHostName <String>
 [-HttpPort <Int32>] [-HttpsPort <Int32>] [-OptimizationType <String>] [-GeoFilters <PSGeoFilter[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ac99-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ac99-107">DESCRIPTION</span></span>
<span data-ttu-id="1ac99-108">A **New-AzureRmCdnEndpoint** parancsmag az Azure Content Delivery Network (CDN) végpontját hozza létre.</span><span class="sxs-lookup"><span data-stu-id="1ac99-108">The **New-AzureRmCdnEndpoint** cmdlet creates an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="1ac99-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1ac99-109">EXAMPLES</span></span>

## <span data-ttu-id="1ac99-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ac99-110">PARAMETERS</span></span>

### <span data-ttu-id="1ac99-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="1ac99-111">-CdnProfile</span></span>
<span data-ttu-id="1ac99-112">Annak a CDN-profil objektumnak a megadása, amelyhez a végpont hozzá van adva.</span><span class="sxs-lookup"><span data-stu-id="1ac99-112">Specifies the CDN profile object to which the endpoint is added.</span></span>

```yaml
Type: PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-113">-ContentTypesToCompress</span><span class="sxs-lookup"><span data-stu-id="1ac99-113">-ContentTypesToCompress</span></span>
<span data-ttu-id="1ac99-114">Itt adhatja meg, hogy milyen tartalomtípusokat tömörít az Edge csomópontról az ügyfélre.</span><span class="sxs-lookup"><span data-stu-id="1ac99-114">Specifies an array of content types to compress from the edge node to the client.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac99-115">-DefaultProfile</span></span>
<span data-ttu-id="1ac99-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1ac99-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1ac99-117">-EndpointName</span></span>
<span data-ttu-id="1ac99-118">A végpont nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ac99-118">Specifies the name of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-119">-GeoFilters</span><span class="sxs-lookup"><span data-stu-id="1ac99-119">-GeoFilters</span></span>
<span data-ttu-id="1ac99-120">A végpontra érvényes geo-szűrők listája.</span><span class="sxs-lookup"><span data-stu-id="1ac99-120">The list of geo filters that applies to this endpoint.</span></span>

```yaml
Type: PSGeoFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-121">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="1ac99-121">-HttpPort</span></span>
<span data-ttu-id="1ac99-122">A HTTP-portszámot adja meg a forrás kiszolgálón.</span><span class="sxs-lookup"><span data-stu-id="1ac99-122">Specifies the HTTP port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-123">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="1ac99-123">-HttpsPort</span></span>
<span data-ttu-id="1ac99-124">A forráskiszolgálón a HTTPS-portszámot adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ac99-124">Specifies the HTTPS port number on the origin server.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-125">-IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="1ac99-125">-IsCompressionEnabled</span></span>
<span data-ttu-id="1ac99-126">Azt jelzi, hogy a végponthoz engedélyezve van-e a tömörítés.</span><span class="sxs-lookup"><span data-stu-id="1ac99-126">Indicates whether compression is enabled for the endpoint.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-127">-IsHttpAllowed</span><span class="sxs-lookup"><span data-stu-id="1ac99-127">-IsHttpAllowed</span></span>
<span data-ttu-id="1ac99-128">Azt jelzi, hogy a végpont engedélyezi-e a HTTP-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="1ac99-128">Indicates whether the endpoint enables HTTP traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-129">-IsHttpsAllowed</span><span class="sxs-lookup"><span data-stu-id="1ac99-129">-IsHttpsAllowed</span></span>
<span data-ttu-id="1ac99-130">Azt jelzi, hogy a végpont engedélyezi-e a HTTPS-forgalmat.</span><span class="sxs-lookup"><span data-stu-id="1ac99-130">Indicates whether the endpoint enables HTTPS traffic.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-131">-Hely</span><span class="sxs-lookup"><span data-stu-id="1ac99-131">-Location</span></span>
<span data-ttu-id="1ac99-132">A végpont erőforrás-helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ac99-132">Specifies the resource location of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-133">-OptimizationType</span><span class="sxs-lookup"><span data-stu-id="1ac99-133">-OptimizationType</span></span>
<span data-ttu-id="1ac99-134">A végpont optimalizálását adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ac99-134">Specifies any optimization this endpoint has.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-135">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="1ac99-135">-OriginHostHeader</span></span>
<span data-ttu-id="1ac99-136">A végpont kezdőpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ac99-136">Specifies the origin host head of the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-137">-OriginHostName</span><span class="sxs-lookup"><span data-stu-id="1ac99-137">-OriginHostName</span></span>
<span data-ttu-id="1ac99-138">A forráskiszolgáló állomásnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ac99-138">Specifies the host name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-139">-OriginName</span><span class="sxs-lookup"><span data-stu-id="1ac99-139">-OriginName</span></span>
<span data-ttu-id="1ac99-140">A forráskiszolgáló erőforrásának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ac99-140">Specifies the resource name of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-141">-OriginPath</span><span class="sxs-lookup"><span data-stu-id="1ac99-141">-OriginPath</span></span>
<span data-ttu-id="1ac99-142">A származási kiszolgáló elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ac99-142">Specifies the path of the origin server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-143">-Fájlnév</span><span class="sxs-lookup"><span data-stu-id="1ac99-143">-ProfileName</span></span>
<span data-ttu-id="1ac99-144">A profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ac99-144">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-145">-QueryStringCachingBehavior</span><span class="sxs-lookup"><span data-stu-id="1ac99-145">-QueryStringCachingBehavior</span></span>
<span data-ttu-id="1ac99-146">A CDN-végpont működését adja meg, ha egy lekérdezési karakterlánc a kérés URL-címében szerepel.</span><span class="sxs-lookup"><span data-stu-id="1ac99-146">Specifies the behavior of CDN endpoint when a query string is in the request URL.</span></span>

```yaml
Type: PSQueryStringCachingBehavior
Parameter Sets: (All)
Aliases:
Accepted values: IgnoreQueryString, BypassCaching, UseQueryString, NotSet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ac99-147">-ResourceGroupName</span></span>
<span data-ttu-id="1ac99-148">Annak az erőforrás-csoportnak a nevét adja meg, amelyhez a végpont tartozik.</span><span class="sxs-lookup"><span data-stu-id="1ac99-148">Specifies the name of the resource group to which this endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-149">-Címke</span><span class="sxs-lookup"><span data-stu-id="1ac99-149">-Tag</span></span>
<span data-ttu-id="1ac99-150">Az Azure CDN-végponttal társítani kívánt címkék.</span><span class="sxs-lookup"><span data-stu-id="1ac99-150">The tags to associate with the Azure CDN endpoint.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ac99-151">-Confirm</span></span>
<span data-ttu-id="1ac99-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ac99-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ac99-153">-WhatIf</span></span>
<span data-ttu-id="1ac99-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ac99-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ac99-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ac99-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac99-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac99-156">CommonParameters</span></span>
<span data-ttu-id="1ac99-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ac99-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac99-158">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac99-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac99-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ac99-159">INPUTS</span></span>

### <span data-ttu-id="1ac99-160">PSProfile</span><span class="sxs-lookup"><span data-stu-id="1ac99-160">PSProfile</span></span>
<span data-ttu-id="1ac99-161">A ' CdnProfile ' paraméter az "PSProfile" típusú értéket fogadja el a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1ac99-161">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="1ac99-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ac99-162">OUTPUTS</span></span>

### <span data-ttu-id="1ac99-163">Microsoft. Azure. Command. CDN. models. Endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ac99-163">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="1ac99-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ac99-164">NOTES</span></span>

## <span data-ttu-id="1ac99-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ac99-165">RELATED LINKS</span></span>

[<span data-ttu-id="1ac99-166">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ac99-166">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="1ac99-167">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ac99-167">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="1ac99-168">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ac99-168">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="1ac99-169">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ac99-169">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="1ac99-170">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="1ac99-170">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


