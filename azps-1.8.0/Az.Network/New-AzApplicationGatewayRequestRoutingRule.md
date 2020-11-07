---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 82f14ce9418566793572e2b5722d09460ab1e827
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670393"
---
# <span data-ttu-id="d827c-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d827c-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d827c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d827c-102">SYNOPSIS</span></span>
<span data-ttu-id="d827c-103">Kérés-útválasztási szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d827c-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="d827c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d827c-104">SYNTAX</span></span>

### <span data-ttu-id="d827c-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d827c-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-BackendHttpSettingsId <String>]
 [-HttpListenerId <String>] [-BackendAddressPoolId <String>] [-UrlPathMapId <String>]
 [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d827c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d827c-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d827c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d827c-107">DESCRIPTION</span></span>
<span data-ttu-id="d827c-108">**Az Add-AzApplicationGatewayRequestRoutingRule** parancsmag kérés-útválasztási szabályt hoz létre az Azure Application Gateway rendszerhez.</span><span class="sxs-lookup"><span data-stu-id="d827c-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="d827c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d827c-109">EXAMPLES</span></span>

### <span data-ttu-id="d827c-110">Példa 1: Request útválasztási szabály létrehozása egy alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="d827c-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="d827c-111">Ez a parancs létrehoz egy Rule01 nevű egyszerű kérést, és az eredményt az $Rule nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d827c-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="d827c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d827c-112">PARAMETERS</span></span>

### <span data-ttu-id="d827c-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d827c-113">-BackendAddressPool</span></span>
<span data-ttu-id="d827c-114">A végponti címkészlet objektumként adja meg a létrehozandó útválasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="d827c-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d827c-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="d827c-116">A létrehozáshoz a Request Routing szabálynak a back-end Address Pool ID azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d827c-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d827c-117">-BackendHttpSettings</span></span>
<span data-ttu-id="d827c-118">Itt adhatja meg objektumként a back-end HTTP-beállításokat objektumként a létrehozandó útválasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="d827c-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d827c-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="d827c-120">A létrehozáshoz a Request Routing szabálynak a back-end HTTP Settings AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d827c-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d827c-121">-DefaultProfile</span></span>
<span data-ttu-id="d827c-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d827c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d827c-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="d827c-123">-HttpListener</span></span>
<span data-ttu-id="d827c-124">A létrehozáshoz szükséges útválasztási szabályhoz tartozó back-end HTTP-figyelőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d827c-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="d827c-125">-HttpListenerId</span></span>
<span data-ttu-id="d827c-126">A létrehozandó útválasztási szabály backend-alapú HTTP-figyelő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d827c-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d827c-127">-Name</span></span>
<span data-ttu-id="d827c-128">A parancsmag által létrehozott Request Routing szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d827c-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d827c-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d827c-129">-RedirectConfiguration</span></span>
<span data-ttu-id="d827c-130">Az Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d827c-130">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d827c-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="d827c-132">Az alkalmazás-átjáró RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="d827c-132">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-133">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d827c-133">-RewriteRuleSet</span></span>
<span data-ttu-id="d827c-134">Az Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d827c-134">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-135">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="d827c-135">-RewriteRuleSetId</span></span>
<span data-ttu-id="d827c-136">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="d827c-136">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-137">-RuleType</span><span class="sxs-lookup"><span data-stu-id="d827c-137">-RuleType</span></span>
<span data-ttu-id="d827c-138">A Request Routing szabály típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d827c-138">Specifies type of the request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-139">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="d827c-139">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-140">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="d827c-140">-UrlPathMapId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d827c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d827c-141">CommonParameters</span></span>
<span data-ttu-id="d827c-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d827c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d827c-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d827c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d827c-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d827c-144">INPUTS</span></span>

### <span data-ttu-id="d827c-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="d827c-145">None</span></span>

## <span data-ttu-id="d827c-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d827c-146">OUTPUTS</span></span>

### <span data-ttu-id="d827c-147">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d827c-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d827c-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d827c-148">NOTES</span></span>

## <span data-ttu-id="d827c-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d827c-149">RELATED LINKS</span></span>

[<span data-ttu-id="d827c-150">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d827c-150">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d827c-151">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d827c-151">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d827c-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d827c-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d827c-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d827c-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


