---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 557cfcaefef1a85fe7ad0a8bd62f4ddbf0ecb6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494508"
---
# <span data-ttu-id="a05fe-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="a05fe-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="a05fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a05fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a05fe-103">Az DevTest Labs-ban egy laboratórium automatikus leállítási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a05fe-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a05fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a05fe-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a05fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a05fe-105">DESCRIPTION</span></span>
<span data-ttu-id="a05fe-106">A **Get-AzureRmDtlAutoShutdownPolicy** parancsmag egy Lab automatikus leállítási házirendjét kapja meg, amely lehetővé teszi, hogy az összes virtuális gépet automatikusan kikapcsolja egy tesztkörnyezetben a nap adott időpontjában.</span><span class="sxs-lookup"><span data-stu-id="a05fe-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="a05fe-107">A parancsmag azt adja eredményül, hogy engedélyezve van-e a házirend állapota, és a nap, amikor beállította, hogy automatikusan leállítsa a laboratóriumi virtuális gépeket.</span><span class="sxs-lookup"><span data-stu-id="a05fe-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="a05fe-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a05fe-108">EXAMPLES</span></span>

## <span data-ttu-id="a05fe-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a05fe-109">PARAMETERS</span></span>

### <span data-ttu-id="a05fe-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05fe-110">-DefaultProfile</span></span>
<span data-ttu-id="a05fe-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a05fe-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a05fe-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="a05fe-112">-LabName</span></span>
<span data-ttu-id="a05fe-113">Annak a laboratóriumnak a nevét adja meg, amelyhez ez a parancsmag az automatikus leállítási házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="a05fe-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05fe-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05fe-114">-ResourceGroupName</span></span>
<span data-ttu-id="a05fe-115">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="a05fe-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a05fe-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05fe-116">CommonParameters</span></span>
<span data-ttu-id="a05fe-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a05fe-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05fe-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a05fe-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05fe-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a05fe-119">INPUTS</span></span>

### <span data-ttu-id="a05fe-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="a05fe-120">None</span></span>
<span data-ttu-id="a05fe-121">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a05fe-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a05fe-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a05fe-122">OUTPUTS</span></span>

### <span data-ttu-id="a05fe-123">Microsoft. Azure. Command. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="a05fe-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="a05fe-124">Ez a parancsmag azt az ütemezést adja eredményül, amely meghatározza, hogy a laboratórium virtuális gépei Mikor legyenek lezárva.</span><span class="sxs-lookup"><span data-stu-id="a05fe-124">This cmdlet returns the schedule which specifies when the lab's virtual machines must shut down.</span></span>

## <span data-ttu-id="a05fe-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a05fe-125">NOTES</span></span>

## <span data-ttu-id="a05fe-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a05fe-126">RELATED LINKS</span></span>

[<span data-ttu-id="a05fe-127">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="a05fe-127">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


