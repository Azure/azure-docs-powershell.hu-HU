---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrewriteruleurlconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRewriteRuleUrlConfiguration.md
ms.openlocfilehash: ca77d1c3490c8e22a22c98682065bcd32a5b98bc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379314"
---
# <span data-ttu-id="6d537-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d537-101">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>

## <span data-ttu-id="6d537-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d537-102">SYNOPSIS</span></span>
<span data-ttu-id="6d537-103">Újraírt szabály URL-konfigurációját hozza létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="6d537-103">Creates a rewrite rule url configuration for an application gateway.</span></span>

## <span data-ttu-id="6d537-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6d537-104">SYNTAX</span></span>

```
New-AzApplicationGatewayRewriteRuleUrlConfiguration [-ModifiedPath <String>] [-ModifiedQueryString <String>] [-Reroute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d537-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6d537-105">DESCRIPTION</span></span>
<span data-ttu-id="6d537-106">**AzApplicationGatewayRewriteRuleUrlConfiguration** parancsmag létrehoz egy újraírási szabály URL-konfigurációját egy Azure-alkalmazás átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="6d537-106">**The AzApplicationGatewayRewriteRuleUrlConfiguration** cmdlet creates a rewrite rule url configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="6d537-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6d537-107">EXAMPLES</span></span>

### <span data-ttu-id="6d537-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="6d537-108">Example 1</span></span>
```powershell
PS C:\> $urlConfiguration = New-AzApplicationGatewayRewriteRuleUrlConfiguration -ModifiedPath "/abc" -ModifiedQueryString "x=y&a=b"
```

<span data-ttu-id="6d537-109">Ez a parancs létrehoz egy átírási szabály URL-konfigurációját, és az eredményt a következő nevű változóban $urlConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6d537-109">This command creates a rewrite rule url configuration and stores the result in the variable named $urlConfiguration.</span></span>

<span data-ttu-id="6d537-110">Ha egy meglévő UrlConfigurációt szeretne frissíteni, ezt úgy tudja megtenni, hogy létrehoz egy új UrlConfigurációt, és hozzárendeli az új UrlConfiguration tulajdonságot az Újraírási szabály műveletkészlet UrlConfiguration tulajdonságához.</span><span class="sxs-lookup"><span data-stu-id="6d537-110">If you want to update any existing UrlConfiguration, you can do it by creating a new UrlConfiguration and assigning the new UrlConfiguration to the UrlConfiguration property of Rewrite Rule Action Set.</span></span>

## <span data-ttu-id="6d537-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d537-111">PARAMETERS</span></span>

### <span data-ttu-id="6d537-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d537-112">-DefaultProfile</span></span>
<span data-ttu-id="6d537-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6d537-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d537-114">-ModifiedPath</span><span class="sxs-lookup"><span data-stu-id="6d537-114">-ModifiedPath</span></span>
<span data-ttu-id="6d537-115">URL elérési út értéke.</span><span class="sxs-lookup"><span data-stu-id="6d537-115">Url path value.</span></span>

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

### <span data-ttu-id="6d537-116">-ModifiedQueryString</span><span class="sxs-lookup"><span data-stu-id="6d537-116">-ModifiedQueryString</span></span>
<span data-ttu-id="6d537-117">Url query string value.</span><span class="sxs-lookup"><span data-stu-id="6d537-117">Url query string value.</span></span>

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

### <span data-ttu-id="6d537-118">-Reroute</span><span class="sxs-lookup"><span data-stu-id="6d537-118">-Reroute</span></span>
<span data-ttu-id="6d537-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span><span class="sxs-lookup"><span data-stu-id="6d537-119">Flag to re-evaluate the url path map provided in path based request routing rules using modified path.</span></span>

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

### <span data-ttu-id="6d537-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d537-120">CommonParameters</span></span>
<span data-ttu-id="6d537-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d537-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d537-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d537-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d537-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d537-123">INPUTS</span></span>

### <span data-ttu-id="6d537-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="6d537-124">None</span></span>

## <span data-ttu-id="6d537-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6d537-125">OUTPUTS</span></span>

### <span data-ttu-id="6d537-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d537-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlConfiguration</span></span>

## <span data-ttu-id="6d537-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6d537-127">NOTES</span></span>

## <span data-ttu-id="6d537-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6d537-128">RELATED LINKS</span></span>

[<span data-ttu-id="6d537-129">Add-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d537-129">Add-AzApplicationGatewayRewriteRuleSet</span></span>](./Add-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6d537-130">Get-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d537-130">Get-AzApplicationGatewayRewriteRuleSet</span></span>](./Get-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6d537-131">New-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d537-131">New-AzApplicationGatewayRewriteRuleSet</span></span>](./New-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6d537-132">Remove-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d537-132">Remove-AzApplicationGatewayRewriteRuleSet</span></span>](./Remove-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6d537-133">Set-AzApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="6d537-133">Set-AzApplicationGatewayRewriteRuleSet</span></span>](./Set-AzApplicationGatewayRewriteRuleSet.md)

[<span data-ttu-id="6d537-134">New-AzApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="6d537-134">New-AzApplicationGatewayRewriteRule</span></span>](./New-AzApplicationGatewayRewriteRule.md)

[<span data-ttu-id="6d537-135">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="6d537-135">New-AzApplicationGatewayRewriteRuleActionSet</span></span>](./New-AzApplicationGatewayRewriteRuleActionSet.md)