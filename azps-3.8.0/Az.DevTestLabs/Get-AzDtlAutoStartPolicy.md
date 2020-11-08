---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 8b2269b46a120d34e696b2ee160aabceb0cba66c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012360"
---
# <span data-ttu-id="bdd3a-101">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="bdd3a-101">Get-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="bdd3a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bdd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd3a-103">A DevTest Labs automatikus indítási házirendjét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="bdd3a-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="bdd3a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bdd3a-104">SYNTAX</span></span>

```
Get-AzDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdd3a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bdd3a-105">DESCRIPTION</span></span>
<span data-ttu-id="bdd3a-106">A **Get-AzDtlAutoStartPolicy** parancsmag egy olyan Lab automatikus kezdési házirendjét kapja meg, amely a laboratóriumi virtuális gépeket ütemezi automatikus indításra.</span><span class="sxs-lookup"><span data-stu-id="bdd3a-106">The **Get-AzDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="bdd3a-107">A parancsmag az engedélyezett vagy letiltott állapotot adja meg, valamint a hét napjait és a nap azon időpontját, amelyet beállított, hogy az automatikus indításhoz az Lab virtuális gépeket ütemezni lehessen.</span><span class="sxs-lookup"><span data-stu-id="bdd3a-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="bdd3a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bdd3a-108">EXAMPLES</span></span>

## <span data-ttu-id="bdd3a-109">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bdd3a-109">PARAMETERS</span></span>

### <span data-ttu-id="bdd3a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd3a-110">-DefaultProfile</span></span>
<span data-ttu-id="bdd3a-111">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bdd3a-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdd3a-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="bdd3a-112">-LabName</span></span>
<span data-ttu-id="bdd3a-113">Annak a laboratóriumnak a neve, amelyhez ez a parancsmag az automatikus kezdési házirendet kapja.</span><span class="sxs-lookup"><span data-stu-id="bdd3a-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="bdd3a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd3a-114">-ResourceGroupName</span></span>
<span data-ttu-id="bdd3a-115">Annak a csoportnak a neve, amelyhez a labor tartozik.</span><span class="sxs-lookup"><span data-stu-id="bdd3a-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="bdd3a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd3a-116">CommonParameters</span></span>
<span data-ttu-id="bdd3a-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bdd3a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd3a-118">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd3a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd3a-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdd3a-119">INPUTS</span></span>

### <span data-ttu-id="bdd3a-120">System. String</span><span class="sxs-lookup"><span data-stu-id="bdd3a-120">System.String</span></span>

## <span data-ttu-id="bdd3a-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bdd3a-121">OUTPUTS</span></span>

### <span data-ttu-id="bdd3a-122">Microsoft. Azure. Command. DevTestLabs. models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="bdd3a-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="bdd3a-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bdd3a-123">NOTES</span></span>

## <span data-ttu-id="bdd3a-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bdd3a-124">RELATED LINKS</span></span>

[<span data-ttu-id="bdd3a-125">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="bdd3a-125">Set-AzDtlAutoStartPolicy</span></span>](./Set-AzDtlAutoStartPolicy.md)


