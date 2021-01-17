---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 6dba24ae79d051668e88a718402c5e01e81a7461
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466128"
---
# <span data-ttu-id="83799-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="83799-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="83799-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83799-102">SYNOPSIS</span></span>
<span data-ttu-id="83799-103">PSBackendPool-objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="83799-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="83799-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="83799-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83799-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="83799-105">DESCRIPTION</span></span>
<span data-ttu-id="83799-106">PSBackendPool-objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="83799-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="83799-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="83799-107">EXAMPLES</span></span>

### <span data-ttu-id="83799-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="83799-108">Example 1</span></span>
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

<span data-ttu-id="83799-109">PSBackendPool-objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="83799-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="83799-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83799-110">PARAMETERS</span></span>

### <span data-ttu-id="83799-111">-Backend</span><span class="sxs-lookup"><span data-stu-id="83799-111">-Backend</span></span>
<span data-ttu-id="83799-112">A készlet háttérkészletei.</span><span class="sxs-lookup"><span data-stu-id="83799-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="83799-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83799-113">-DefaultProfile</span></span>
<span data-ttu-id="83799-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83799-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83799-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="83799-115">-FrontDoorName</span></span>
<span data-ttu-id="83799-116">Annak a front door-nak a neve, amelyhez ez az útválasztási szabály tartozik.</span><span class="sxs-lookup"><span data-stu-id="83799-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="83799-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="83799-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="83799-118">A háttérkészlet állapotbeállításának neve</span><span class="sxs-lookup"><span data-stu-id="83799-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="83799-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="83799-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="83799-120">A háttérkészlet terheléselosztási beállításainak neve</span><span class="sxs-lookup"><span data-stu-id="83799-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="83799-121">-Name</span><span class="sxs-lookup"><span data-stu-id="83799-121">-Name</span></span>
<span data-ttu-id="83799-122">BackendPool neve.</span><span class="sxs-lookup"><span data-stu-id="83799-122">BackendPool name.</span></span>

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

### <span data-ttu-id="83799-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83799-123">-ResourceGroupName</span></span>
<span data-ttu-id="83799-124">Az erőforráscsoport neve, amelyből a RoutingRule létrejön.</span><span class="sxs-lookup"><span data-stu-id="83799-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="83799-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83799-125">CommonParameters</span></span>
<span data-ttu-id="83799-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83799-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83799-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83799-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83799-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="83799-128">INPUTS</span></span>

### <span data-ttu-id="83799-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="83799-129">None</span></span>

## <span data-ttu-id="83799-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83799-130">OUTPUTS</span></span>

### <span data-ttu-id="83799-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="83799-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="83799-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="83799-132">NOTES</span></span>

## <span data-ttu-id="83799-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83799-133">RELATED LINKS</span></span>

<span data-ttu-id="83799-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="83799-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
