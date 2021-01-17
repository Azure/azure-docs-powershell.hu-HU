---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384270"
---
# <span data-ttu-id="59b4f-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="59b4f-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="59b4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="59b4f-103">Egy Stream Analytics-feladat kimenetének törlése.</span><span class="sxs-lookup"><span data-stu-id="59b4f-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="59b4f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="59b4f-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59b4f-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="59b4f-105">DESCRIPTION</span></span>
<span data-ttu-id="59b4f-106">A **Remove-AzStreamAnalyticsOutput** parancsmag aszinkron módon töröl egy kimenetet az Azure Stream Analytics-feladatából.</span><span class="sxs-lookup"><span data-stu-id="59b4f-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="59b4f-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="59b4f-107">EXAMPLES</span></span>

### <span data-ttu-id="59b4f-108">1. PÉLDA: Kimenet eltávolítása egy feladatból</span><span class="sxs-lookup"><span data-stu-id="59b4f-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="59b4f-109">Ez a parancs eltávolítja a kimenetet a Streaming Streaming Job feladatból.</span><span class="sxs-lookup"><span data-stu-id="59b4f-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="59b4f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59b4f-110">PARAMETERS</span></span>

### <span data-ttu-id="59b4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b4f-111">-DefaultProfile</span></span>
<span data-ttu-id="59b4f-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59b4f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59b4f-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="59b4f-113">-JobName</span></span>
<span data-ttu-id="59b4f-114">Annak az Azure Stream Analytics-feladatnak a neve, amelyhez az Azure Stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="59b4f-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="59b4f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="59b4f-115">-Name</span></span>
<span data-ttu-id="59b4f-116">Az eltávolítható Azure Stream Analytics-kimenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59b4f-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="59b4f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b4f-117">-ResourceGroupName</span></span>
<span data-ttu-id="59b4f-118">Annak az erőforráscsoportnak a neve, amelyhez az Azure Stream Analytics kimenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="59b4f-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="59b4f-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59b4f-119">-Confirm</span></span>
<span data-ttu-id="59b4f-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="59b4f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59b4f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59b4f-121">-WhatIf</span></span>
<span data-ttu-id="59b4f-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="59b4f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59b4f-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59b4f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59b4f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b4f-124">CommonParameters</span></span>
<span data-ttu-id="59b4f-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b4f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b4f-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b4f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b4f-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59b4f-127">INPUTS</span></span>

### <span data-ttu-id="59b4f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="59b4f-128">System.String</span></span>

## <span data-ttu-id="59b4f-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59b4f-129">OUTPUTS</span></span>

### <span data-ttu-id="59b4f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="59b4f-130">System.Boolean</span></span>

## <span data-ttu-id="59b4f-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="59b4f-131">NOTES</span></span>

## <span data-ttu-id="59b4f-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59b4f-132">RELATED LINKS</span></span>

[<span data-ttu-id="59b4f-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="59b4f-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="59b4f-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="59b4f-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="59b4f-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="59b4f-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


