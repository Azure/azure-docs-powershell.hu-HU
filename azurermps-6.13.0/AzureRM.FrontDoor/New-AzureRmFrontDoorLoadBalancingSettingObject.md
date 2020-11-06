---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: de13a33aeaf60dbd83fcacebb8380bee27c18c46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494056"
---
# <span data-ttu-id="2bcf0-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="2bcf0-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="2bcf0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2bcf0-102">SYNOPSIS</span></span>
<span data-ttu-id="2bcf0-103">PSLoadBalancingSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="2bcf0-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bcf0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2bcf0-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bcf0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2bcf0-105">DESCRIPTION</span></span>
<span data-ttu-id="2bcf0-106">PSLoadBalancingSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="2bcf0-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="2bcf0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2bcf0-107">EXAMPLES</span></span>

### <span data-ttu-id="2bcf0-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2bcf0-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="2bcf0-109">PSLoadBalancingSetting objektum létrehozása a bejárati ajtó létrehozása céljából</span><span class="sxs-lookup"><span data-stu-id="2bcf0-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="2bcf0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2bcf0-110">PARAMETERS</span></span>

### <span data-ttu-id="2bcf0-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="2bcf0-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="2bcf0-112">A Szondák további késése ezredmásodpercben a legalacsonyabb késésű gyűjtőben.</span><span class="sxs-lookup"><span data-stu-id="2bcf0-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="2bcf0-113">Az alapértelmezett érték 0</span><span class="sxs-lookup"><span data-stu-id="2bcf0-113">Default value is 0</span></span>

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

### <span data-ttu-id="2bcf0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bcf0-114">-DefaultProfile</span></span>
<span data-ttu-id="2bcf0-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2bcf0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bcf0-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2bcf0-116">-Name</span></span>
<span data-ttu-id="2bcf0-117">az állapot-szonda beállítás neve.</span><span class="sxs-lookup"><span data-stu-id="2bcf0-117">health probe setting name.</span></span>

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

### <span data-ttu-id="2bcf0-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="2bcf0-118">-SampleSize</span></span>
<span data-ttu-id="2bcf0-119">A terheléselosztási döntésekhez figyelembe vett minták száma.</span><span class="sxs-lookup"><span data-stu-id="2bcf0-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="2bcf0-120">Az alapértelmezett érték 4</span><span class="sxs-lookup"><span data-stu-id="2bcf0-120">Default value is 4</span></span>

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

### <span data-ttu-id="2bcf0-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="2bcf0-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="2bcf0-122">A minta időszakra eső minták száma, amelyeknek az alapértelmezett értéknek kell lennie 2</span><span class="sxs-lookup"><span data-stu-id="2bcf0-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="2bcf0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bcf0-123">CommonParameters</span></span>
<span data-ttu-id="2bcf0-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2bcf0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bcf0-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bcf0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bcf0-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bcf0-126">INPUTS</span></span>

### <span data-ttu-id="2bcf0-127">Nincs</span><span class="sxs-lookup"><span data-stu-id="2bcf0-127">None</span></span>

## <span data-ttu-id="2bcf0-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2bcf0-128">OUTPUTS</span></span>

### <span data-ttu-id="2bcf0-129">Microsoft. Azure. Command. FrontDoor. models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="2bcf0-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="2bcf0-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2bcf0-130">NOTES</span></span>

## <span data-ttu-id="2bcf0-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2bcf0-131">RELATED LINKS</span></span>

<span data-ttu-id="2bcf0-132">[Új – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="2bcf0-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
