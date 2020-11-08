---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 6dba24ae79d051668e88a718402c5e01e81a7461
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017763"
---
# <span data-ttu-id="cf601-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="cf601-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="cf601-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf601-102">SYNOPSIS</span></span>
<span data-ttu-id="cf601-103">PSBackendPool objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="cf601-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="cf601-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf601-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf601-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf601-105">DESCRIPTION</span></span>
<span data-ttu-id="cf601-106">PSBackendPool objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="cf601-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="cf601-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cf601-107">EXAMPLES</span></span>

### <span data-ttu-id="cf601-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cf601-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
althProbeSettingsName "healthProbeSetting1" -LoadBalancingSettingsName "loadBalancingSetting1"


Backends                : {Microsoft.Azure.Commands.FrontDoor.Models.PSBackend}
LoadBalancingSettingRef : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/LoadBalancingSettings/loadBalancingSetting1
HealthProbeSettingRef   : /subscriptions/{subid}/resourceGroups/{resourceGroupName}/providers
                          /Microsoft.Network/frontDoors/frontdoor5/HealthProbeSettings/healthProbeSetting1
EnabledState            : Enabled
ResourceState           :
Id                      :
Name                    : backendpool1
Type                    :
```

<span data-ttu-id="cf601-109">PSBackendPool objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="cf601-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="cf601-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf601-110">PARAMETERS</span></span>

### <span data-ttu-id="cf601-111">-Backend</span><span class="sxs-lookup"><span data-stu-id="cf601-111">-Backend</span></span>
<span data-ttu-id="cf601-112">A készlet backend-lehetőségei.</span><span class="sxs-lookup"><span data-stu-id="cf601-112">The set of backends for this pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackend[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf601-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf601-113">-DefaultProfile</span></span>
<span data-ttu-id="cf601-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf601-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf601-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="cf601-115">-FrontDoorName</span></span>
<span data-ttu-id="cf601-116">Annak a bejárati ajtónak a neve, amelyhez ez a művelettervi szabály tartozik.</span><span class="sxs-lookup"><span data-stu-id="cf601-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="cf601-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="cf601-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="cf601-118">Az e backend-készlethez tartozó egészségvédelmi szonda beállításainak neve</span><span class="sxs-lookup"><span data-stu-id="cf601-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="cf601-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="cf601-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="cf601-120">A backend-készlet terheléselosztási beállításainak neve</span><span class="sxs-lookup"><span data-stu-id="cf601-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="cf601-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cf601-121">-Name</span></span>
<span data-ttu-id="cf601-122">BackendPool neve</span><span class="sxs-lookup"><span data-stu-id="cf601-122">BackendPool name.</span></span>

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

### <span data-ttu-id="cf601-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf601-123">-ResourceGroupName</span></span>
<span data-ttu-id="cf601-124">Annak az erőforráscsoport-névnek a neve, amelyet a RoutingRule fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="cf601-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="cf601-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf601-125">CommonParameters</span></span>
<span data-ttu-id="cf601-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf601-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf601-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cf601-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf601-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf601-128">INPUTS</span></span>

### <span data-ttu-id="cf601-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="cf601-129">None</span></span>

## <span data-ttu-id="cf601-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf601-130">OUTPUTS</span></span>

### <span data-ttu-id="cf601-131">Microsoft. Azure. Command. FrontDoor. models. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="cf601-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="cf601-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf601-132">NOTES</span></span>

## <span data-ttu-id="cf601-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf601-133">RELATED LINKS</span></span>

<span data-ttu-id="cf601-134">[Új – AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Új – AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="cf601-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
