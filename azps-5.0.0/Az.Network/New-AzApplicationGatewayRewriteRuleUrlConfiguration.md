---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302759"
---
# <span data-ttu-id="3bfdd-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bfdd-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="3bfdd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3bfdd-102">SYNOPSIS</span></span>
<span data-ttu-id="3bfdd-103">Új szabály URL-konfigurációjának létrehozása egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="3bfdd-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="3bfdd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3bfdd-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bfdd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3bfdd-105">DESCRIPTION</span></span>
<span data-ttu-id="3bfdd-106">**Az AzApplicationGatewayRewriteRuleUrlConfiguration** parancsmag létrehoz egy átírási szabály URL-konfigurációját az Azure Application Gateway számára.</span><span class="sxs-lookup"><span data-stu-id="3bfdd-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="3bfdd-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3bfdd-107">EXAMPLES</span></span>

### <span data-ttu-id="3bfdd-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3bfdd-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="3bfdd-109">Ez a parancs létrehoz egy rewrite szabály URL-konfigurációját, és az eredményt az $urlConfiguration nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="3bfdd-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="3bfdd-110">Ha frissíteni szeretné bármelyik meglévő UrlConfiguration, megteheti azt egy új UrlConfiguration létrehozásával és az új UrlConfiguration hozzárendelésével.</span><span class="sxs-lookup"><span data-stu-id="3bfdd-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="3bfdd-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3bfdd-111">PARAMETERS</span></span>

### <span data-ttu-id="3bfdd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bfdd-112">-DefaultProfile</span></span>
<span data-ttu-id="3bfdd-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3bfdd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bfdd-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="3bfdd-114">-ModifiedPath</span></span>
<span data-ttu-id="3bfdd-115">URL-elérési út értéke</span><span class="sxs-lookup"><span data-stu-id="3bfdd-115">Url path value.</span></span>

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

### <span data-ttu-id="3bfdd-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="3bfdd-116">-ModifiedQueryString</span></span>
<span data-ttu-id="3bfdd-117">URL-lekérdezés karakterláncának értéke.</span><span class="sxs-lookup"><span data-stu-id="3bfdd-117">Url query string value.</span></span>

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

### <span data-ttu-id="3bfdd-118">-Átirányítás</span><span class="sxs-lookup"><span data-stu-id="3bfdd-118">-Reroute</span></span>
<span data-ttu-id="3bfdd-119">Jelölő: a Path based Request (elérési út) útválasztási szabályokban megadott URL-megfeleltetés újraértékelése módosított elérési úttal.</span><span class="sxs-lookup"><span data-stu-id="3bfdd-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bfdd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bfdd-120">CommonParameters</span></span>
<span data-ttu-id="3bfdd-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3bfdd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bfdd-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3bfdd-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bfdd-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bfdd-123">INPUTS</span></span>

### <span data-ttu-id="3bfdd-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="3bfdd-124">None</span></span>

## <span data-ttu-id="3bfdd-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3bfdd-125">OUTPUTS</span></span>

### <span data-ttu-id="3bfdd-126">Microsoft. Azure. commands. Network. models. PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="3bfdd-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="3bfdd-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3bfdd-127">NOTES</span></span>

## <span data-ttu-id="3bfdd-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3bfdd-128">RELATED LINKS</span></span>

[<span data-ttu-id="3bfdd-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3bfdd-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3bfdd-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3bfdd-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3bfdd-131">Új – AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3bfdd-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3bfdd-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3bfdd-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3bfdd-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="3bfdd-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="3bfdd-134">Új – AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="3bfdd-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="3bfdd-135">Új – AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="3bfdd-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)