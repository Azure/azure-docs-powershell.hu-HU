---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145106"
---
# <span data-ttu-id="c8841-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="c8841-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="c8841-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8841-102">SYNOPSIS</span></span>
<span data-ttu-id="c8841-103">Kézbesítési műveletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="c8841-103">Creates a delivery action.</span></span>

## <span data-ttu-id="c8841-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c8841-104">SYNTAX</span></span>

### <span data-ttu-id="c8841-105">CacheExpirationActionParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c8841-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8841-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8841-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8841-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8841-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8841-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8841-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8841-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8841-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8841-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c8841-110">DESCRIPTION</span></span>
<span data-ttu-id="c8841-111">A **New-AzCdnDeliveryRule** parancsmag kézbesítési szabályt hoz létre a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="c8841-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="c8841-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c8841-112">EXAMPLES</span></span>

### <span data-ttu-id="c8841-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="c8841-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="c8841-114">Hozzon létre egy egyszerű kézbesítési szabályt.</span><span class="sxs-lookup"><span data-stu-id="c8841-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="c8841-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8841-115">PARAMETERS</span></span>

### <span data-ttu-id="c8841-116">-Action</span><span class="sxs-lookup"><span data-stu-id="c8841-116">-Action</span></span>
<span data-ttu-id="c8841-117">Teljesítenünk kell egy műveletet.</span><span class="sxs-lookup"><span data-stu-id="c8841-117">Action to perform.</span></span>

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

### <span data-ttu-id="c8841-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="c8841-118">-CacheBehavior</span></span>
<span data-ttu-id="c8841-119">A művelet gyorsítótárazása</span><span class="sxs-lookup"><span data-stu-id="c8841-119">Caching behavior for the action</span></span>

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

### <span data-ttu-id="c8841-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="c8841-120">-CacheDuration</span></span>
<span data-ttu-id="c8841-121">Az az időtartam, amelyre a tartalmat gyorsítótárazni kell.</span><span class="sxs-lookup"><span data-stu-id="c8841-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="c8841-122">Az engedélyezett formátum \[ d. \] óó:pp:mm</span><span class="sxs-lookup"><span data-stu-id="c8841-122">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="c8841-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="c8841-123">-CustomFragment</span></span>
<span data-ttu-id="c8841-124">Az átirányítás URL-címéhez hozzáadható töredezettség.</span><span class="sxs-lookup"><span data-stu-id="c8841-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="c8841-125">A feldarabolás az URL-cím #után következő része.</span><span class="sxs-lookup"><span data-stu-id="c8841-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="c8841-126">Ne tartalmazza a #.</span><span class="sxs-lookup"><span data-stu-id="c8841-126">Do not include the #.</span></span>

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

### <span data-ttu-id="c8841-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="c8841-127">-CustomHostname</span></span>
<span data-ttu-id="c8841-128">Átirányítani kell az állomást.</span><span class="sxs-lookup"><span data-stu-id="c8841-128">Host to redirect.</span></span>
<span data-ttu-id="c8841-129">Hagyja üresen, hogy a bejövő állomást használja a cél gazdakiszolgálóként.</span><span class="sxs-lookup"><span data-stu-id="c8841-129">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="c8841-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="c8841-130">-CustomPath</span></span>
<span data-ttu-id="c8841-131">Az átirányítás teljes elérési útja.</span><span class="sxs-lookup"><span data-stu-id="c8841-131">The full path to redirect.</span></span>
<span data-ttu-id="c8841-132">Az elérési út nem lehet üres, és a /-val kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="c8841-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="c8841-133">Hagyja üresen a bejövő útvonal célvonalként való használatát.</span><span class="sxs-lookup"><span data-stu-id="c8841-133">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="c8841-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="c8841-134">-CustomQueryString</span></span>
<span data-ttu-id="c8841-135">Az átirányítási URL-címbe helyező lekérdezési karakterláncok halmaza.</span><span class="sxs-lookup"><span data-stu-id="c8841-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="c8841-136">Ennek az értéknek a beállítása lecserélné a meglévő lekérdezési karakterláncokat; hagyja üresen a bejövő lekérdezési karakterlánc megőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="c8841-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="c8841-137">A lekérdezési karakterláncnak formátumban kell \<key\> = \<value\> lennie.</span><span class="sxs-lookup"><span data-stu-id="c8841-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="c8841-138">?</span><span class="sxs-lookup"><span data-stu-id="c8841-138">?</span></span> <span data-ttu-id="c8841-139">és & automatikusan megjelenik, ezért ne foglalja bele őket a programba.</span><span class="sxs-lookup"><span data-stu-id="c8841-139">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="c8841-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8841-140">-DefaultProfile</span></span>
<span data-ttu-id="c8841-141">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8841-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8841-142">-Destination</span><span class="sxs-lookup"><span data-stu-id="c8841-142">-Destination</span></span>
<span data-ttu-id="c8841-143">Adja meg azt a relatív URL-címet, amelyre a fenti kérelmeket át fogja írni.</span><span class="sxs-lookup"><span data-stu-id="c8841-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

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

