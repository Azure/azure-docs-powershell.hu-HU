---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: d893850105656a9f599870e2ef17a6b195254ad6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025532"
---
# <span data-ttu-id="bcc14-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="bcc14-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="bcc14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bcc14-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc14-103">Létrehoz egy kézbesítési tevékenységet.</span><span class="sxs-lookup"><span data-stu-id="bcc14-103">Creates a delivery action.</span></span>

## <span data-ttu-id="bcc14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bcc14-104">SYNTAX</span></span>

### <span data-ttu-id="bcc14-105">CacheExpirationActionParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bcc14-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcc14-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcc14-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcc14-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcc14-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcc14-108">CacheKeyQueryStringActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcc14-108">CacheKeyQueryStringActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -QueryStringBehavior <String> [-QueryParameter <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcc14-109">UrlRewriteActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bcc14-109">UrlRewriteActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -SourcePattern <String> -Destination <String> [-PreservePath]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcc14-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="bcc14-110">DESCRIPTION</span></span>
<span data-ttu-id="bcc14-111">A **New-AzCdnDeliveryRule** parancsmag szállítási szabályt hoz létre a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="bcc14-111">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="bcc14-112">Példák</span><span class="sxs-lookup"><span data-stu-id="bcc14-112">EXAMPLES</span></span>

### <span data-ttu-id="bcc14-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="bcc14-113">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="bcc14-114">Egyszerű kézbesítési szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="bcc14-114">Create a simple delivery rule.</span></span>

## <span data-ttu-id="bcc14-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bcc14-115">PARAMETERS</span></span>

### <span data-ttu-id="bcc14-116">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="bcc14-116">-Action</span></span>
<span data-ttu-id="bcc14-117">Végrehajtani kívánt művelet.</span><span class="sxs-lookup"><span data-stu-id="bcc14-117">Action to perform.</span></span>

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

### <span data-ttu-id="bcc14-118">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="bcc14-118">-CacheBehavior</span></span>
<span data-ttu-id="bcc14-119">A műveletek gyorsítótárazási viselkedése</span><span class="sxs-lookup"><span data-stu-id="bcc14-119">Caching behavior for the action</span></span>

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

### <span data-ttu-id="bcc14-120">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="bcc14-120">-CacheDuration</span></span>
<span data-ttu-id="bcc14-121">Az az időtartam, amelyre a tartalmat gyorsítótárazni kell.</span><span class="sxs-lookup"><span data-stu-id="bcc14-121">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="bcc14-122">Engedélyezett formátum: \[ d. \] óó: PP: SS</span><span class="sxs-lookup"><span data-stu-id="bcc14-122">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="bcc14-123">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="bcc14-123">-CustomFragment</span></span>
<span data-ttu-id="bcc14-124">Az átirányítási URL-címhez hozzáadni kívánt részlet</span><span class="sxs-lookup"><span data-stu-id="bcc14-124">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="bcc14-125">A töredék a # után elkerülő URL-cím része.</span><span class="sxs-lookup"><span data-stu-id="bcc14-125">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="bcc14-126">Ne szerepeljen a #.</span><span class="sxs-lookup"><span data-stu-id="bcc14-126">Do not include the #.</span></span>

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

### <span data-ttu-id="bcc14-127">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="bcc14-127">-CustomHostname</span></span>
<span data-ttu-id="bcc14-128">Állomás átirányítását.</span><span class="sxs-lookup"><span data-stu-id="bcc14-128">Host to redirect.</span></span>
<span data-ttu-id="bcc14-129">Hagyja üresen a bejövő állomás rendeltetési állomásként való használatát.</span><span class="sxs-lookup"><span data-stu-id="bcc14-129">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="bcc14-130">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="bcc14-130">-CustomPath</span></span>
<span data-ttu-id="bcc14-131">Az átirányítás teljes elérési útja.</span><span class="sxs-lookup"><span data-stu-id="bcc14-131">The full path to redirect.</span></span>
<span data-ttu-id="bcc14-132">Az elérési út nem lehet üres, és a/értékkel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="bcc14-132">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="bcc14-133">Hagyja üresen a bejövő út rendeltetési útvonalként való használatát.</span><span class="sxs-lookup"><span data-stu-id="bcc14-133">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="bcc14-134">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="bcc14-134">-CustomQueryString</span></span>
<span data-ttu-id="bcc14-135">Az átirányítási URL-címben elhelyezni kívánt lekérdezési karakterláncok halmaza.</span><span class="sxs-lookup"><span data-stu-id="bcc14-135">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="bcc14-136">Beállítás: az érték felülírhatja a meglévő lekérdezési karakterláncokat; hagyja üresen a bejövő lekérdezési karakterlánc megőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="bcc14-136">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="bcc14-137">A lekérdezési karakterláncnak formátumban kell lennie \<key\> = \<value\> .</span><span class="sxs-lookup"><span data-stu-id="bcc14-137">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="bcc14-138">?</span><span class="sxs-lookup"><span data-stu-id="bcc14-138">?</span></span> <span data-ttu-id="bcc14-139">a & automatikusan felveszi a program, hogy ne szerepeljenek benne.</span><span class="sxs-lookup"><span data-stu-id="bcc14-139">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="bcc14-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc14-140">-DefaultProfile</span></span>
<span data-ttu-id="bcc14-141">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bcc14-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcc14-142">-Destination (cél)</span><span class="sxs-lookup"><span data-stu-id="bcc14-142">-Destination</span></span>
<span data-ttu-id="bcc14-143">Adja meg azt a relatív URL-címet, amelyre a fenti kérelmeket át szeretné írni.</span><span class="sxs-lookup"><span data-stu-id="bcc14-143">Define the relative URL to which the above requests will be rewritten by.</span></span>

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

