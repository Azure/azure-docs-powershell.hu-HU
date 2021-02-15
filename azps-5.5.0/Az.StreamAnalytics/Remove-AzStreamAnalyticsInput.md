---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150178"
---
# <span data-ttu-id="0e3e3-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0e3e3-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="0e3e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e3e3-102">SYNOPSIS</span></span>
<span data-ttu-id="0e3e3-103">Adatbevitel törlése egy Stream Analytics-feladatból.</span><span class="sxs-lookup"><span data-stu-id="0e3e3-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="0e3e3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0e3e3-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e3e3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0e3e3-105">DESCRIPTION</span></span>
<span data-ttu-id="0e3e3-106">A **Remove-AzStreamAnalyticsInput** parancsmag aszinkron módon töröl egy bemenetet az Azure Stream Analytics-feladatából.</span><span class="sxs-lookup"><span data-stu-id="0e3e3-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="0e3e3-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0e3e3-107">EXAMPLES</span></span>

### <span data-ttu-id="0e3e3-108">1. PÉLDA: Bemeneti adatfolyam eltávolítása egy feladatból</span><span class="sxs-lookup"><span data-stu-id="0e3e3-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="0e3e3-109">Ez a parancs eltávolítja a bemeneti EventStreamet a StreamingStreamből.</span><span class="sxs-lookup"><span data-stu-id="0e3e3-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="0e3e3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e3e3-110">PARAMETERS</span></span>

### <span data-ttu-id="0e3e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e3e3-111">-DefaultProfile</span></span>
<span data-ttu-id="0e3e3-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0e3e3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e3e3-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="0e3e3-113">-JobName</span></span>
<span data-ttu-id="0e3e3-114">Annak az Azure Stream Analytics-feladatnak a neve, amelyhez az Azure Stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="0e3e3-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="0e3e3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0e3e3-115">-Name</span></span>
<span data-ttu-id="0e3e3-116">Az eltávolítható Azure Stream Analytics-bemenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0e3e3-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="0e3e3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e3e3-117">-ResourceGroupName</span></span>
<span data-ttu-id="0e3e3-118">Annak az erőforráscsoportnak a nevét adja meg, amelyhez az Azure Stream Analytics-bemenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="0e3e3-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="0e3e3-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e3e3-119">-Confirm</span></span>
<span data-ttu-id="0e3e3-120">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0e3e3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e3e3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e3e3-121">-WhatIf</span></span>
<span data-ttu-id="0e3e3-122">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0e3e3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e3e3-123">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0e3e3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e3e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e3e3-124">CommonParameters</span></span>
<span data-ttu-id="0e3e3-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e3e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e3e3-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e3e3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e3e3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0e3e3-127">INPUTS</span></span>

### <span data-ttu-id="0e3e3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0e3e3-128">System.String</span></span>

## <span data-ttu-id="0e3e3-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0e3e3-129">OUTPUTS</span></span>

### <span data-ttu-id="0e3e3-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0e3e3-130">System.Boolean</span></span>

## <span data-ttu-id="0e3e3-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0e3e3-131">NOTES</span></span>

## <span data-ttu-id="0e3e3-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0e3e3-132">RELATED LINKS</span></span>

[<span data-ttu-id="0e3e3-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0e3e3-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="0e3e3-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0e3e3-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="0e3e3-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="0e3e3-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


