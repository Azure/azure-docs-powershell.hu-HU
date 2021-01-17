---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469785"
---
# <span data-ttu-id="f8b4e-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="f8b4e-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="f8b4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8b4e-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b4e-103">PSLoadBalancingSetting objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f8b4e-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="f8b4e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f8b4e-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8b4e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f8b4e-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b4e-106">PSLoadBalancingSetting objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f8b4e-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="f8b4e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f8b4e-107">EXAMPLES</span></span>

### <span data-ttu-id="f8b4e-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="f8b4e-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="f8b4e-109">PSLoadBalancingSetting objektum létrehozása a Front Door létrehozásához</span><span class="sxs-lookup"><span data-stu-id="f8b4e-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="f8b4e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8b4e-110">PARAMETERS</span></span>

### <span data-ttu-id="f8b4e-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="f8b4e-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="f8b4e-112">A további késés ezredmásodpercben, hogy a késések a legkisebb késési gyűjtőbe csökkennek.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="f8b4e-113">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="f8b4e-113">Default value is 0</span></span>

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

### <span data-ttu-id="f8b4e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b4e-114">-DefaultProfile</span></span>
<span data-ttu-id="f8b4e-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8b4e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f8b4e-116">-Name</span></span>
<span data-ttu-id="f8b4e-117">egészségügyi állapot beállításának neve.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-117">health probe setting name.</span></span>

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

### <span data-ttu-id="f8b4e-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="f8b4e-118">-SampleSize</span></span>
<span data-ttu-id="f8b4e-119">A terheléselosztási döntésekhez megfontolt minták száma.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="f8b4e-120">Az alapértelmezett érték 4</span><span class="sxs-lookup"><span data-stu-id="f8b4e-120">Default value is 4</span></span>

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

### <span data-ttu-id="f8b4e-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="f8b4e-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="f8b4e-122">A mintaidőszakon belül az alapértelmezett értéknek megfelelő minták száma 2</span><span class="sxs-lookup"><span data-stu-id="f8b4e-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="f8b4e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b4e-123">CommonParameters</span></span>
<span data-ttu-id="f8b4e-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b4e-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8b4e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b4e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8b4e-126">INPUTS</span></span>

### <span data-ttu-id="f8b4e-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="f8b4e-127">None</span></span>

## <span data-ttu-id="f8b4e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8b4e-128">OUTPUTS</span></span>

### <span data-ttu-id="f8b4e-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="f8b4e-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="f8b4e-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f8b4e-130">NOTES</span></span>

## <span data-ttu-id="f8b4e-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8b4e-131">RELATED LINKS</span></span>

<span data-ttu-id="f8b4e-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="f8b4e-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
