---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 2ad9574cbd50c4100dbda7b35a64e557b195898a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012363"
---
# <span data-ttu-id="b2861-101">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="b2861-101">Get-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="b2861-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b2861-102">SYNOPSIS</span></span>
<span data-ttu-id="b2861-103">Az DevTest Labs-ban egy laboratórium automatikus leállítási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b2861-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="b2861-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b2861-104">SYNTAX</span></span>

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2861-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b2861-105">DESCRIPTION</span></span>
<span data-ttu-id="b2861-106">A **Get-AzDtlAutoShutdownPolicy** parancsmag egy Lab automatikus leállítási házirendjét kapja meg, amely lehetővé teszi, hogy az összes virtuális gépet automatikusan kikapcsolja egy tesztkörnyezetben a nap adott időpontjában.</span><span class="sxs-lookup"><span data-stu-id="b2861-106">The **Get-AzDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="b2861-107">A parancsmag azt adja eredményül, hogy engedélyezve van-e a házirend állapota, és a nap, amikor beállította, hogy automatikusan leállítsa a laboratóriumi virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="b2861-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="b2861-108">Példák</span><span class="sxs-lookup"><span data-stu-id="b2861-108">EXAMPLES</span></span>

## <span data-ttu-id="b2861-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b2861-109">PARAMETERS</span></span>

### <span data-ttu-id="b2861-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2861-110">-DefaultProfile</span></span>
<span data-ttu-id="b2861-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b2861-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2861-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="b2861-112">-LabName</span></span>
<span data-ttu-id="b2861-113">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag az automatikus leállítási házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="b2861-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="b2861-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2861-114">-ResourceGroupName</span></span>
<span data-ttu-id="b2861-115">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="b2861-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="b2861-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2861-116">CommonParameters</span></span>
<span data-ttu-id="b2861-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b2861-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2861-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2861-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2861-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2861-119">INPUTS</span></span>

### <span data-ttu-id="b2861-120">System. String</span><span class="sxs-lookup"><span data-stu-id="b2861-120">System.String</span></span>

## <span data-ttu-id="b2861-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b2861-121">OUTPUTS</span></span>

### <span data-ttu-id="b2861-122">Microsoft. Azure. Command. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="b2861-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="b2861-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b2861-123">NOTES</span></span>

## <span data-ttu-id="b2861-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b2861-124">RELATED LINKS</span></span>

[<span data-ttu-id="b2861-125">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="b2861-125">Set-AzDtlAutoShutdownPolicy</span></span>](./Set-AzDtlAutoShutdownPolicy.md)


