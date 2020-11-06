---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: ab053235c928f109321cdf9adf3429e589958ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497540"
---
# <span data-ttu-id="7801d-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7801d-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="7801d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7801d-102">SYNOPSIS</span></span>
<span data-ttu-id="7801d-103">Kérés-útválasztási szabályt hoz létre egy alkalmazás-átjáróhoz.</span><span class="sxs-lookup"><span data-stu-id="7801d-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7801d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7801d-104">SYNTAX</span></span>

### <span data-ttu-id="7801d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7801d-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7801d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7801d-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7801d-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="7801d-107">DESCRIPTION</span></span>
<span data-ttu-id="7801d-108">**Az Add-AzureRmApplicationGatewayRequestRoutingRule** parancsmag kérés-útválasztási szabályt hoz létre az Azure Application Gateway rendszerhez.</span><span class="sxs-lookup"><span data-stu-id="7801d-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="7801d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="7801d-109">EXAMPLES</span></span>

### <span data-ttu-id="7801d-110">Példa 1: Request útválasztási szabály létrehozása egy alkalmazás-átjáróhoz</span><span class="sxs-lookup"><span data-stu-id="7801d-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="7801d-111">Ez a parancs létrehoz egy Rule01 nevű egyszerű kérést, és az eredményt az $Rule nevű változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7801d-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="7801d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7801d-112">PARAMETERS</span></span>

### <span data-ttu-id="7801d-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7801d-113">-BackendAddressPool</span></span>
<span data-ttu-id="7801d-114">A végponti címkészlet objektumként adja meg a létrehozandó útválasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="7801d-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7801d-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="7801d-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="7801d-116">A létrehozáshoz a Request Routing szabálynak a back-end Address Pool ID azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7801d-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7801d-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7801d-117">-BackendHttpSettings</span></span>
<span data-ttu-id="7801d-118">Itt adhatja meg objektumként a back-end HTTP-beállításokat objektumként a létrehozandó útválasztási szabályhoz.</span><span class="sxs-lookup"><span data-stu-id="7801d-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7801d-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="7801d-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="7801d-120">A létrehozáshoz a Request Routing szabálynak a back-end HTTP Settings AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7801d-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7801d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7801d-121">-DefaultProfile</span></span>
<span data-ttu-id="7801d-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7801d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7801d-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="7801d-123">-HttpListener</span></span>
<span data-ttu-id="7801d-124">A létrehozáshoz szükséges útválasztási szabályhoz tartozó back-end HTTP-figyelőt adja meg.</span><span class="sxs-lookup"><span data-stu-id="7801d-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7801d-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="7801d-125">-HttpListenerId</span></span>
<span data-ttu-id="7801d-126">A létrehozandó útválasztási szabály backend-alapú HTTP-figyelő AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7801d-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7801d-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7801d-127">-Name</span></span>
<span data-ttu-id="7801d-128">A parancsmag által létrehozott Request Routing szabály nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7801d-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7801d-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7801d-129">-RedirectConfiguration</span></span>
<span data-ttu-id="7801d-130">Az Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="7801d-130">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7801d-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="7801d-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="7801d-132">Az alkalmazás-átjáró RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="7801d-132">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7801d-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="7801d-133">-RuleType</span></span>
<span data-ttu-id="7801d-134">A Request Routing szabály típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="7801d-134">Specifies type of the request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7801d-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="7801d-135">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7801d-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="7801d-136">-UrlPathMapId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7801d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7801d-137">CommonParameters</span></span>
<span data-ttu-id="7801d-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7801d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7801d-139">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7801d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7801d-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7801d-140">INPUTS</span></span>

### <span data-ttu-id="7801d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7801d-141">System.String</span></span>

## <span data-ttu-id="7801d-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7801d-142">OUTPUTS</span></span>

### <span data-ttu-id="7801d-143">Microsoft. Azure. commands. Network. models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7801d-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="7801d-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7801d-144">NOTES</span></span>

## <span data-ttu-id="7801d-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7801d-145">RELATED LINKS</span></span>

[<span data-ttu-id="7801d-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7801d-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7801d-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7801d-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7801d-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7801d-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7801d-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7801d-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


