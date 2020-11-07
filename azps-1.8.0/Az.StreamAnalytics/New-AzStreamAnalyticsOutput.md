---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 1669d30081ab0ec99579228efbf26d8c76207865
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668446"
---
# <span data-ttu-id="2c67a-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="2c67a-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="2c67a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2c67a-102">SYNOPSIS</span></span>
<span data-ttu-id="2c67a-103">Kimeneteket hoz létre vagy frissít egy adatfolyam-elemzési feladathoz.</span><span class="sxs-lookup"><span data-stu-id="2c67a-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="2c67a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2c67a-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c67a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2c67a-105">DESCRIPTION</span></span>
<span data-ttu-id="2c67a-106">A **New-AzStreamAnalyticsOutput** parancsmag kimenetet hoz létre egy adatfolyam-elemzési munkafolyamaton belül, vagy egy meglévő kimenetet frissít.</span><span class="sxs-lookup"><span data-stu-id="2c67a-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="2c67a-107">A kimenet neve megadható a mezőben. JSON-fájl vagy a parancssorban.</span><span class="sxs-lookup"><span data-stu-id="2c67a-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="2c67a-108">Ha a két érték van megadva, a parancssorban lévő név egyeznie kell a fájl nevével.</span><span class="sxs-lookup"><span data-stu-id="2c67a-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="2c67a-109">Ha olyan kimenetet ad meg, amely már létezik, és nem adja meg az *erő* paramétert, a parancsmag azt fogja megkérdezni, hogy a meglévő kimenetet szeretné-e cserélni.</span><span class="sxs-lookup"><span data-stu-id="2c67a-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="2c67a-110">Ha megadja az *erő* paramétert, és egy meglévő kimeneti nevet ad meg, a program megerősítés nélkül lecseréli a kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2c67a-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="2c67a-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2c67a-111">EXAMPLES</span></span>

### <span data-ttu-id="2c67a-112">1. példa: kimenet hozzáadása a projekthez</span><span class="sxs-lookup"><span data-stu-id="2c67a-112">EXAMPLE 1: Add an output to a job</span></span>
```
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="2c67a-113">Ezzel a paranccsal létrehoz egy új kimenet nevű kimenetet a StreamingJob nevű feladatba.</span><span class="sxs-lookup"><span data-stu-id="2c67a-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="2c67a-114">Ha már meg van határozva egy meglévő kimenet, akkor a parancsmag azt fogja megkérdezni, hogy lecseréli-e.</span><span class="sxs-lookup"><span data-stu-id="2c67a-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="2c67a-115">2. példa: a projekt kimeneti definíciójának cseréje</span><span class="sxs-lookup"><span data-stu-id="2c67a-115">EXAMPLE 2: Replace a job output definition</span></span>
```
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="2c67a-116">A parancs felülírja a StreamingJob nevű feladat kimenetének definícióját megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="2c67a-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="2c67a-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2c67a-117">PARAMETERS</span></span>

### <span data-ttu-id="2c67a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c67a-118">-DefaultProfile</span></span>
<span data-ttu-id="2c67a-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c67a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c67a-120">-Fájl</span><span class="sxs-lookup"><span data-stu-id="2c67a-120">-File</span></span>
<span data-ttu-id="2c67a-121">Annak a JSON-fájlnak az elérési útját adja meg, amely az Azure stream Analytics kimenetének JSON-ábrázolását tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="2c67a-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="2c67a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2c67a-122">-Force</span></span>
<span data-ttu-id="2c67a-123">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="2c67a-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c67a-124">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="2c67a-124">-JobName</span></span>
<span data-ttu-id="2c67a-125">Annak az Azure stream Analytics-feladatnak a nevét adja meg, amely alatt az Azure stream Analytics kimenete hozható létre.</span><span class="sxs-lookup"><span data-stu-id="2c67a-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="2c67a-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2c67a-126">-Name</span></span>
<span data-ttu-id="2c67a-127">A létrehozandó Azure stream Analytics-kimenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c67a-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="2c67a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c67a-128">-ResourceGroupName</span></span>
<span data-ttu-id="2c67a-129">Annak az erőforráscsoport-csoportnak a nevét adja meg, amely alatt létrehozhatja az Azure stream Analytics kimenetét.</span><span class="sxs-lookup"><span data-stu-id="2c67a-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="2c67a-130">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2c67a-130">-Confirm</span></span>
<span data-ttu-id="2c67a-131">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2c67a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c67a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c67a-132">-WhatIf</span></span>
<span data-ttu-id="2c67a-133">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2c67a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c67a-134">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c67a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c67a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c67a-135">CommonParameters</span></span>
<span data-ttu-id="2c67a-136">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2c67a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c67a-137">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c67a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c67a-138">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c67a-138">INPUTS</span></span>

### <span data-ttu-id="2c67a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2c67a-139">System.String</span></span>

## <span data-ttu-id="2c67a-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c67a-140">OUTPUTS</span></span>

### <span data-ttu-id="2c67a-141">Microsoft. Azure. Command. StreamAnalytics. models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="2c67a-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="2c67a-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2c67a-142">NOTES</span></span>

## <span data-ttu-id="2c67a-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c67a-143">RELATED LINKS</span></span>

[<span data-ttu-id="2c67a-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="2c67a-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="2c67a-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="2c67a-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="2c67a-146">Teszt-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="2c67a-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


