---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: a1e5c02c1764d9d5284e28c8921ef09888a9d245
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666422"
---
# <span data-ttu-id="fdea8-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="fdea8-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="fdea8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fdea8-102">SYNOPSIS</span></span>
<span data-ttu-id="fdea8-103">PSLoadBalancingSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="fdea8-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="fdea8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fdea8-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdea8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fdea8-105">DESCRIPTION</span></span>
<span data-ttu-id="fdea8-106">PSLoadBalancingSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="fdea8-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="fdea8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fdea8-107">EXAMPLES</span></span>

### <span data-ttu-id="fdea8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fdea8-108">Example 1</span></span>
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

<span data-ttu-id="fdea8-109">PSLoadBalancingSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="fdea8-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="fdea8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fdea8-110">PARAMETERS</span></span>

### <span data-ttu-id="fdea8-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="fdea8-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="fdea8-112">A Szondák további késése ezredmásodpercben a legalacsonyabb késésű gyűjtőben.</span><span class="sxs-lookup"><span data-stu-id="fdea8-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="fdea8-113">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="fdea8-113">Default value is 0</span></span>

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

### <span data-ttu-id="fdea8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdea8-114">-DefaultProfile</span></span>
<span data-ttu-id="fdea8-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fdea8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdea8-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fdea8-116">-Name</span></span>
<span data-ttu-id="fdea8-117">az állapot-szonda beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="fdea8-117">health probe setting name.</span></span>

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

### <span data-ttu-id="fdea8-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="fdea8-118">-SampleSize</span></span>
<span data-ttu-id="fdea8-119">A terheléselosztási döntésekhez figyelembe vett minták száma.</span><span class="sxs-lookup"><span data-stu-id="fdea8-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="fdea8-120">Az alapértelmezett érték 4</span><span class="sxs-lookup"><span data-stu-id="fdea8-120">Default value is 4</span></span>

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

### <span data-ttu-id="fdea8-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="fdea8-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="fdea8-122">A minta időszakra eső minták száma, amelyeknek az alapértelmezett értéknek kell lennie 2</span><span class="sxs-lookup"><span data-stu-id="fdea8-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="fdea8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdea8-123">CommonParameters</span></span>
<span data-ttu-id="fdea8-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fdea8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdea8-125">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fdea8-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdea8-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdea8-126">INPUTS</span></span>

### <span data-ttu-id="fdea8-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="fdea8-127">None</span></span>

## <span data-ttu-id="fdea8-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fdea8-128">OUTPUTS</span></span>

### <span data-ttu-id="fdea8-129">Microsoft. Azure. Command. FrontDoor. models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="fdea8-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="fdea8-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fdea8-130">NOTES</span></span>

## <span data-ttu-id="fdea8-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fdea8-131">RELATED LINKS</span></span>

<span data-ttu-id="fdea8-132">[Új – AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="fdea8-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
