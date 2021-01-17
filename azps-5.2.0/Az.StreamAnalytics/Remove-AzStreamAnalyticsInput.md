---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366294"
---
# <span data-ttu-id="b4565-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b4565-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="b4565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4565-102">SYNOPSIS</span></span>
<span data-ttu-id="b4565-103">Adatbevitel törlése egy Stream Analytics-feladatból.</span><span class="sxs-lookup"><span data-stu-id="b4565-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="b4565-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b4565-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4565-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b4565-105">DESCRIPTION</span></span>
<span data-ttu-id="b4565-106">A **Remove-AzStreamAnalyticsInput** parancsmag aszinkron módon töröl egy bemenetet az Azure Stream Analytics-feladatából.</span><span class="sxs-lookup"><span data-stu-id="b4565-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="b4565-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b4565-107">EXAMPLES</span></span>

### <span data-ttu-id="b4565-108">1. PÉLDA: Bemeneti adatfolyam eltávolítása egy feladatból</span><span class="sxs-lookup"><span data-stu-id="b4565-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="b4565-109">Ez a parancs eltávolítja a bemeneti EventStreamet a StreamingStreamből.</span><span class="sxs-lookup"><span data-stu-id="b4565-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="b4565-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4565-110">PARAMETERS</span></span>

### <span data-ttu-id="b4565-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4565-111">-DefaultProfile</span></span>
<span data-ttu-id="b4565-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b4565-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4565-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="b4565-113">-JobName</span></span>
<span data-ttu-id="b4565-114">Annak az Azure Stream Analytics-feladatnak a nevét adja meg, amelyhez az Azure Stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="b4565-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="b4565-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b4565-115">-Name</span></span>
<span data-ttu-id="b4565-116">Az eltávolítható Azure Stream Analytics-bemenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b4565-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="b4565-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4565-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4565-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az Azure Stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="b4565-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="b4565-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4565-119">-Confirm</span></span>
<span data-ttu-id="b4565-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="b4565-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4565-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4565-121">-WhatIf</span></span>
<span data-ttu-id="b4565-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="b4565-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4565-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="b4565-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4565-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4565-124">CommonParameters</span></span>
<span data-ttu-id="b4565-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4565-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4565-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4565-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4565-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4565-127">INPUTS</span></span>

### <span data-ttu-id="b4565-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b4565-128">System.String</span></span>

## <span data-ttu-id="b4565-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b4565-129">OUTPUTS</span></span>

### <span data-ttu-id="b4565-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4565-130">System.Boolean</span></span>

## <span data-ttu-id="b4565-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b4565-131">NOTES</span></span>

## <span data-ttu-id="b4565-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b4565-132">RELATED LINKS</span></span>

[<span data-ttu-id="b4565-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b4565-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="b4565-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b4565-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="b4565-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="b4565-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


