---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 3b34a60fa2b85f18a5bee10e0e1f66a4ab102c7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93670952"
---
# <span data-ttu-id="376e7-101">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="376e7-101">Get-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="376e7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="376e7-102">SYNOPSIS</span></span>
<span data-ttu-id="376e7-103">Az DevTest Labs-ban egy laboratórium automatikus leállítási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="376e7-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="376e7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="376e7-104">SYNTAX</span></span>

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="376e7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="376e7-105">DESCRIPTION</span></span>
<span data-ttu-id="376e7-106">A **Get-AzDtlAutoShutdownPolicy** parancsmag egy Lab automatikus leállítási házirendjét kapja meg, amely lehetővé teszi, hogy az összes virtuális gépet automatikusan kikapcsolja egy tesztkörnyezetben a nap adott időpontjában.</span><span class="sxs-lookup"><span data-stu-id="376e7-106">The **Get-AzDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="376e7-107">A parancsmag azt adja eredményül, hogy engedélyezve van-e a házirend állapota, és a nap, amikor beállította, hogy automatikusan leállítsa a laboratóriumi virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="376e7-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="376e7-108">Példák</span><span class="sxs-lookup"><span data-stu-id="376e7-108">EXAMPLES</span></span>

## <span data-ttu-id="376e7-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="376e7-109">PARAMETERS</span></span>

### <span data-ttu-id="376e7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376e7-110">-DefaultProfile</span></span>
<span data-ttu-id="376e7-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="376e7-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="376e7-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="376e7-112">-LabName</span></span>
<span data-ttu-id="376e7-113">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag az automatikus leállítási házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="376e7-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376e7-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="376e7-114">-ResourceGroupName</span></span>
<span data-ttu-id="376e7-115">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="376e7-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="376e7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376e7-116">CommonParameters</span></span>
<span data-ttu-id="376e7-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="376e7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376e7-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="376e7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376e7-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="376e7-119">INPUTS</span></span>

### <span data-ttu-id="376e7-120">System. String</span><span class="sxs-lookup"><span data-stu-id="376e7-120">System.String</span></span>

## <span data-ttu-id="376e7-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="376e7-121">OUTPUTS</span></span>

### <span data-ttu-id="376e7-122">Microsoft. Azure. Command. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="376e7-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="376e7-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="376e7-123">NOTES</span></span>

## <span data-ttu-id="376e7-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="376e7-124">RELATED LINKS</span></span>

[<span data-ttu-id="376e7-125">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="376e7-125">Set-AzDtlAutoShutdownPolicy</span></span>](./Set-AzDtlAutoShutdownPolicy.md)


