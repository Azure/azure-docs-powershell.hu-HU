---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b0e32d58d416fce869995595c3e2a2ff69e8f349
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366308"
---
# <span data-ttu-id="0c7e6-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0c7e6-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="0c7e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7e6-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7e6-103">Létrehozza vagy frissíti a Stream Analytics-feladat kimeneteit.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="0c7e6-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0c7e6-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0c7e6-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0c7e6-105">DESCRIPTION</span></span>
<span data-ttu-id="0c7e6-106">A **New-AzStreamAnalyticsOutput** parancsmag létrehoz egy kimenetet egy Stream Analytics-feladaton belül, vagy frissíti a meglévő kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="0c7e6-107">A kimenet nevét meg lehet adni a . JSON-fájlban vagy a parancssorban.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="0c7e6-108">Ha mindkettő meg van adva, a parancssorban található névnek meg kell egyeznie a fájlban található névvel.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="0c7e6-109">Ha olyan kimenetet ad meg, amely már létezik, és nem adja meg a *Force* paramétert, a parancsmag megkérdezi, hogy lecseréli-e a meglévő kimenetet.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="0c7e6-110">Ha megadja az *Kényszerítés* paramétert, és megad egy meglévő kimeneti nevet, a kimenetet megerősítés nélkül cseréli le a rendszer.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="0c7e6-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0c7e6-111">EXAMPLES</span></span>

### <span data-ttu-id="0c7e6-112">1. példa: Kimenet hozzáadása egy feladathoz</span><span class="sxs-lookup"><span data-stu-id="0c7e6-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="0c7e6-113">Ez a parancs létrehoz egy Kimenet nevű új kimenetet a Streaming Streaming Nevű feladatban.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="0c7e6-114">Ha már definiált egy ilyen nevű kimenetet, a parancsmag megkérdezi, hogy lecseréli-e azt.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="0c7e6-115">2. példa: Feladatkimeneti definíció cseréje</span><span class="sxs-lookup"><span data-stu-id="0c7e6-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="0c7e6-116">Ez a parancs jóváhagyás nélkül lecseréli a Streaming Streaming Streaming nevű feladat kimenetének definícióját.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="0c7e6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c7e6-117">PARAMETERS</span></span>

### <span data-ttu-id="0c7e6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7e6-118">-DefaultProfile</span></span>
<span data-ttu-id="0c7e6-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c7e6-120">-File</span><span class="sxs-lookup"><span data-stu-id="0c7e6-120">-File</span></span>
<span data-ttu-id="0c7e6-121">Egy JSON-fájl elérési útját adja meg, amely tartalmazza a létrehozni kívánt Azure Stream Analytics kimenet JSON-ábrázolásait.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="0c7e6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0c7e6-122">-Force</span></span>
<span data-ttu-id="0c7e6-123">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c7e6-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="0c7e6-124">-JobName</span></span>
<span data-ttu-id="0c7e6-125">Megadja annak az Azure Stream Analytics-feladatnak a nevét, amely alatt létre kell hoznia az Azure Stream Analytics kimenetét.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="0c7e6-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0c7e6-126">-Name</span></span>
<span data-ttu-id="0c7e6-127">A létrehozni szükséges Azure Stream Analytics-kimenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="0c7e6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c7e6-128">-ResourceGroupName</span></span>
<span data-ttu-id="0c7e6-129">Megadja annak az erőforráscsoportnak a nevét, amely alatt létre kell hoznia az Azure Stream Analytics kimenetét.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="0c7e6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c7e6-130">-Confirm</span></span>
<span data-ttu-id="0c7e6-131">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c7e6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c7e6-132">-WhatIf</span></span>
<span data-ttu-id="0c7e6-133">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c7e6-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c7e6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7e6-135">CommonParameters</span></span>
<span data-ttu-id="0c7e6-136">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c7e6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7e6-137">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c7e6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7e6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c7e6-138">INPUTS</span></span>

### <span data-ttu-id="0c7e6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0c7e6-139">System.String</span></span>

## <span data-ttu-id="0c7e6-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c7e6-140">OUTPUTS</span></span>

### <span data-ttu-id="0c7e6-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="0c7e6-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="0c7e6-142">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0c7e6-142">NOTES</span></span>

## <span data-ttu-id="0c7e6-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c7e6-143">RELATED LINKS</span></span>

[<span data-ttu-id="0c7e6-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0c7e6-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="0c7e6-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0c7e6-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="0c7e6-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="0c7e6-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


