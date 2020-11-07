---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdndeliveryruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnDeliveryRuleAction.md
ms.openlocfilehash: a1ebadb47bbde091ca6b430fab86111b35bf34bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667587"
---
# <span data-ttu-id="5077b-101">New-AzCdnDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="5077b-101">New-AzCdnDeliveryRuleAction</span></span>

## <span data-ttu-id="5077b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5077b-102">SYNOPSIS</span></span>
<span data-ttu-id="5077b-103">Létrehoz egy kézbesítési tevékenységet.</span><span class="sxs-lookup"><span data-stu-id="5077b-103">Creates a delivery action.</span></span>

## <span data-ttu-id="5077b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5077b-104">SYNTAX</span></span>

### <span data-ttu-id="5077b-105">CacheExpirationActionParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5077b-105">CacheExpirationActionParameterSet (Default)</span></span>
```
New-AzCdnDeliveryRuleAction -CacheBehavior <String> [-CacheDuration <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5077b-106">HeaderActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5077b-106">HeaderActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -HeaderActionType <String> -Action <String> -HeaderName <String> [-Value <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5077b-107">UrlRedirectActionParameterSet</span><span class="sxs-lookup"><span data-stu-id="5077b-107">UrlRedirectActionParameterSet</span></span>
```
New-AzCdnDeliveryRuleAction -RedirectType <String> [-DestinationProtocol <String>] [-CustomPath <String>]
 [-CustomHostname <String>] [-CustomQueryString <String>] [-CustomFragment <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5077b-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="5077b-108">DESCRIPTION</span></span>
<span data-ttu-id="5077b-109">A **New-AzCdnDeliveryRule** parancsmag szállítási szabályt hoz létre a CDN-végpontok létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="5077b-109">The **New-AzCdnDeliveryRule** cmdlet creates a delivery rule for CDN endpoint creation.</span></span>

## <span data-ttu-id="5077b-110">Példák</span><span class="sxs-lookup"><span data-stu-id="5077b-110">EXAMPLES</span></span>

### <span data-ttu-id="5077b-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5077b-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnDeliveryRuleAction -HeaderActionType ModifyRequestHeader -Action Append -HeaderName "Accept-Encoding" -Value "gzip"

HeaderActionType    Action HeaderName      Value
----------------    ------ ----------      -----
ModifyRequestHeader Append Accept-Encoding gzip
```

<span data-ttu-id="5077b-112">Egyszerű kézbesítési szabály létrehozása</span><span class="sxs-lookup"><span data-stu-id="5077b-112">Create a simple delivery rule.</span></span>

## <span data-ttu-id="5077b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5077b-113">PARAMETERS</span></span>

### <span data-ttu-id="5077b-114">-Műveletek</span><span class="sxs-lookup"><span data-stu-id="5077b-114">-Action</span></span>
<span data-ttu-id="5077b-115">Végrehajtani kívánt művelet.</span><span class="sxs-lookup"><span data-stu-id="5077b-115">Action to perform.</span></span>

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

### <span data-ttu-id="5077b-116">-CacheBehavior</span><span class="sxs-lookup"><span data-stu-id="5077b-116">-CacheBehavior</span></span>
<span data-ttu-id="5077b-117">A műveletek gyorsítótárazási viselkedése</span><span class="sxs-lookup"><span data-stu-id="5077b-117">Caching behavior for the action</span></span>

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

### <span data-ttu-id="5077b-118">-CacheDuration</span><span class="sxs-lookup"><span data-stu-id="5077b-118">-CacheDuration</span></span>
<span data-ttu-id="5077b-119">Az az időtartam, amelyre a tartalmat gyorsítótárazni kell.</span><span class="sxs-lookup"><span data-stu-id="5077b-119">The duration for which the content needs to be cached.</span></span>
<span data-ttu-id="5077b-120">Engedélyezett formátum: \[ d. \] óó: PP: SS</span><span class="sxs-lookup"><span data-stu-id="5077b-120">Allowed format is \[d.\]hh:mm:ss</span></span>

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

### <span data-ttu-id="5077b-121">-CustomFragment</span><span class="sxs-lookup"><span data-stu-id="5077b-121">-CustomFragment</span></span>
<span data-ttu-id="5077b-122">Az átirányítási URL-címhez hozzáadni kívánt részlet</span><span class="sxs-lookup"><span data-stu-id="5077b-122">Fragment to add to the redirect URL.</span></span>
<span data-ttu-id="5077b-123">A töredék a # után elkerülő URL-cím része.</span><span class="sxs-lookup"><span data-stu-id="5077b-123">Fragment is the part of the URL that comes after #.</span></span>
<span data-ttu-id="5077b-124">Ne szerepeljen a #.</span><span class="sxs-lookup"><span data-stu-id="5077b-124">Do not include the #.</span></span>

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

### <span data-ttu-id="5077b-125">-CustomHostname</span><span class="sxs-lookup"><span data-stu-id="5077b-125">-CustomHostname</span></span>
<span data-ttu-id="5077b-126">Állomás átirányítását.</span><span class="sxs-lookup"><span data-stu-id="5077b-126">Host to redirect.</span></span>
<span data-ttu-id="5077b-127">Hagyja üresen a bejövő állomás rendeltetési állomásként való használatát.</span><span class="sxs-lookup"><span data-stu-id="5077b-127">Leave empty to use the incoming host as the destination host.</span></span>

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

### <span data-ttu-id="5077b-128">-CustomPath</span><span class="sxs-lookup"><span data-stu-id="5077b-128">-CustomPath</span></span>
<span data-ttu-id="5077b-129">Az átirányítás teljes elérési útja.</span><span class="sxs-lookup"><span data-stu-id="5077b-129">The full path to redirect.</span></span>
<span data-ttu-id="5077b-130">Az elérési út nem lehet üres, és a/értékkel kell kezdődnie.</span><span class="sxs-lookup"><span data-stu-id="5077b-130">Path cannot be empty and must start with /.</span></span>
<span data-ttu-id="5077b-131">Hagyja üresen a bejövő út rendeltetési útvonalként való használatát.</span><span class="sxs-lookup"><span data-stu-id="5077b-131">Leave empty to use the incoming path as destination path.</span></span>

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

### <span data-ttu-id="5077b-132">-CustomQueryString</span><span class="sxs-lookup"><span data-stu-id="5077b-132">-CustomQueryString</span></span>
<span data-ttu-id="5077b-133">Az átirányítási URL-címben elhelyezni kívánt lekérdezési karakterláncok halmaza.</span><span class="sxs-lookup"><span data-stu-id="5077b-133">The set of query strings to be placed in the redirect URL.</span></span>
<span data-ttu-id="5077b-134">Beállítás: az érték felülírhatja a meglévő lekérdezési karakterláncokat; hagyja üresen a bejövő lekérdezési karakterlánc megőrzéséhez.</span><span class="sxs-lookup"><span data-stu-id="5077b-134">Setting this value would replace any existing query string; leave empty to preserve the incoming query string.</span></span>
<span data-ttu-id="5077b-135">A lekérdezési karakterláncnak \< fontos \> = \< érték \> formátumúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="5077b-135">Query string must be in \<key\>=\<value\> format.</span></span>
<span data-ttu-id="5077b-136">?</span><span class="sxs-lookup"><span data-stu-id="5077b-136">?</span></span> <span data-ttu-id="5077b-137">a & automatikusan felveszi a program, hogy ne szerepeljenek benne.</span><span class="sxs-lookup"><span data-stu-id="5077b-137">and & will be added automatically so do not include them.</span></span>

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

### <span data-ttu-id="5077b-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5077b-138">-DefaultProfile</span></span>
<span data-ttu-id="5077b-139">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5077b-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5077b-140">-DestinationProtocol</span><span class="sxs-lookup"><span data-stu-id="5077b-140">-DestinationProtocol</span></span>
<span data-ttu-id="5077b-141">Az átirányítás számára használandó protokoll.</span><span class="sxs-lookup"><span data-stu-id="5077b-141">Protocol to use for the redirect.</span></span>
<span data-ttu-id="5077b-142">Az alapértelmezett érték a MatchRequest.</span><span class="sxs-lookup"><span data-stu-id="5077b-142">The default value is MatchRequest.</span></span>

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

### <span data-ttu-id="5077b-143">-HeaderActionType</span><span class="sxs-lookup"><span data-stu-id="5077b-143">-HeaderActionType</span></span>
<span data-ttu-id="5077b-144">Szeretné-e módosítani a kérés fejlécét vagy a válasz fejlécét</span><span class="sxs-lookup"><span data-stu-id="5077b-144">Whether to modify request header or response header</span></span>

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

### <span data-ttu-id="5077b-145">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="5077b-145">-HeaderName</span></span>
<span data-ttu-id="5077b-146">Annak a fejlécnek a neve, amelyet módosítani szeretne.</span><span class="sxs-lookup"><span data-stu-id="5077b-146">Name of the header to modify.</span></span>

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

### <span data-ttu-id="5077b-147">-RedirectType</span><span class="sxs-lookup"><span data-stu-id="5077b-147">-RedirectType</span></span>
<span data-ttu-id="5077b-148">Az átirányítás típusa, amelyet a szabály a forgalom átirányításakor fog használni</span><span class="sxs-lookup"><span data-stu-id="5077b-148">The redirect type the rule will use when redirecting traffic</span></span>

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

### <span data-ttu-id="5077b-149">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="5077b-149">-Value</span></span>
<span data-ttu-id="5077b-150">A megadott tevékenység értéke</span><span class="sxs-lookup"><span data-stu-id="5077b-150">Value for the specified action.</span></span>

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

### <span data-ttu-id="5077b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5077b-151">CommonParameters</span></span>
<span data-ttu-id="5077b-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5077b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5077b-153">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="5077b-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5077b-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5077b-154">INPUTS</span></span>

### <span data-ttu-id="5077b-155">Nincs</span><span class="sxs-lookup"><span data-stu-id="5077b-155">None</span></span>

## <span data-ttu-id="5077b-156">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5077b-156">OUTPUTS</span></span>

### <span data-ttu-id="5077b-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span><span class="sxs-lookup"><span data-stu-id="5077b-157">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSDeliveryRuleAction</span></span>

## <span data-ttu-id="5077b-158">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5077b-158">NOTES</span></span>

## <span data-ttu-id="5077b-159">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5077b-159">RELATED LINKS</span></span>
