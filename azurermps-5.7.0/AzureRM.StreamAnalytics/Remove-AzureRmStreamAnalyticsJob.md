---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 64ebe431333914a907c515744501f4624a7977ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494264"
---
# <span data-ttu-id="002b6-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="002b6-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="002b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="002b6-102">SYNOPSIS</span></span>
<span data-ttu-id="002b6-103">Adatfolyam-elemzési feladat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="002b6-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="002b6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="002b6-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="002b6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="002b6-105">DESCRIPTION</span></span>
<span data-ttu-id="002b6-106">A **Remove-AzureRmStreamAnalyticsJob** parancsmag aszinkron módon töröl egy adott adatfolyam-elemzési feladatot az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="002b6-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="002b6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="002b6-107">EXAMPLES</span></span>

### <span data-ttu-id="002b6-108">1. példa: feladat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="002b6-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="002b6-109">Ez a parancs eltávolítja a projekt StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="002b6-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="002b6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="002b6-110">PARAMETERS</span></span>

### <span data-ttu-id="002b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="002b6-111">-DefaultProfile</span></span>
<span data-ttu-id="002b6-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="002b6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="002b6-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="002b6-113">-Name</span></span>
<span data-ttu-id="002b6-114">Megadja az eltávolítandó Azure stream Analytics-feladat nevét.</span><span class="sxs-lookup"><span data-stu-id="002b6-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="002b6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="002b6-115">-ResourceGroupName</span></span>
<span data-ttu-id="002b6-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="002b6-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="002b6-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="002b6-117">-Confirm</span></span>
<span data-ttu-id="002b6-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="002b6-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="002b6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="002b6-119">-WhatIf</span></span>
<span data-ttu-id="002b6-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="002b6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="002b6-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="002b6-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="002b6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="002b6-122">CommonParameters</span></span>
<span data-ttu-id="002b6-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="002b6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="002b6-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="002b6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="002b6-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="002b6-125">INPUTS</span></span>

### <span data-ttu-id="002b6-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="002b6-126">None</span></span>
<span data-ttu-id="002b6-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="002b6-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="002b6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="002b6-128">OUTPUTS</span></span>

### <span data-ttu-id="002b6-129">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="002b6-129">System.Object</span></span>

## <span data-ttu-id="002b6-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="002b6-130">NOTES</span></span>

## <span data-ttu-id="002b6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="002b6-131">RELATED LINKS</span></span>

[<span data-ttu-id="002b6-132">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="002b6-132">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="002b6-133">Új – AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="002b6-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="002b6-134">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="002b6-134">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="002b6-135">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="002b6-135">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


