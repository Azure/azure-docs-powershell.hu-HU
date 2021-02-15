---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 65d0e40fd522d223eed2d0462e5c66beb9e9709a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150163"
---
# <span data-ttu-id="0fa27-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0fa27-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="0fa27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fa27-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa27-103">Eltávolítja a Stream Analytics feladatot.</span><span class="sxs-lookup"><span data-stu-id="0fa27-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="0fa27-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0fa27-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fa27-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0fa27-105">DESCRIPTION</span></span>
<span data-ttu-id="0fa27-106">A **Remove-AzStreamAnalyticsSync** parancsmag aszinkron módon töröl egy adott Stream Analytics-feladatot az Azure-ban.</span><span class="sxs-lookup"><span data-stu-id="0fa27-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="0fa27-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0fa27-107">EXAMPLES</span></span>

### <span data-ttu-id="0fa27-108">1. PÉLDA: Feladat eltávolítása</span><span class="sxs-lookup"><span data-stu-id="0fa27-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="0fa27-109">Ez a parancs eltávolítja a Streaming Streaming Streaming feladatot.</span><span class="sxs-lookup"><span data-stu-id="0fa27-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="0fa27-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fa27-110">PARAMETERS</span></span>

### <span data-ttu-id="0fa27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa27-111">-DefaultProfile</span></span>
<span data-ttu-id="0fa27-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0fa27-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fa27-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0fa27-113">-Name</span></span>
<span data-ttu-id="0fa27-114">Az eltávolítható Azure Stream Analytics-feladat neve.</span><span class="sxs-lookup"><span data-stu-id="0fa27-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="0fa27-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fa27-115">-ResourceGroupName</span></span>
<span data-ttu-id="0fa27-116">Annak az erőforráscsoportnak a neve, amelyhez az Azure Stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="0fa27-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="0fa27-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fa27-117">-Confirm</span></span>
<span data-ttu-id="0fa27-118">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0fa27-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fa27-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fa27-119">-WhatIf</span></span>
<span data-ttu-id="0fa27-120">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0fa27-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fa27-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0fa27-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fa27-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa27-122">CommonParameters</span></span>
<span data-ttu-id="0fa27-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fa27-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa27-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fa27-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa27-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fa27-125">INPUTS</span></span>

### <span data-ttu-id="0fa27-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0fa27-126">System.String</span></span>

## <span data-ttu-id="0fa27-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0fa27-127">OUTPUTS</span></span>

### <span data-ttu-id="0fa27-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0fa27-128">System.Boolean</span></span>

## <span data-ttu-id="0fa27-129">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0fa27-129">NOTES</span></span>

## <span data-ttu-id="0fa27-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0fa27-130">RELATED LINKS</span></span>

[<span data-ttu-id="0fa27-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0fa27-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="0fa27-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0fa27-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="0fa27-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0fa27-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="0fa27-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="0fa27-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


