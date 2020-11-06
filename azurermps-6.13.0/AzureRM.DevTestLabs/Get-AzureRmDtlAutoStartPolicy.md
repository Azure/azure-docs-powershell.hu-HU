---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: efe948e2676b44a70917efb43e901f8848dec0e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495136"
---
# <span data-ttu-id="735bf-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="735bf-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="735bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="735bf-102">SYNOPSIS</span></span>
<span data-ttu-id="735bf-103">A DevTest Labs automatikus indítási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="735bf-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="735bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="735bf-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="735bf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="735bf-105">DESCRIPTION</span></span>
<span data-ttu-id="735bf-106">A **Get-AzureRmDtlAutoStartPolicy** parancsmag egy olyan Lab automatikus kezdési házirendjét kapja meg, amely a laboratóriumi virtuális gépeket ütemezi automatikus indításra.</span><span class="sxs-lookup"><span data-stu-id="735bf-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="735bf-107">A parancsmag az engedélyezett vagy letiltott állapotot adja meg, valamint a hét napjait és a nap azon időpontját, amelyet beállított, hogy az automatikus indításhoz az Lab virtuális gépeket ütemezni lehessen.</span><span class="sxs-lookup"><span data-stu-id="735bf-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="735bf-108">Példák</span><span class="sxs-lookup"><span data-stu-id="735bf-108">EXAMPLES</span></span>

## <span data-ttu-id="735bf-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="735bf-109">PARAMETERS</span></span>

### <span data-ttu-id="735bf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735bf-110">-DefaultProfile</span></span>
<span data-ttu-id="735bf-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="735bf-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="735bf-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="735bf-112">-LabName</span></span>
<span data-ttu-id="735bf-113">Annak a laboratóriumnak a neve, amelyhez ez a parancsmag az automatikus kezdési házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="735bf-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="735bf-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="735bf-114">-ResourceGroupName</span></span>
<span data-ttu-id="735bf-115">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="735bf-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="735bf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735bf-116">CommonParameters</span></span>
<span data-ttu-id="735bf-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="735bf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735bf-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="735bf-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735bf-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="735bf-119">INPUTS</span></span>

### <span data-ttu-id="735bf-120">System. String</span><span class="sxs-lookup"><span data-stu-id="735bf-120">System.String</span></span>

## <span data-ttu-id="735bf-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="735bf-121">OUTPUTS</span></span>

### <span data-ttu-id="735bf-122">Microsoft. Azure. Command. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="735bf-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="735bf-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="735bf-123">NOTES</span></span>

## <span data-ttu-id="735bf-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="735bf-124">RELATED LINKS</span></span>

[<span data-ttu-id="735bf-125">Set-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="735bf-125">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)


