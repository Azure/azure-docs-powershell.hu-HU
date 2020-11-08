---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 8fc8f6785e9b6eda55615fb1e2ececbaf9ab0349
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194273"
---
# <span data-ttu-id="d3517-101">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d3517-101">New-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d3517-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3517-102">SYNOPSIS</span></span>
<span data-ttu-id="d3517-103">Kérés-útválasztási szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="d3517-103">Creates a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="d3517-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3517-104">SYNTAX</span></span>

### <span data-ttu-id="d3517-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3517-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String> [-BackendHttpSettingsId <String>]
 [-HttpListenerId <String>] [-BackendAddressPoolId <String>] [-UrlPathMapId <String>]
 [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3517-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d3517-106">SetByResource</span></span>
```
New-AzApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3517-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3517-107">DESCRIPTION</span></span>
<span data-ttu-id="d3517-108">**Az Add-AzApplicationGatewayRequestRoutingRule** parancsmag kérés-útválasztási szabályt hoz létre az Azure Application Gateway rendszerhez.</span><span class="sxs-lookup"><span data-stu-id="d3517-108">**The Add-AzApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="d3517-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d3517-109">EXAMPLES</span></span>

### <span data-ttu-id="d3517-110">Példa 1: Request útválasztási szabály létrehozása egy alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="d3517-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="d3517-111">Ez a parancs létrehoz egy Rule01 nevű egyszerű kérést, és az eredményt az $Rule nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="d3517-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="d3517-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3517-112">PARAMETERS</span></span>

### <span data-ttu-id="d3517-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="d3517-113">-BackendAddressPool</span></span>
<span data-ttu-id="d3517-114">A végponti címkészlet objektumként adja meg a létrehozandó útválasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="d3517-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="d3517-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="d3517-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="d3517-116">A létrehozáshoz a Request Routing szabálynak a back-end Address Pool ID azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3517-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="d3517-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="d3517-117">-BackendHttpSettings</span></span>
<span data-ttu-id="d3517-118">Itt adhatja meg objektumként a back-end HTTP-beállításokat objektumként a létrehozandó útválasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="d3517-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

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

### <span data-ttu-id="d3517-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="d3517-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="d3517-120">A létrehozáshoz a Request Routing szabálynak a back-end HTTP Settings AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3517-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

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

### <span data-ttu-id="d3517-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3517-121">-DefaultProfile</span></span>
<span data-ttu-id="d3517-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3517-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3517-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="d3517-123">-HttpListener</span></span>
<span data-ttu-id="d3517-124">A létrehozáshoz szükséges útválasztási szabályhoz tartozó back-end HTTP-figyelőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3517-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

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

### <span data-ttu-id="d3517-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="d3517-125">-HttpListenerId</span></span>
<span data-ttu-id="d3517-126">A létrehozandó útválasztási szabály backend-alapú HTTP-figyelő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3517-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

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

### <span data-ttu-id="d3517-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d3517-127">-Name</span></span>
<span data-ttu-id="d3517-128">A parancsmag által létrehozott Request Routing szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3517-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d3517-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3517-129">-RedirectConfiguration</span></span>
<span data-ttu-id="d3517-130">Az Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3517-130">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="d3517-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d3517-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="d3517-132">Az alkalmazás-átjáró RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="d3517-132">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="d3517-133">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3517-133">-RewriteRuleSet</span></span>
<span data-ttu-id="d3517-134">Az Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="d3517-134">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="d3517-135">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="d3517-135">-RewriteRuleSetId</span></span>
<span data-ttu-id="d3517-136">Az alkalmazás-átjáró RewriteRuleSet azonosítója</span><span class="sxs-lookup"><span data-stu-id="d3517-136">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="d3517-137">-RuleType</span><span class="sxs-lookup"><span data-stu-id="d3517-137">-RuleType</span></span>
<span data-ttu-id="d3517-138">A Request Routing szabály típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3517-138">Specifies type of the request routing rule.</span></span>

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

### <span data-ttu-id="d3517-139">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="d3517-139">-UrlPathMap</span></span>
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

### <span data-ttu-id="d3517-140">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="d3517-140">-UrlPathMapId</span></span>
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

### <span data-ttu-id="d3517-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3517-141">CommonParameters</span></span>
<span data-ttu-id="d3517-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3517-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3517-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3517-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3517-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3517-144">INPUTS</span></span>

### <span data-ttu-id="d3517-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="d3517-145">None</span></span>

## <span data-ttu-id="d3517-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3517-146">OUTPUTS</span></span>

### <span data-ttu-id="d3517-147">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d3517-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="d3517-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3517-148">NOTES</span></span>

## <span data-ttu-id="d3517-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3517-149">RELATED LINKS</span></span>

[<span data-ttu-id="d3517-150">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d3517-150">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d3517-151">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d3517-151">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d3517-152">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d3517-152">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="d3517-153">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="d3517-153">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