### <span data-ttu-id="c8841-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="c8841-144">-DestinationProtocol</span></span>
<span data-ttu-id="c8841-145">Az átirányításhoz használt protokoll.</span><span class="sxs-lookup"><span data-stu-id="c8841-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="c8841-146">Az alapértelmezett érték a MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="c8841-146">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="c8841-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="c8841-147">-HeaderActionType</span></span>
<span data-ttu-id="c8841-148">A kérelem fejlécének vagy válaszfejlécének módosítása</span><span class="sxs-lookup"><span data-stu-id="c8841-148">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="c8841-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="c8841-149">-HeaderName</span></span>
<span data-ttu-id="c8841-150">A módosítani szükséges fejléc neve.</span><span class="sxs-lookup"><span data-stu-id="c8841-150">Name of the header to modify.</span></span>

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

### <span data-ttu-id="c8841-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="c8841-151">-PreservePath</span></span>
<span data-ttu-id="c8841-152">Meg kell-e őrizni a nem egyező elérési utat.</span><span class="sxs-lookup"><span data-stu-id="c8841-152">Whether to preserve unmatched path.</span></span>

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

### <span data-ttu-id="c8841-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="c8841-153">-QueryParameter</span></span>
<span data-ttu-id="c8841-154">A felosztani vagy kizárni (vesszővel elválasztott) lekérdezésparaméterek.</span><span class="sxs-lookup"><span data-stu-id="c8841-154">Query parameters to include or exclude (comma separated).</span></span>

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

### <span data-ttu-id="c8841-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="c8841-155">-QueryStringBehavior</span></span>
<span data-ttu-id="c8841-156">QueryString behavior for the requests</span><span class="sxs-lookup"><span data-stu-id="c8841-156">QueryString behavior for the requests</span></span>

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

### <span data-ttu-id="c8841-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="c8841-157">-RedirectType</span></span>
<span data-ttu-id="c8841-158">A szabály által a forgalom átirányításakor használt átirányítás típusa</span><span class="sxs-lookup"><span data-stu-id="c8841-158">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="c8841-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="c8841-159">-SourcePattern</span></span>
<span data-ttu-id="c8841-160">Definiálja a kérelem URI-mintáját, amely azonosítja az újraírható kérelmek típusát.</span><span class="sxs-lookup"><span data-stu-id="c8841-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="c8841-161">Ha az érték üres, az összes karakterlánc egyezést fog hagyni.</span><span class="sxs-lookup"><span data-stu-id="c8841-161">If value is blank, all strings are matched.</span></span>

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

### <span data-ttu-id="c8841-162">-Érték</span><span class="sxs-lookup"><span data-stu-id="c8841-162">-Value</span></span>
<span data-ttu-id="c8841-163">A megadott művelet értéke.</span><span class="sxs-lookup"><span data-stu-id="c8841-163">Value for the specified action.</span></span>

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

### <span data-ttu-id="c8841-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8841-164">CommonParameters</span></span>
<span data-ttu-id="c8841-165">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8841-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8841-166">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8841-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8841-167">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8841-167">INPUTS</span></span>

### <span data-ttu-id="c8841-168">Nincs</span><span class="sxs-lookup"><span data-stu-id="c8841-168">None</span></span>

## <span data-ttu-id="c8841-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8841-169">OUTPUTS</span></span>

### <span data-ttu-id="c8841-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="c8841-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="c8841-171">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c8841-171">NOTES</span></span>

## <span data-ttu-id="c8841-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8841-172">RELATED LINKS</span></span>
