---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 4d65985d724033244f761748634adb3b2002a199
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928122"
---
# <span data-ttu-id="7fbda-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="7fbda-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="7fbda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fbda-102">SYNOPSIS</span></span>
<span data-ttu-id="7fbda-103">PSHealthProbeSetting objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="7fbda-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="7fbda-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7fbda-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fbda-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7fbda-105">DESCRIPTION</span></span>
<span data-ttu-id="7fbda-106">PSHealthProbeSetting objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="7fbda-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="7fbda-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7fbda-107">EXAMPLES</span></span>

### <span data-ttu-id="7fbda-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="7fbda-108">Example 1</span></span>
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

<span data-ttu-id="7fbda-109">Megjegyzés: A HealthProbeMethod beállítás nem megkülönbözteti a kis- és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="7fbda-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="7fbda-110">PSHealthProbeSetting objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="7fbda-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="7fbda-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fbda-111">PARAMETERS</span></span>

### <span data-ttu-id="7fbda-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fbda-112">-DefaultProfile</span></span>
<span data-ttu-id="7fbda-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7fbda-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fbda-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="7fbda-114">-EnabledState</span></span>
<span data-ttu-id="7fbda-115">Engedélyezi-e, hogy a backendPools szolgáltatásban definiált háttértörlelőkre vonatkozó állapotszokásokat ad-e a rendszer.</span><span class="sxs-lookup"><span data-stu-id="7fbda-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="7fbda-116">Az állapotok csak akkor tilthatók le, ha egy engedélyezett háttérkészletben egyetlen engedélyezett háttérkészlet található.</span><span class="sxs-lookup"><span data-stu-id="7fbda-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="7fbda-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="7fbda-117">-HealthProbeMethod</span></span>
<span data-ttu-id="7fbda-118">Azt adja meg, hogy melyik HTTP-módszert használja a BackendPools csoportban definiált háttér-nek.</span><span class="sxs-lookup"><span data-stu-id="7fbda-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="7fbda-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7fbda-119">-IntervalInSeconds</span></span>
<span data-ttu-id="7fbda-120">Az állapotok közti másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="7fbda-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="7fbda-121">Az alapértelmezett érték 30</span><span class="sxs-lookup"><span data-stu-id="7fbda-121">Default value is 30</span></span>

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

### <span data-ttu-id="7fbda-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7fbda-122">-Name</span></span>
<span data-ttu-id="7fbda-123">Állapotbeállítás neve.</span><span class="sxs-lookup"><span data-stu-id="7fbda-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="7fbda-124">-Path</span><span class="sxs-lookup"><span data-stu-id="7fbda-124">-Path</span></span>
<span data-ttu-id="7fbda-125">Az egészségügyi problémákhoz használt elérési út.</span><span class="sxs-lookup"><span data-stu-id="7fbda-125">The path to use for the health probe.</span></span>
<span data-ttu-id="7fbda-126">Alapértelmezett érték/</span><span class="sxs-lookup"><span data-stu-id="7fbda-126">Default is /</span></span>

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

### <span data-ttu-id="7fbda-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="7fbda-127">-Protocol</span></span>
<span data-ttu-id="7fbda-128">Protokollrendszer ehhez az alapértelmezett beállításhoz: HTTP</span><span class="sxs-lookup"><span data-stu-id="7fbda-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="7fbda-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fbda-129">CommonParameters</span></span>
<span data-ttu-id="7fbda-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fbda-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fbda-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fbda-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fbda-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7fbda-132">INPUTS</span></span>

### <span data-ttu-id="7fbda-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="7fbda-133">None</span></span>
## <span data-ttu-id="7fbda-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7fbda-134">OUTPUTS</span></span>

### <span data-ttu-id="7fbda-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="7fbda-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="7fbda-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7fbda-136">NOTES</span></span>

## <span data-ttu-id="7fbda-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7fbda-137">RELATED LINKS</span></span>

<span data-ttu-id="7fbda-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="7fbda-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
