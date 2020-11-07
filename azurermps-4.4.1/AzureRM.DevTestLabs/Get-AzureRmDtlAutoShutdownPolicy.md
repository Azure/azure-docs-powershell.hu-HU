---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 4717fa187a8bd8234cd786ff5c6ad6d1678696b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679452"
---
# <span data-ttu-id="66a2d-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="66a2d-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="66a2d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="66a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="66a2d-103">Az DevTest Labs-ban egy laboratórium automatikus leállítási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="66a2d-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66a2d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="66a2d-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66a2d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="66a2d-105">DESCRIPTION</span></span>
<span data-ttu-id="66a2d-106">A **Get-AzureRmDtlAutoShutdownPolicy** parancsmag egy Lab automatikus leállítási házirendjét kapja meg, amely lehetővé teszi, hogy az összes virtuális gépet automatikusan kikapcsolja egy tesztkörnyezetben a nap adott időpontjában.</span><span class="sxs-lookup"><span data-stu-id="66a2d-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="66a2d-107">A parancsmag azt adja eredményül, hogy engedélyezve van-e a házirend állapota, és a nap, amikor beállította, hogy automatikusan leállítsa a laboratóriumi virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="66a2d-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="66a2d-108">Példák</span><span class="sxs-lookup"><span data-stu-id="66a2d-108">EXAMPLES</span></span>

## <span data-ttu-id="66a2d-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="66a2d-109">PARAMETERS</span></span>

### <span data-ttu-id="66a2d-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="66a2d-110">-LabName</span></span>
<span data-ttu-id="66a2d-111">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag az automatikus leállítási házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="66a2d-111">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="66a2d-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66a2d-112">-ResourceGroupName</span></span>
<span data-ttu-id="66a2d-113">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="66a2d-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="66a2d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66a2d-114">-DefaultProfile</span></span>
<span data-ttu-id="66a2d-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="66a2d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66a2d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66a2d-116">CommonParameters</span></span>
<span data-ttu-id="66a2d-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="66a2d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66a2d-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66a2d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66a2d-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="66a2d-119">INPUTS</span></span>

## <span data-ttu-id="66a2d-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="66a2d-120">OUTPUTS</span></span>

### <span data-ttu-id="66a2d-121">Microsoft. Azure. Command. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="66a2d-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="66a2d-122">Ez a parancsmag azt az ütemezést adja eredményül, amely meghatározza, hogy a laboratórium virtuális gépei Mikor legyenek lezárva.</span><span class="sxs-lookup"><span data-stu-id="66a2d-122">This cmdlet returns the schedule which specifies when the lab's virtual machines must shut down.</span></span>

## <span data-ttu-id="66a2d-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="66a2d-123">NOTES</span></span>

## <span data-ttu-id="66a2d-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="66a2d-124">RELATED LINKS</span></span>

[<span data-ttu-id="66a2d-125">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="66a2d-125">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


