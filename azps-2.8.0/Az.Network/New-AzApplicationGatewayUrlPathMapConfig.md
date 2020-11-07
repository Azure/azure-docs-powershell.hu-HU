---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 1e9a97d01fd42bae636d93311b41bc6150394d9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93837483"
---
# <span data-ttu-id="8a985-101">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8a985-101">New-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="8a985-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8a985-102">SYNOPSIS</span></span>
<span data-ttu-id="8a985-103">URL-elérésiút-megfeleltetések tömbjét hozza létre a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="8a985-103">Creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="8a985-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8a985-104">SYNTAX</span></span>

### <span data-ttu-id="8a985-105">BackendSetByResource (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8a985-105">BackendSetByResource (Default)</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a985-106">BackendSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a985-106">BackendSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPoolId <String> -DefaultBackendHttpSettingsId <String>
 [-DefaultRewriteRuleSetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a985-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="8a985-107">RedirectSetByResource</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a985-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a985-108">RedirectSetByResourceId</span></span>
```
New-AzApplicationGatewayUrlPathMapConfig -Name <String> -PathRules <PSApplicationGatewayPathRule[]>
 [-DefaultRewriteRuleSetId <String>] -DefaultRedirectConfigurationId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a985-109">Leírás</span><span class="sxs-lookup"><span data-stu-id="8a985-109">DESCRIPTION</span></span>
<span data-ttu-id="8a985-110">A **New-AzApplicationGatewayUrlPathMapConfig** parancsmag az URL-címek tömbjét hozza létre a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="8a985-110">The **New-AzApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="8a985-111">Példák</span><span class="sxs-lookup"><span data-stu-id="8a985-111">EXAMPLES</span></span>

### <span data-ttu-id="8a985-112">Példa 1: URL-elérésiút-megfeleltetések tömbje létrehozása egy backend-kiszolgáló készletéből</span><span class="sxs-lookup"><span data-stu-id="8a985-112">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="8a985-113">Ez a parancs URL-elérésiút-megfeleltetések tömbjét hozza létre a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="8a985-113">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="8a985-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8a985-114">PARAMETERS</span></span>

### <span data-ttu-id="8a985-115">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8a985-115">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="8a985-116">Az alapértelmezett backend-címkészletet adja meg az átirányításhoz, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="8a985-116">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a985-117">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="8a985-117">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="8a985-118">Az alapértelmezett backend-címkészlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a985-118">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a985-119">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="8a985-119">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="8a985-120">Az alapértelmezett backend-HTTP-beállításokat adja meg, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="8a985-120">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a985-121">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="8a985-121">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="8a985-122">Az alapértelmezett backend-HTTP-beállítások AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a985-122">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a985-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a985-123">-DefaultProfile</span></span>
<span data-ttu-id="8a985-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8a985-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a985-125">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a985-125">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="8a985-126">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a985-126">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a985-127">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="8a985-127">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="8a985-128">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="8a985-128">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a985-129">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="8a985-129">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="8a985-130">Az alkalmazás-átjáró alapértelmezett átírási szabály beállítása</span><span class="sxs-lookup"><span data-stu-id="8a985-130">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a985-131">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="8a985-131">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="8a985-132">Az alkalmazás-átjáró alapértelmezett átírási szabályának azonosítója</span><span class="sxs-lookup"><span data-stu-id="8a985-132">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a985-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8a985-133">-Name</span></span>
<span data-ttu-id="8a985-134">Itt adhatja meg a parancsmag által létrehozott URL-elérési út megfeleltetésének nevét.</span><span class="sxs-lookup"><span data-stu-id="8a985-134">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8a985-135">-PathRules</span><span class="sxs-lookup"><span data-stu-id="8a985-135">-PathRules</span></span>
<span data-ttu-id="8a985-136">Az elérésiút-szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8a985-136">Specifies a list of path rules.</span></span>
<span data-ttu-id="8a985-137">Ügyeljen arra, hogy az elérésiút-szabályok a megrendelésük során bizalmasak legyenek, ezeket a program a megadott sorrendben alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="8a985-137">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a985-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a985-138">CommonParameters</span></span>
<span data-ttu-id="8a985-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8a985-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a985-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a985-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a985-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a985-141">INPUTS</span></span>

### <span data-ttu-id="8a985-142">Nincs</span><span class="sxs-lookup"><span data-stu-id="8a985-142">None</span></span>

## <span data-ttu-id="8a985-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8a985-143">OUTPUTS</span></span>

### <span data-ttu-id="8a985-144">Microsoft. Azure. commands. Network. models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="8a985-144">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="8a985-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8a985-145">NOTES</span></span>

## <span data-ttu-id="8a985-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8a985-146">RELATED LINKS</span></span>

[<span data-ttu-id="8a985-147">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8a985-147">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8a985-148">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8a985-148">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8a985-149">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8a985-149">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="8a985-150">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="8a985-150">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


