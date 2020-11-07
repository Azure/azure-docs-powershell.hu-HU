---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F312FD6E-AF0F-4901-B763-741E1B46A654
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: e43d5277566311fe77ee239d88e55f658aca8b40
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848422"
---
# <span data-ttu-id="5941f-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5941f-101">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5941f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5941f-102">SYNOPSIS</span></span>
<span data-ttu-id="5941f-103">URL-elérésiút-megfeleltetések tömbjét hozza létre a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="5941f-103">Creates an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5941f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5941f-104">SYNTAX</span></span>

### <span data-ttu-id="5941f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5941f-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5941f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5941f-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayUrlPathMapConfig -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5941f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5941f-107">DESCRIPTION</span></span>
<span data-ttu-id="5941f-108">A **New-AzureRmApplicationGatewayUrlPathMapConfig** parancsmag az URL-címek tömbjét hozza létre a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="5941f-108">The **New-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5941f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="5941f-109">EXAMPLES</span></span>

### <span data-ttu-id="5941f-110">Példa 1: URL-elérésiút-megfeleltetések tömbje létrehozása egy backend-kiszolgáló készletéből</span><span class="sxs-lookup"><span data-stu-id="5941f-110">Example 1: Create an array of URL path mappings to a backend server pool</span></span>
```
PS C:\>New-AzureRmApplicationGatewayUrlPathMapConfig -Name $UrlPathMapName -PathRules $VideoPathRule, $ImagePathRule -DefaultBackendAddressPool $Pool -DefaultBackendHttpSettings $PoolSetting02
```

<span data-ttu-id="5941f-111">Ez a parancs URL-elérésiút-megfeleltetések tömbjét hozza létre a backend-kiszolgálók készletéből.</span><span class="sxs-lookup"><span data-stu-id="5941f-111">This command creates an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="5941f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5941f-112">PARAMETERS</span></span>

### <span data-ttu-id="5941f-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5941f-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="5941f-114">Az alapértelmezett backend-címkészletet adja meg az átirányításhoz, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="5941f-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5941f-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5941f-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="5941f-116">Az alapértelmezett backend-címkészlet AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5941f-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="5941f-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5941f-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="5941f-118">Az alapértelmezett backend-HTTP-beállításokat adja meg, ha a *pathRules* paraméterben megadott szabályok egyike sem egyezik meg.</span><span class="sxs-lookup"><span data-stu-id="5941f-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5941f-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5941f-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="5941f-120">Az alapértelmezett backend-HTTP-beállítások AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5941f-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="5941f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5941f-121">-DefaultProfile</span></span>
<span data-ttu-id="5941f-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5941f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5941f-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5941f-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="5941f-124">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5941f-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5941f-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5941f-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="5941f-126">Az alkalmazás-átjáró alapértelmezett RedirectConfiguration azonosítója</span><span class="sxs-lookup"><span data-stu-id="5941f-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5941f-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5941f-127">-Name</span></span>
<span data-ttu-id="5941f-128">Itt adhatja meg a parancsmag által létrehozott URL-elérési út megfeleltetésének nevét.</span><span class="sxs-lookup"><span data-stu-id="5941f-128">Specifies the URL path map name that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5941f-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="5941f-129">-PathRules</span></span>
<span data-ttu-id="5941f-130">Az elérésiút-szabályok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5941f-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="5941f-131">Ügyeljen arra, hogy az elérésiút-szabályok a megrendelésük során bizalmasak legyenek, ezeket a program a megadott sorrendben alkalmazza.</span><span class="sxs-lookup"><span data-stu-id="5941f-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5941f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5941f-132">CommonParameters</span></span>
<span data-ttu-id="5941f-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5941f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5941f-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5941f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5941f-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5941f-135">INPUTS</span></span>

## <span data-ttu-id="5941f-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5941f-136">OUTPUTS</span></span>

### <span data-ttu-id="5941f-137">Microsoft. Azure. commands. Network. models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="5941f-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="5941f-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5941f-138">NOTES</span></span>

## <span data-ttu-id="5941f-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5941f-139">RELATED LINKS</span></span>

[<span data-ttu-id="5941f-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5941f-140">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5941f-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5941f-141">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5941f-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5941f-142">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5941f-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5941f-143">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


