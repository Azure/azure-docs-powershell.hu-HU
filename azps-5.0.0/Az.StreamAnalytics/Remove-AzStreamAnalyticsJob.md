---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 65d0e40fd522d223eed2d0462e5c66beb9e9709a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186167"
---
# <span data-ttu-id="9a51c-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9a51c-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="9a51c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a51c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a51c-103">Adatfolyam-elemzési feladat eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="9a51c-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="9a51c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a51c-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a51c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a51c-105">DESCRIPTION</span></span>
<span data-ttu-id="9a51c-106">A **Remove-AzStreamAnalyticsJob** parancsmag aszinkron módon töröl egy adott adatfolyam-elemzési feladatot az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="9a51c-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="9a51c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9a51c-107">EXAMPLES</span></span>

### <span data-ttu-id="9a51c-108">1. példa: feladat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="9a51c-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="9a51c-109">Ez a parancs eltávolítja a projekt StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="9a51c-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="9a51c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a51c-110">PARAMETERS</span></span>

### <span data-ttu-id="9a51c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a51c-111">-DefaultProfile</span></span>
<span data-ttu-id="9a51c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a51c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a51c-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a51c-113">-Name</span></span>
<span data-ttu-id="9a51c-114">Megadja az eltávolítandó Azure stream Analytics-feladat nevét.</span><span class="sxs-lookup"><span data-stu-id="9a51c-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="9a51c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a51c-115">-ResourceGroupName</span></span>
<span data-ttu-id="9a51c-116">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="9a51c-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="9a51c-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9a51c-117">-Confirm</span></span>
<span data-ttu-id="9a51c-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9a51c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a51c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a51c-119">-WhatIf</span></span>
<span data-ttu-id="9a51c-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9a51c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a51c-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a51c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a51c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a51c-122">CommonParameters</span></span>
<span data-ttu-id="9a51c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a51c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a51c-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a51c-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a51c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a51c-125">INPUTS</span></span>

### <span data-ttu-id="9a51c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9a51c-126">System.String</span></span>

## <span data-ttu-id="9a51c-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a51c-127">OUTPUTS</span></span>

### <span data-ttu-id="9a51c-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a51c-128">System.Boolean</span></span>

## <span data-ttu-id="9a51c-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a51c-129">NOTES</span></span>

## <span data-ttu-id="9a51c-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a51c-130">RELATED LINKS</span></span>

[<span data-ttu-id="9a51c-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9a51c-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="9a51c-132">Új – AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9a51c-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="9a51c-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9a51c-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="9a51c-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9a51c-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

