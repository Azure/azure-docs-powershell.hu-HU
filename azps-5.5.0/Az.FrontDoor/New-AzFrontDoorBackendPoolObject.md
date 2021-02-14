---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolObject.md
ms.openlocfilehash: 6dba24ae79d051668e88a718402c5e01e81a7461
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147891"
---
# <span data-ttu-id="b5d80-101">New-AzFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="b5d80-101">New-AzFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="b5d80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5d80-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d80-103">PSBackendPool-objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="b5d80-103">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="b5d80-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5d80-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5d80-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5d80-105">DESCRIPTION</span></span>
<span data-ttu-id="b5d80-106">PSBackendPool-objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="b5d80-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="b5d80-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5d80-107">EXAMPLES</span></span>

### <span data-ttu-id="b5d80-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="b5d80-108">Example 1</span></span>
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

<span data-ttu-id="b5d80-109">PSBackendPool-objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="b5d80-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="b5d80-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5d80-110">PARAMETERS</span></span>

### <span data-ttu-id="b5d80-111">-Backend</span><span class="sxs-lookup"><span data-stu-id="b5d80-111">-Backend</span></span>
<span data-ttu-id="b5d80-112">A készlet háttérkészletei.</span><span class="sxs-lookup"><span data-stu-id="b5d80-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="b5d80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d80-113">-DefaultProfile</span></span>
<span data-ttu-id="b5d80-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5d80-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5d80-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="b5d80-115">-FrontDoorName</span></span>
<span data-ttu-id="b5d80-116">Annak a front door-nak a neve, amelyhez ez az útválasztási szabály tartozik.</span><span class="sxs-lookup"><span data-stu-id="b5d80-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="b5d80-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="b5d80-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="b5d80-118">A háttérkészlet állapotbeállításának neve</span><span class="sxs-lookup"><span data-stu-id="b5d80-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="b5d80-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="b5d80-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="b5d80-120">A háttérkészlet terheléselosztási beállításainak neve</span><span class="sxs-lookup"><span data-stu-id="b5d80-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="b5d80-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b5d80-121">-Name</span></span>
<span data-ttu-id="b5d80-122">BackendPool neve.</span><span class="sxs-lookup"><span data-stu-id="b5d80-122">BackendPool name.</span></span>

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

### <span data-ttu-id="b5d80-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5d80-123">-ResourceGroupName</span></span>
<span data-ttu-id="b5d80-124">Az erőforráscsoport neve, amelyből a RoutingRule létrejön.</span><span class="sxs-lookup"><span data-stu-id="b5d80-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="b5d80-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d80-125">CommonParameters</span></span>
<span data-ttu-id="b5d80-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5d80-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d80-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5d80-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d80-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5d80-128">INPUTS</span></span>

### <span data-ttu-id="b5d80-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="b5d80-129">None</span></span>

## <span data-ttu-id="b5d80-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5d80-130">OUTPUTS</span></span>

### <span data-ttu-id="b5d80-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="b5d80-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="b5d80-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5d80-132">NOTES</span></span>

## <span data-ttu-id="b5d80-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5d80-133">RELATED LINKS</span></span>

<span data-ttu-id="b5d80-134">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="b5d80-134">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[New-AzFrontDoorBackendObject](./New-AzFrontDoorBackendObject.md)</span></span>
