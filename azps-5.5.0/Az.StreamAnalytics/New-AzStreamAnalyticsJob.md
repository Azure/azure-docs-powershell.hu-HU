---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: ed5b11684fdb8701343c9390962e95942f4075e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100150210"
---
# <span data-ttu-id="32fc9-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="32fc9-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="32fc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="32fc9-103">Létrehozza vagy frissíti a Stream Analytics feladatot.</span><span class="sxs-lookup"><span data-stu-id="32fc9-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="32fc9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="32fc9-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32fc9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="32fc9-105">DESCRIPTION</span></span>
<span data-ttu-id="32fc9-106">A **New-AzStreamAnalytics Job** parancsmag létrehoz egy új Stream Analytics-feladatot az Azure-ban, vagy frissíti egy meglévő megadott feladat definícióját.</span><span class="sxs-lookup"><span data-stu-id="32fc9-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="32fc9-107">A feladat nevét meg lehet adni a . JSON-fájlban vagy a parancssorban.</span><span class="sxs-lookup"><span data-stu-id="32fc9-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="32fc9-108">Ha mindkettő meg van adva, a parancssorban található névnek meg kell egyeznie a fájlban található névvel.</span><span class="sxs-lookup"><span data-stu-id="32fc9-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="32fc9-109">Ha olyan feladatnevet ad meg, amely már létezik, és nem adja meg a *Force* paramétert, a parancsmag megkérdezi, hogy lecseréli-e a meglévő feladatot.</span><span class="sxs-lookup"><span data-stu-id="32fc9-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="32fc9-110">Ha megadja az *Kényszerítés* paramétert, és megad egy meglévő feladatnevet, a program megerősítés nélkül lecseréli a feladatdefiníciót.</span><span class="sxs-lookup"><span data-stu-id="32fc9-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="32fc9-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="32fc9-111">EXAMPLES</span></span>

### <span data-ttu-id="32fc9-112">1. PÉLDA: Feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="32fc9-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="32fc9-113">Ez a parancs létrehoz egy feladatot a "BeJobDefinition.jsdefinícióból.</span><span class="sxs-lookup"><span data-stu-id="32fc9-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="32fc9-114">Ha a feladatdefiníciós fájlban megadott nevű meglévő feladat már definiálva van, a parancsmag megkérdezi, hogy lecseréli-e azt.</span><span class="sxs-lookup"><span data-stu-id="32fc9-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="32fc9-115">2. PÉLDA: Feladatdefiníció cseréje</span><span class="sxs-lookup"><span data-stu-id="32fc9-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="32fc9-116">Ez a parancs jóváhagyás nélkül lecseréli a Streaming Streaming Streaming feladatdefinícióját.</span><span class="sxs-lookup"><span data-stu-id="32fc9-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="32fc9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32fc9-117">PARAMETERS</span></span>

### <span data-ttu-id="32fc9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32fc9-118">-DefaultProfile</span></span>
<span data-ttu-id="32fc9-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="32fc9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32fc9-120">-File</span><span class="sxs-lookup"><span data-stu-id="32fc9-120">-File</span></span>
<span data-ttu-id="32fc9-121">A létrehozni kívánt Azure Stream Analytics-feladat JSON-ábrázolását tartalmazó JSON-fájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="32fc9-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32fc9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="32fc9-122">-Force</span></span>
<span data-ttu-id="32fc9-123">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="32fc9-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32fc9-124">-Name</span><span class="sxs-lookup"><span data-stu-id="32fc9-124">-Name</span></span>
<span data-ttu-id="32fc9-125">A létrehozni szükséges Azure Stream Analytics-feladat neve.</span><span class="sxs-lookup"><span data-stu-id="32fc9-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32fc9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32fc9-126">-ResourceGroupName</span></span>
<span data-ttu-id="32fc9-127">Annak az erőforráscsoportnak a neve, amelyhez az Azure Stream Analytics-feladatnak tartozni kell.</span><span class="sxs-lookup"><span data-stu-id="32fc9-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="32fc9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32fc9-128">-Confirm</span></span>
<span data-ttu-id="32fc9-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="32fc9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32fc9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32fc9-130">-WhatIf</span></span>
<span data-ttu-id="32fc9-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="32fc9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32fc9-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="32fc9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32fc9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32fc9-133">CommonParameters</span></span>
<span data-ttu-id="32fc9-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32fc9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32fc9-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32fc9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32fc9-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="32fc9-136">INPUTS</span></span>

### <span data-ttu-id="32fc9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="32fc9-137">System.String</span></span>

## <span data-ttu-id="32fc9-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="32fc9-138">OUTPUTS</span></span>

### <span data-ttu-id="32fc9-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="32fc9-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="32fc9-140">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="32fc9-140">NOTES</span></span>

## <span data-ttu-id="32fc9-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="32fc9-141">RELATED LINKS</span></span>

[<span data-ttu-id="32fc9-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="32fc9-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="32fc9-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="32fc9-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="32fc9-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="32fc9-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="32fc9-145">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="32fc9-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="32fc9-146">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="32fc9-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


