---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466122"
---
# <span data-ttu-id="01d96-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="01d96-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="01d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01d96-102">SYNOPSIS</span></span>
<span data-ttu-id="01d96-103">PSHealthProbeSetting objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="01d96-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="01d96-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01d96-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01d96-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01d96-105">DESCRIPTION</span></span>
<span data-ttu-id="01d96-106">PSHealthProbeSetting objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="01d96-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="01d96-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01d96-107">EXAMPLES</span></span>

### <span data-ttu-id="01d96-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="01d96-108">Example 1</span></span>
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

<span data-ttu-id="01d96-109">Megjegyzés: A HealthProbeMethod beállítás nem megkülönbözteti a kis- és nagybetűket.</span><span class="sxs-lookup"><span data-stu-id="01d96-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="01d96-110">PSHealthProbeSetting objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="01d96-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="01d96-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01d96-111">PARAMETERS</span></span>

### <span data-ttu-id="01d96-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d96-112">-DefaultProfile</span></span>
<span data-ttu-id="01d96-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01d96-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01d96-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="01d96-114">-EnabledState</span></span>
<span data-ttu-id="01d96-115">Engedélyezi-e, hogy a backendPools szolgáltatásban definiált háttértörlelőkre vonatkozó állapotszokásokat ad-e a rendszer.</span><span class="sxs-lookup"><span data-stu-id="01d96-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="01d96-116">Az állapotok csak akkor tilthatók le, ha egy engedélyezett háttérkészletben egyetlen engedélyezett háttérkészlet található.</span><span class="sxs-lookup"><span data-stu-id="01d96-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

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

### <span data-ttu-id="01d96-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="01d96-117">-HealthProbeMethod</span></span>
<span data-ttu-id="01d96-118">Azt adja meg, hogy melyik HTTP-módszert használja a BackendPools csoportban definiált háttér-nek.</span><span class="sxs-lookup"><span data-stu-id="01d96-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="01d96-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="01d96-119">-IntervalInSeconds</span></span>
<span data-ttu-id="01d96-120">Az állapotok közti másodpercek száma.</span><span class="sxs-lookup"><span data-stu-id="01d96-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="01d96-121">Az alapértelmezett érték 30</span><span class="sxs-lookup"><span data-stu-id="01d96-121">Default value is 30</span></span>

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

### <span data-ttu-id="01d96-122">-Name</span><span class="sxs-lookup"><span data-stu-id="01d96-122">-Name</span></span>
<span data-ttu-id="01d96-123">Állapotbeállítás neve.</span><span class="sxs-lookup"><span data-stu-id="01d96-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="01d96-124">-Path</span><span class="sxs-lookup"><span data-stu-id="01d96-124">-Path</span></span>
<span data-ttu-id="01d96-125">Az egészségügyi problémákhoz használt elérési út.</span><span class="sxs-lookup"><span data-stu-id="01d96-125">The path to use for the health probe.</span></span>
<span data-ttu-id="01d96-126">Alapértelmezett érték/</span><span class="sxs-lookup"><span data-stu-id="01d96-126">Default is /</span></span>

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

### <span data-ttu-id="01d96-127">-Protocol</span><span class="sxs-lookup"><span data-stu-id="01d96-127">-Protocol</span></span>
<span data-ttu-id="01d96-128">Protokollrendszer ehhez az alapértelmezett beállításhoz: HTTP</span><span class="sxs-lookup"><span data-stu-id="01d96-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="01d96-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d96-129">CommonParameters</span></span>
<span data-ttu-id="01d96-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01d96-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d96-131">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01d96-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d96-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01d96-132">INPUTS</span></span>

### <span data-ttu-id="01d96-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="01d96-133">None</span></span>
## <span data-ttu-id="01d96-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01d96-134">OUTPUTS</span></span>

### <span data-ttu-id="01d96-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="01d96-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="01d96-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01d96-136">NOTES</span></span>

## <span data-ttu-id="01d96-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01d96-137">RELATED LINKS</span></span>

<span data-ttu-id="01d96-138">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="01d96-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
