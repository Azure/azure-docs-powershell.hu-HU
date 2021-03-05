---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: 127c73a34b030a991b5875f141ea8dd850a4f0a1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009253"
---
# <span data-ttu-id="b3b98-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="b3b98-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="b3b98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3b98-102">SYNOPSIS</span></span>
<span data-ttu-id="b3b98-103">Kézbesítési műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="b3b98-103">Creates a delivery action.</span></span>

## <span data-ttu-id="b3b98-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b3b98-104">SYNTAX</span></span>

### <span data-ttu-id="b3b98-105">CacheExpirationActionParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b3b98-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b98-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3b98-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b98-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3b98-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b98-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3b98-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3b98-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3b98-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3b98-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b3b98-110">DESCRIPTION</span></span>
<span data-ttu-id="b3b98-111">A **New-AzCdnDeliveryRule** parancsmag létrehoz egy kézbesítési szabályt a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="b3b98-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="b3b98-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b3b98-112">EXAMPLES</span></span>

### <span data-ttu-id="b3b98-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="b3b98-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="b3b98-114">Hozzon létre egy egyszerű kézbesítési szabályt.</span><span class="sxs-lookup"><span data-stu-id="b3b98-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="b3b98-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3b98-115">PARAMETERS</span></span>

### <span data-ttu-id="b3b98-116">-Művelet</span><span class="sxs-lookup"><span data-stu-id="b3b98-116">-Action</span></span>
<span data-ttu-id="b3b98-117">Teljesítenünk kell egy műveletet.</span><span class="sxs-lookup"><span data-stu-id="b3b98-117">Action to perform.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="b3b98-118">-CacheBehavior</span></span>
<span data-ttu-id="b3b98-119">A művelet gyorsítótárazása</span><span class="sxs-lookup"><span data-stu-id="b3b98-119">Caching behavior for the action</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="b3b98-120">-CacheDuration</span></span>
<span data-ttu-id="b3b98-121">Az az időtartam, amelyre a tartalmat gyorsítótárazni kell.</span><span class="sxs-lookup"><span data-stu-id="b3b98-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="b3b98-122">Az engedélyezett formátum \[ d. \] óó:pp:mm</span><span class="sxs-lookup"><span data-stu-id="b3b98-122">Allowed format is \[d.\]hh:mm:ss</span></span>

