---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94184944"
---
# <span data-ttu-id="8fd35-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="8fd35-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="8fd35-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fd35-102">SYNOPSIS</span></span>
<span data-ttu-id="8fd35-103">PSHealthProbeSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="8fd35-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="8fd35-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fd35-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fd35-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fd35-105">DESCRIPTION</span></span>
<span data-ttu-id="8fd35-106">PSHealthProbeSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="8fd35-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="8fd35-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8fd35-107">EXAMPLES</span></span>

### <span data-ttu-id="8fd35-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8fd35-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
HealthProbeMethod : Head
EnabledState      : Enabled
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="8fd35-109">Megjegyzés: a HealthProbeMethod beállítás nem megkülönbözteti a kis-és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="8fd35-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="8fd35-110">PSHealthProbeSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="8fd35-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="8fd35-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fd35-111">PARAMETERS</span></span>

### <span data-ttu-id="8fd35-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fd35-112">-DefaultProfile</span></span>
<span data-ttu-id="8fd35-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fd35-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fd35-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="8fd35-114">-EnabledState</span></span>
<span data-ttu-id="8fd35-115">Engedélyezi-e a backendPools-ban meghatározott backend-próbák állapotát.</span><span class="sxs-lookup"><span data-stu-id="8fd35-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="8fd35-116">Az egészségügyi Szondák csak akkor tilthatók le, ha egyetlen engedélyezett backend van a backend-készletben.</span><span class="sxs-lookup"><span data-stu-id="8fd35-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd35-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="8fd35-117">-HealthProbeMethod</span></span>
<span data-ttu-id="8fd35-118">Beállíthatja, hogy melyik HTTP-módszert használja a backendPools csoportban definiált backend-problémák megoldásához.</span><span class="sxs-lookup"><span data-stu-id="8fd35-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="8fd35-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8fd35-119">-IntervalInSeconds</span></span>
<span data-ttu-id="8fd35-120">Az egészségügyi Szondák közötti másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="8fd35-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="8fd35-121">Az alapértelmezett érték 30</span><span class="sxs-lookup"><span data-stu-id="8fd35-121">Default value is 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd35-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8fd35-122">-Name</span></span>
<span data-ttu-id="8fd35-123">Az állapot-szonda beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="8fd35-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="8fd35-124">-Path (elérési út)</span><span class="sxs-lookup"><span data-stu-id="8fd35-124">-Path</span></span>
<span data-ttu-id="8fd35-125">Az állapot-szonda használati útvonala.</span><span class="sxs-lookup"><span data-stu-id="8fd35-125">The path to use for the health probe.</span></span>
<span data-ttu-id="8fd35-126">Alapértelmezett érték/</span><span class="sxs-lookup"><span data-stu-id="8fd35-126">Default is /</span></span>

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

### <span data-ttu-id="8fd35-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="8fd35-127">-Protocol</span></span>
<span data-ttu-id="8fd35-128">Az ehhez a szonda alapértelmezett értékéhez használandó Protocol-séma HTTP</span><span class="sxs-lookup"><span data-stu-id="8fd35-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fd35-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fd35-129">CommonParameters</span></span>
<span data-ttu-id="8fd35-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fd35-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fd35-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8fd35-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fd35-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fd35-132">INPUTS</span></span>

### <span data-ttu-id="8fd35-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="8fd35-133">None</span></span>
## <span data-ttu-id="8fd35-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fd35-134">OUTPUTS</span></span>

### <span data-ttu-id="8fd35-135">Microsoft. Azure. Command. FrontDoor. models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="8fd35-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="8fd35-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fd35-136">NOTES</span></span>

## <span data-ttu-id="8fd35-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fd35-137">RELATED LINKS</span></span>

<span data-ttu-id="8fd35-138">[Új – AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="8fd35-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>