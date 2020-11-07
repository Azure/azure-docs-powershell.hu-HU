---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: 50d0345fea26d233147ad8373ab3daae785d6715
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679450"
---
# <span data-ttu-id="a6536-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="a6536-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="a6536-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a6536-102">SYNOPSIS</span></span>
<span data-ttu-id="a6536-103">A DevTest Labs automatikus indítási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a6536-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6536-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a6536-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6536-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a6536-105">DESCRIPTION</span></span>
<span data-ttu-id="a6536-106">A **Get-AzureRmDtlAutoStartPolicy** parancsmag egy olyan Lab automatikus kezdési házirendjét kapja meg, amely a laboratóriumi virtuális gépeket ütemezi automatikus indításra.</span><span class="sxs-lookup"><span data-stu-id="a6536-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="a6536-107">A parancsmag az engedélyezett vagy letiltott állapotot adja meg, valamint a hét napjait és a nap azon időpontját, amelyet beállított, hogy az automatikus indításhoz az Lab virtuális gépeket ütemezni lehessen.</span><span class="sxs-lookup"><span data-stu-id="a6536-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="a6536-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a6536-108">EXAMPLES</span></span>

## <span data-ttu-id="a6536-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a6536-109">PARAMETERS</span></span>

### <span data-ttu-id="a6536-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="a6536-110">-LabName</span></span>
<span data-ttu-id="a6536-111">Annak a laboratóriumnak a neve, amelyhez ez a parancsmag az automatikus kezdési házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="a6536-111">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="a6536-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6536-112">-ResourceGroupName</span></span>
<span data-ttu-id="a6536-113">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="a6536-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a6536-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6536-114">-DefaultProfile</span></span>
<span data-ttu-id="a6536-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a6536-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6536-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6536-116">CommonParameters</span></span>
<span data-ttu-id="a6536-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a6536-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6536-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6536-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6536-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6536-119">INPUTS</span></span>

## <span data-ttu-id="a6536-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a6536-120">OUTPUTS</span></span>

### <span data-ttu-id="a6536-121">Microsoft. Azure. Command. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="a6536-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="a6536-122">Ez a parancsmag azt az ütemtervet adja eredményül, amely meghatározza, hogy mikor kell elindítani a laboratórium virtuális számítógépeit.</span><span class="sxs-lookup"><span data-stu-id="a6536-122">This cmdlet returns the schedule that specifies when the lab's virtual machines must be started.</span></span>

## <span data-ttu-id="a6536-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a6536-123">NOTES</span></span>

## <span data-ttu-id="a6536-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a6536-124">RELATED LINKS</span></span>

[<span data-ttu-id="a6536-125">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="a6536-125">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)