### <span data-ttu-id="bcc14-144">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="bcc14-144">-DestinationProtocol</span></span>
<span data-ttu-id="bcc14-145">Az átirányítás számára használandó protokoll.</span><span class="sxs-lookup"><span data-stu-id="bcc14-145">Protocol to use for the redirect.</span></span>
<span data-ttu-id="bcc14-146">Az alapértelmezett érték a MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="bcc14-146">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="bcc14-147">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="bcc14-147">-HeaderActionType</span></span>
<span data-ttu-id="bcc14-148">Szeretné-e módosítani a kérés fejlécét vagy a válasz fejlécét</span><span class="sxs-lookup"><span data-stu-id="bcc14-148">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="bcc14-149">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="bcc14-149">-HeaderName</span></span>
<span data-ttu-id="bcc14-150">Annak a fejlécnek a neve, amelyet módosítani szeretne.</span><span class="sxs-lookup"><span data-stu-id="bcc14-150">Name of the header to modify.</span></span>

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

### <span data-ttu-id="bcc14-151">-PreservePath</span><span class="sxs-lookup"><span data-stu-id="bcc14-151">-PreservePath</span></span>
<span data-ttu-id="bcc14-152">A nem egyező elérési út megőrzése</span><span class="sxs-lookup"><span data-stu-id="bcc14-152">Whether to preserve unmatched path.</span></span>

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

### <span data-ttu-id="bcc14-153">-QueryParameter</span><span class="sxs-lookup"><span data-stu-id="bcc14-153">-QueryParameter</span></span>
<span data-ttu-id="bcc14-154">A befoglalni vagy kizárni kívánt lekérdezési paraméterek (vesszővel elválasztva).</span><span class="sxs-lookup"><span data-stu-id="bcc14-154">Query parameters to include or exclude (comma separated).</span></span>

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

### <span data-ttu-id="bcc14-155">-QueryStringBehavior</span><span class="sxs-lookup"><span data-stu-id="bcc14-155">-QueryStringBehavior</span></span>
<span data-ttu-id="bcc14-156">A QueryString viselkedése a kérésekhez</span><span class="sxs-lookup"><span data-stu-id="bcc14-156">QueryString behavior for the requests</span></span>

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

### <span data-ttu-id="bcc14-157">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="bcc14-157">-RedirectType</span></span>
<span data-ttu-id="bcc14-158">Az átirányítás típusa, amelyet a szabály a forgalom átirányításakor fog használni</span><span class="sxs-lookup"><span data-stu-id="bcc14-158">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="bcc14-159">-SourcePattern</span><span class="sxs-lookup"><span data-stu-id="bcc14-159">-SourcePattern</span></span>
<span data-ttu-id="bcc14-160">Adjon meg egy olyan kérés URI-mintát, amely azonosítja az esetleg átírni kívánt kérések típusát.</span><span class="sxs-lookup"><span data-stu-id="bcc14-160">Define a request URI pattern that identifies the type of requests that may be rewritten.</span></span> <span data-ttu-id="bcc14-161">Ha az érték üres, a program az összes karakterláncot egyezteti.</span><span class="sxs-lookup"><span data-stu-id="bcc14-161">If value is blank, all strings are matched.</span></span>

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

### <span data-ttu-id="bcc14-162">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="bcc14-162">-Value</span></span>
<span data-ttu-id="bcc14-163">A megadott tevékenység értéke</span><span class="sxs-lookup"><span data-stu-id="bcc14-163">Value for the specified action.</span></span>

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

### <span data-ttu-id="bcc14-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc14-164">CommonParameters</span></span>
<span data-ttu-id="bcc14-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bcc14-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc14-166">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bcc14-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc14-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcc14-167">INPUTS</span></span>

### <span data-ttu-id="bcc14-168">Nincs</span><span class="sxs-lookup"><span data-stu-id="bcc14-168">None</span></span>

## <span data-ttu-id="bcc14-169">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bcc14-169">OUTPUTS</span></span>

### <span data-ttu-id="bcc14-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="bcc14-170">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="bcc14-171">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bcc14-171">NOTES</span></span>

## <span data-ttu-id="bcc14-172">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bcc14-172">RELATED LINKS</span></span>
