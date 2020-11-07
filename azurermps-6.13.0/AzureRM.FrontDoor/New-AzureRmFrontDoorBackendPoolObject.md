---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorbackendpoolobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorBackendPoolObject.md
ms.openlocfilehash: 13b28d236e1c6e758c4f7883285c55017ce5a727
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672932"
---
# <span data-ttu-id="fed43-101">New-AzureRmFrontDoorBackendPoolObject</span><span class="sxs-lookup"><span data-stu-id="fed43-101">New-AzureRmFrontDoorBackendPoolObject</span></span>

## <span data-ttu-id="fed43-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fed43-102">SYNOPSIS</span></span>
<span data-ttu-id="fed43-103">PSBackendPool objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="fed43-103">Create a PSBackendPool object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fed43-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fed43-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorBackendPoolObject -ResourceGroupName <String> -Name <String> -FrontDoorName <String>
 -Backend <PSBackend[]> -LoadBalancingSettingsName <String> -HealthProbeSettingsName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fed43-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fed43-105">DESCRIPTION</span></span>
<span data-ttu-id="fed43-106">PSBackendPool objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="fed43-106">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="fed43-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fed43-107">EXAMPLES</span></span>

### <span data-ttu-id="fed43-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fed43-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorBackendPoolObject -Name "backendpool1" -FrontDoorName $Name -ResourceGroupName $resourceGroupName -Backend $backend1 -He
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

<span data-ttu-id="fed43-109">PSBackendPool objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="fed43-109">Create a PSBackendPool object for Front Door creation</span></span>

## <span data-ttu-id="fed43-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fed43-110">PARAMETERS</span></span>

### <span data-ttu-id="fed43-111">-Backend</span><span class="sxs-lookup"><span data-stu-id="fed43-111">-Backend</span></span>
<span data-ttu-id="fed43-112">A készlet backend-lehetőségei.</span><span class="sxs-lookup"><span data-stu-id="fed43-112">The set of backends for this pool.</span></span>

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

### <span data-ttu-id="fed43-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fed43-113">-DefaultProfile</span></span>
<span data-ttu-id="fed43-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fed43-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fed43-115">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="fed43-115">-FrontDoorName</span></span>
<span data-ttu-id="fed43-116">Annak a bejárati ajtónak a neve, amelyhez ez a művelettervi szabály tartozik.</span><span class="sxs-lookup"><span data-stu-id="fed43-116">The name of the Front Door to which this routing rule belongs.</span></span>

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

### <span data-ttu-id="fed43-117">-HealthProbeSettingsName</span><span class="sxs-lookup"><span data-stu-id="fed43-117">-HealthProbeSettingsName</span></span>
<span data-ttu-id="fed43-118">Az e backend-készlethez tartozó egészségvédelmi szonda beállításainak neve</span><span class="sxs-lookup"><span data-stu-id="fed43-118">The name of the health probe settings for this backend pool</span></span>

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

### <span data-ttu-id="fed43-119">-LoadBalancingSettingsName</span><span class="sxs-lookup"><span data-stu-id="fed43-119">-LoadBalancingSettingsName</span></span>
<span data-ttu-id="fed43-120">A backend-készlet terheléselosztási beállításainak neve</span><span class="sxs-lookup"><span data-stu-id="fed43-120">The name of the load balancing settings for this backend pool</span></span>

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

### <span data-ttu-id="fed43-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fed43-121">-Name</span></span>
<span data-ttu-id="fed43-122">BackendPool neve</span><span class="sxs-lookup"><span data-stu-id="fed43-122">BackendPool name.</span></span>

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

### <span data-ttu-id="fed43-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fed43-123">-ResourceGroupName</span></span>
<span data-ttu-id="fed43-124">Annak az erőforráscsoport-névnek a neve, amelyet a RoutingRule fog létrehozni.</span><span class="sxs-lookup"><span data-stu-id="fed43-124">The resource group name that the RoutingRule will be created in.</span></span>

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

### <span data-ttu-id="fed43-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed43-125">CommonParameters</span></span>
<span data-ttu-id="fed43-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fed43-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed43-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fed43-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed43-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fed43-128">INPUTS</span></span>

### <span data-ttu-id="fed43-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="fed43-129">None</span></span>

## <span data-ttu-id="fed43-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fed43-130">OUTPUTS</span></span>

### <span data-ttu-id="fed43-131">Microsoft. Azure. Command. FrontDoor. models. PSBackendPool</span><span class="sxs-lookup"><span data-stu-id="fed43-131">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool</span></span>

## <span data-ttu-id="fed43-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fed43-132">NOTES</span></span>

## <span data-ttu-id="fed43-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fed43-133">RELATED LINKS</span></span>

<span data-ttu-id="fed43-134">[Új – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [Új – AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span><span class="sxs-lookup"><span data-stu-id="fed43-134">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorBackendObject](./New-AzureRmFrontDoorBackendObject.md)</span></span>