```yaml
Type: System.String
Parameter Sets: CacheExpirationActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="b3b98-123">-CustomFragment</span></span>
<span data-ttu-id="b3b98-124">Az átirányítási URL-címhez hozzáadható töredezettség.</span><span class="sxs-lookup"><span data-stu-id="b3b98-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="b3b98-125">A töredezettség az URL-cím #után következő része.</span><span class="sxs-lookup"><span data-stu-id="b3b98-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="b3b98-126">Ne tartalmazza a #.</span><span class="sxs-lookup"><span data-stu-id="b3b98-126">Do not include the #.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="b3b98-127">-CustomHostname</span></span>
<span data-ttu-id="b3b98-128">Átirányítani kell az állomást.</span><span class="sxs-lookup"><span data-stu-id="b3b98-128">Host to redirect.</span></span>
<span data-ttu-id="b3b98-129">Hagyja üresen, hogy a bejövő állomást használja a cél gazdakiszolgálóként.</span><span class="sxs-lookup"><span data-stu-id="b3b98-129">Leave empty to use the incoming host as the destination host.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="b3b98-130">-CustomPath</span></span>
<span data-ttu-id="b3b98-131">Az átirányítás teljes elérési útja.</span><span class="sxs-lookup"><span data-stu-id="b3b98-131">The full path to redirect.</span></span>
<span data-ttu-id="b3b98-132">Az elérési út nem lehet üres, és a /-val kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="b3b98-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="b3b98-133">Hagyja üresen a bejövő útvonal célvonalként való használatát.</span><span class="sxs-lookup"><span data-stu-id="b3b98-133">Leave empty to use the incoming path as destination path.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="b3b98-134">-CustomQueryString</span></span>
<span data-ttu-id="b3b98-135">Az átirányítás URL-címében elhelyezni kívánt lekérdezési karakterláncok halmaza.</span><span class="sxs-lookup"><span data-stu-id="b3b98-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="b3b98-136">Ha ezt az értéket adná meg, az lecserélné a meglévő lekérdezési karakterláncokat; hagyja üresen a bejövő lekérdezési karakterlánc megőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="b3b98-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="b3b98-137">A lekérdezési karakterláncnak formátumban kell \<key\> = \<value\> lennie.</span><span class="sxs-lookup"><span data-stu-id="b3b98-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="b3b98-138">?</span><span class="sxs-lookup"><span data-stu-id="b3b98-138">?</span></span> <span data-ttu-id="b3b98-139">és & automatikusan megjelenik, ezért ne foglalja bele őket.</span><span class="sxs-lookup"><span data-stu-id="b3b98-139">and & will be added automatically so do not include them.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3b98-140">-DefaultProfile</span></span>
<span data-ttu-id="b3b98-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b3b98-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3b98-142">-Destination</span><span class="sxs-lookup"><span data-stu-id="b3b98-142">-Destination</span></span>
<span data-ttu-id="b3b98-143">Adja meg azt a relatív URL-címet, amelyre a fenti kérelmeket újra fogja írni.</span><span class="sxs-lookup"><span data-stu-id="b3b98-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="b3b98-144">-DestinationProtocol</span></span>
<span data-ttu-id="b3b98-145">Az átirányításhoz használt protokoll.</span><span class="sxs-lookup"><span data-stu-id="b3b98-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="b3b98-146">Az alapértelmezett érték a MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="b3b98-146">The default value is MatchRequest.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="b3b98-147">-HeaderActionType</span></span>
<span data-ttu-id="b3b98-148">A kérelem fejlécének vagy válaszfejlécének módosítása</span><span class="sxs-lookup"><span data-stu-id="b3b98-148">Whether to modify request header or response header</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="b3b98-149">-HeaderName</span></span>
<span data-ttu-id="b3b98-150">A módosítani szükséges fejléc neve.</span><span class="sxs-lookup"><span data-stu-id="b3b98-150">Name of the header to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="b3b98-151">-PreservePath</span></span>
<span data-ttu-id="b3b98-152">Meg kell-e őrizni a nem egyező elérési utat.</span><span class="sxs-lookup"><span data-stu-id="b3b98-152">Whether to preserve unmatched path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="b3b98-153">-QueryParameter</span></span>
<span data-ttu-id="b3b98-154">A felosztani vagy kizárni (vesszővel elválasztott) lekérdezésparaméterek.</span><span class="sxs-lookup"><span data-stu-id="b3b98-154">Query parameters to include or exclude (comma separated).</span></span>

```yaml
Type: System.String[]
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="b3b98-155">-QueryStringBehavior</span></span>
<span data-ttu-id="b3b98-156">QueryString behavior for the requests</span><span class="sxs-lookup"><span data-stu-id="b3b98-156">QueryString behavior for the requests</span></span>

```yaml
Type: System.String
Parameter Sets: CacheKeyQueryStringActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="b3b98-157">-RedirectType</span></span>
<span data-ttu-id="b3b98-158">A szabály által a forgalom átirányításakor használt átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="b3b98-158">The redirect type the rule will use when redirecting traffic</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRedirectActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="b3b98-159">-SourcePattern</span></span>
<span data-ttu-id="b3b98-160">Olyan kérési URI-mintát definiálhat, amely azonosítja az újraírható kérelmek típusát.</span><span class="sxs-lookup"><span data-stu-id="b3b98-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="b3b98-161">Ha az érték üres, az összes karakterlánc egyezést fog hagyni.</span><span class="sxs-lookup"><span data-stu-id="b3b98-161">If value is blank, all strings are matched.</span></span>

```yaml
Type: System.String
Parameter Sets: UrlRewriteActionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-162">-Érték</span><span class="sxs-lookup"><span data-stu-id="b3b98-162">-Value</span></span>
<span data-ttu-id="b3b98-163">A megadott művelet értéke.</span><span class="sxs-lookup"><span data-stu-id="b3b98-163">Value for the specified action.</span></span>

```yaml
Type: System.String
Parameter Sets: HeaderActionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3b98-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3b98-164">CommonParameters</span></span>
<span data-ttu-id="b3b98-165">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3b98-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3b98-166">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3b98-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3b98-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3b98-167">INPUTS</span></span>

### <span data-ttu-id="b3b98-168">Nincs</span><span class="sxs-lookup"><span data-stu-id="b3b98-168">None</span></span>

## <span data-ttu-id="b3b98-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b3b98-169">OUTPUTS</span></span>

### <span data-ttu-id="b3b98-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="b3b98-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="b3b98-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b3b98-171">NOTES</span></span>

## <span data-ttu-id="b3b98-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b3b98-172">RELATED LINKS</span></span>
