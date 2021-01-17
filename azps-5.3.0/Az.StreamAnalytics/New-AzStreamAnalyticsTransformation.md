---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 017c084e98d8983343ae1f8c19464cc254b26e2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384297"
---
# <span data-ttu-id="f77e0-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="f77e0-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="f77e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f77e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f77e0-103">Átalakítást hoz létre vagy frissítéseket végez egy feladaton belül.</span><span class="sxs-lookup"><span data-stu-id="f77e0-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="f77e0-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f77e0-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f77e0-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f77e0-105">DESCRIPTION</span></span>
<span data-ttu-id="f77e0-106">A **New-AzStreamAnalyticsTransformation** parancsmag átalakítást hoz létre egy Stream Analytics-feladaton belül, vagy frissíti a meglévő átalakítást.</span><span class="sxs-lookup"><span data-stu-id="f77e0-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="f77e0-107">Az átalakítás nevét meg lehet adni a . JSON-fájlban vagy a parancssorban.</span><span class="sxs-lookup"><span data-stu-id="f77e0-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="f77e0-108">Ha mindkettő meg van adva, a parancssorban található névnek meg kell egyeznie a fájlban található névvel.</span><span class="sxs-lookup"><span data-stu-id="f77e0-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="f77e0-109">Ha olyan átalakítást ad meg, amely már létezik, és nem adja meg a Force paramétert, a parancsmag megkérdezi, hogy lecseréli-e a meglévő átalakítást.</span><span class="sxs-lookup"><span data-stu-id="f77e0-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="f77e0-110">Ha megadja az *Kényszerítés* paramétert, és megad egy meglévő átalakításnevet, a transzformációt megerősítés nélkül lecseréli a rendszer.</span><span class="sxs-lookup"><span data-stu-id="f77e0-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="f77e0-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f77e0-111">EXAMPLES</span></span>

### <span data-ttu-id="f77e0-112">1. példa: Átalakítás létrehozása vagy cseréje egy feladatban</span><span class="sxs-lookup"><span data-stu-id="f77e0-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="f77e0-113">Ez a parancs létrehoz egy Streaming StreamingTransform nevű átalakítást a Streaming Streaming Streaming nevű feladatban.</span><span class="sxs-lookup"><span data-stu-id="f77e0-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="f77e0-114">Ha egy meglévő átalakítás már definiálva van ezzel a névvel, a parancsmag megkérdezi, hogy lecseréli-e azt.</span><span class="sxs-lookup"><span data-stu-id="f77e0-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="f77e0-115">2. példa: Átalakítás cseréje egy feladatban</span><span class="sxs-lookup"><span data-stu-id="f77e0-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="f77e0-116">Ez a parancs jóváhagyás nélkül lecseréli a StreamingTransform definícióját a Streaming Streaming Streaming feladatban.</span><span class="sxs-lookup"><span data-stu-id="f77e0-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="f77e0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f77e0-117">PARAMETERS</span></span>

### <span data-ttu-id="f77e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f77e0-118">-DefaultProfile</span></span>
<span data-ttu-id="f77e0-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f77e0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f77e0-120">-File</span><span class="sxs-lookup"><span data-stu-id="f77e0-120">-File</span></span>
<span data-ttu-id="f77e0-121">Egy JSON-fájl elérési útját adja meg, amely a létrehozni kívánt Azure Stream Analytics-átalakítás JSON-ábrázolását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f77e0-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f77e0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f77e0-122">-Force</span></span>
<span data-ttu-id="f77e0-123">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="f77e0-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f77e0-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="f77e0-124">-JobName</span></span>
<span data-ttu-id="f77e0-125">Megadja annak az Azure Stream Analytics-feladatnak a nevét, amely alatt létre kell hoznia az Azure Stream Analytics-átalakítást.</span><span class="sxs-lookup"><span data-stu-id="f77e0-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="f77e0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f77e0-126">-Name</span></span>
<span data-ttu-id="f77e0-127">A létrehozni szükséges Azure Stream Analytics-átalakítás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f77e0-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f77e0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f77e0-128">-ResourceGroupName</span></span>
<span data-ttu-id="f77e0-129">Megadja annak az erőforráscsoportnak a nevét, amely alatt létre kell hoznia az Azure Stream Analytics-átalakítást.</span><span class="sxs-lookup"><span data-stu-id="f77e0-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="f77e0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f77e0-130">-Confirm</span></span>
<span data-ttu-id="f77e0-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="f77e0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f77e0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f77e0-132">-WhatIf</span></span>
<span data-ttu-id="f77e0-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="f77e0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f77e0-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f77e0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f77e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f77e0-135">CommonParameters</span></span>
<span data-ttu-id="f77e0-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f77e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f77e0-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f77e0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f77e0-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f77e0-138">INPUTS</span></span>

### <span data-ttu-id="f77e0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f77e0-139">System.String</span></span>

## <span data-ttu-id="f77e0-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f77e0-140">OUTPUTS</span></span>

### <span data-ttu-id="f77e0-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="f77e0-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="f77e0-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f77e0-142">NOTES</span></span>

## <span data-ttu-id="f77e0-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f77e0-143">RELATED LINKS</span></span>

[<span data-ttu-id="f77e0-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="f77e0-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


