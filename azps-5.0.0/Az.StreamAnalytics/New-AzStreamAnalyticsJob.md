---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: ed5b11684fdb8701343c9390962e95942f4075e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186611"
---
# <span data-ttu-id="1cb21-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1cb21-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="1cb21-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1cb21-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb21-103">Adatfolyam-elemzési feladatot hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="1cb21-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="1cb21-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1cb21-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cb21-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1cb21-105">DESCRIPTION</span></span>
<span data-ttu-id="1cb21-106">A **New-AzStreamAnalyticsJob** parancsmag létrehoz egy új adatfolyam-elemzési feladatot az Azure-ban, vagy frissíti egy meglévő meghatározott feladat definícióját.</span><span class="sxs-lookup"><span data-stu-id="1cb21-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="1cb21-107">A feladat neve megadható a mezőben. JSON-fájl vagy a parancssorban.</span><span class="sxs-lookup"><span data-stu-id="1cb21-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="1cb21-108">Ha a két érték van megadva, a parancssorban lévő név egyeznie kell a fájl nevével.</span><span class="sxs-lookup"><span data-stu-id="1cb21-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="1cb21-109">Ha olyan feladatot ad meg, amely már létezik, és nem adja meg az *erő* paramétert, a parancsmag azt fogja megkérdezni, hogy a meglévő feladatot lecseréli-e.</span><span class="sxs-lookup"><span data-stu-id="1cb21-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="1cb21-110">Ha megadhatja a *Force* paramétert, és megadhat egy meglévőt, a feladatdefiníció megerősítés nélkül lesz lecserélve.</span><span class="sxs-lookup"><span data-stu-id="1cb21-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="1cb21-111">Példák</span><span class="sxs-lookup"><span data-stu-id="1cb21-111">EXAMPLES</span></span>

### <span data-ttu-id="1cb21-112">Példa 1: feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="1cb21-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="1cb21-113">Ez a parancs létrehoz egy feladatot a definícióban JobDefinition.jsbekapcsolva.</span><span class="sxs-lookup"><span data-stu-id="1cb21-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="1cb21-114">Ha már definiálva van egy meglévő feladat a megadott névvel a Job definition-fájlban, a parancsmag megkérdezi, hogy a program lecseréli-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="1cb21-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="1cb21-115">2. példa: feladatdefiníció cseréje</span><span class="sxs-lookup"><span data-stu-id="1cb21-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="1cb21-116">Ez a parancs megerősítés nélkül lecseréli a StreamingJob a feladatdefiníció fogalmát.</span><span class="sxs-lookup"><span data-stu-id="1cb21-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="1cb21-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1cb21-117">PARAMETERS</span></span>

### <span data-ttu-id="1cb21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb21-118">-DefaultProfile</span></span>
<span data-ttu-id="1cb21-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1cb21-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cb21-120">-Fájl</span><span class="sxs-lookup"><span data-stu-id="1cb21-120">-File</span></span>
<span data-ttu-id="1cb21-121">Annak a JSON-fájlnak az elérési útját adja meg, amely az Azure stream Analytics-feladat által létrehozott JSON-ábrázolást tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1cb21-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="1cb21-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1cb21-122">-Force</span></span>
<span data-ttu-id="1cb21-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1cb21-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1cb21-124">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1cb21-124">-Name</span></span>
<span data-ttu-id="1cb21-125">A létrehozandó Azure stream Analytics-feladat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1cb21-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="1cb21-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb21-126">-ResourceGroupName</span></span>
<span data-ttu-id="1cb21-127">Annak az erőforráscsoport-csoportnak a neve, amelyhez az Azure stream Analytics-feladat tartozik.</span><span class="sxs-lookup"><span data-stu-id="1cb21-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="1cb21-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1cb21-128">-Confirm</span></span>
<span data-ttu-id="1cb21-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1cb21-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cb21-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cb21-130">-WhatIf</span></span>
<span data-ttu-id="1cb21-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1cb21-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cb21-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1cb21-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cb21-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb21-133">CommonParameters</span></span>
<span data-ttu-id="1cb21-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1cb21-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb21-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cb21-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb21-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cb21-136">INPUTS</span></span>

### <span data-ttu-id="1cb21-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1cb21-137">System.String</span></span>

## <span data-ttu-id="1cb21-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1cb21-138">OUTPUTS</span></span>

### <span data-ttu-id="1cb21-139">Microsoft. Azure. Command. StreamAnalytics. models. PSJob</span><span class="sxs-lookup"><span data-stu-id="1cb21-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="1cb21-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1cb21-140">NOTES</span></span>

## <span data-ttu-id="1cb21-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1cb21-141">RELATED LINKS</span></span>

[<span data-ttu-id="1cb21-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1cb21-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="1cb21-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1cb21-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="1cb21-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1cb21-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="1cb21-145">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1cb21-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="1cb21-146">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1cb21-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

