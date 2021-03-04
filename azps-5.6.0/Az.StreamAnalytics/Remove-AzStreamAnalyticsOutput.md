---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 950d761324f0750f2433b0b88edb5d37859945e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934625"
---
# <span data-ttu-id="a8613-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a8613-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="a8613-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8613-102">SYNOPSIS</span></span>
<span data-ttu-id="a8613-103">Egy Stream Analytics-feladat kimenetének törlése.</span><span class="sxs-lookup"><span data-stu-id="a8613-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="a8613-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a8613-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8613-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a8613-105">DESCRIPTION</span></span>
<span data-ttu-id="a8613-106">A **Remove-AzStreamAnalyticsOutput** parancsmag aszinkron módon töröl egy kimenetet az Azure Stream Analytics-feladatából.</span><span class="sxs-lookup"><span data-stu-id="a8613-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="a8613-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a8613-107">EXAMPLES</span></span>

### <span data-ttu-id="a8613-108">1. PÉLDA: Kimenet eltávolítása egy feladatból</span><span class="sxs-lookup"><span data-stu-id="a8613-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="a8613-109">Ez a parancs eltávolítja a kimenetet a Streaming Streaming Job feladatból.</span><span class="sxs-lookup"><span data-stu-id="a8613-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="a8613-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8613-110">PARAMETERS</span></span>

### <span data-ttu-id="a8613-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8613-111">-DefaultProfile</span></span>
<span data-ttu-id="a8613-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a8613-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8613-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="a8613-113">-JobName</span></span>
<span data-ttu-id="a8613-114">Annak az Azure Stream Analytics-feladatnak a neve, amelyhez az Azure Stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="a8613-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="a8613-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a8613-115">-Name</span></span>
<span data-ttu-id="a8613-116">Az eltávolítható Azure Stream Analytics-kimenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a8613-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8613-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8613-117">-ResourceGroupName</span></span>
<span data-ttu-id="a8613-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az Azure Stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="a8613-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="a8613-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8613-119">-Confirm</span></span>
<span data-ttu-id="a8613-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a8613-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8613-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8613-121">-WhatIf</span></span>
<span data-ttu-id="a8613-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a8613-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8613-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a8613-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8613-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8613-124">CommonParameters</span></span>
<span data-ttu-id="a8613-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8613-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8613-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8613-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8613-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8613-127">INPUTS</span></span>

### <span data-ttu-id="a8613-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a8613-128">System.String</span></span>

## <span data-ttu-id="a8613-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a8613-129">OUTPUTS</span></span>

### <span data-ttu-id="a8613-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a8613-130">System.Boolean</span></span>

## <span data-ttu-id="a8613-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a8613-131">NOTES</span></span>

## <span data-ttu-id="a8613-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a8613-132">RELATED LINKS</span></span>

[<span data-ttu-id="a8613-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a8613-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="a8613-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a8613-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="a8613-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="a8613-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


