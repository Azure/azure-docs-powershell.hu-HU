---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b6c703b1c3373e4e0f1347d9bb2a9819ac1e5de6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497204"
---
# <span data-ttu-id="e3ec6-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e3ec6-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="e3ec6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e3ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ec6-103">Adatfolyam-elemzési feladat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e3ec6-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3ec6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e3ec6-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3ec6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e3ec6-105">DESCRIPTION</span></span>
<span data-ttu-id="e3ec6-106">A **Remove-AzureRmStreamAnalyticsJob** parancsmag aszinkron módon töröl egy adott adatfolyam-elemzési feladatot az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="e3ec6-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="e3ec6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e3ec6-107">EXAMPLES</span></span>

### <span data-ttu-id="e3ec6-108">1. példa: feladat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e3ec6-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="e3ec6-109">Ez a parancs eltávolítja a projekt StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="e3ec6-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="e3ec6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e3ec6-110">PARAMETERS</span></span>

### <span data-ttu-id="e3ec6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ec6-111">-DefaultProfile</span></span>
<span data-ttu-id="e3ec6-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e3ec6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3ec6-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e3ec6-113">-Name</span></span>
<span data-ttu-id="e3ec6-114">Megadja az eltávolítandó Azure stream Analytics-feladat nevét.</span><span class="sxs-lookup"><span data-stu-id="e3ec6-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="e3ec6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ec6-115">-ResourceGroupName</span></span>
<span data-ttu-id="e3ec6-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="e3ec6-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="e3ec6-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e3ec6-117">-Confirm</span></span>
<span data-ttu-id="e3ec6-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e3ec6-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ec6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3ec6-119">-WhatIf</span></span>
<span data-ttu-id="e3ec6-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e3ec6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3ec6-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e3ec6-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3ec6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ec6-122">CommonParameters</span></span>
<span data-ttu-id="e3ec6-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e3ec6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ec6-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3ec6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ec6-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3ec6-125">INPUTS</span></span>

### <span data-ttu-id="e3ec6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e3ec6-126">System.String</span></span>

## <span data-ttu-id="e3ec6-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e3ec6-127">OUTPUTS</span></span>

### <span data-ttu-id="e3ec6-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3ec6-128">System.Boolean</span></span>

## <span data-ttu-id="e3ec6-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e3ec6-129">NOTES</span></span>

## <span data-ttu-id="e3ec6-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e3ec6-130">RELATED LINKS</span></span>

[<span data-ttu-id="e3ec6-131">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e3ec6-131">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e3ec6-132">Új – AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e3ec6-132">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e3ec6-133">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e3ec6-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="e3ec6-134">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="e3ec6-134">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


