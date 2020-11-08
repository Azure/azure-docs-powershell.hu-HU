---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 74145a6d65fdaa9634d7681133e10b2496b5f903
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94017485"
---
# <span data-ttu-id="3d18d-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3d18d-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="3d18d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d18d-102">SYNOPSIS</span></span>
<span data-ttu-id="3d18d-103">Projekthez tartozó bevitelt hoz létre vagy frissít.</span><span class="sxs-lookup"><span data-stu-id="3d18d-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="3d18d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d18d-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d18d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d18d-105">DESCRIPTION</span></span>
<span data-ttu-id="3d18d-106">A **New-AzStreamAnalyticsInput** parancsmag létrehoz egy bemenetet egy adatfolyam-elemzési munkafolyamaton belül, vagy egy meglévő bemenetet frissít.</span><span class="sxs-lookup"><span data-stu-id="3d18d-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="3d18d-107">A beviteli nevet a JSON-fájlban vagy a parancssorban lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="3d18d-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="3d18d-108">Ha a két érték van megadva, a parancssorban lévő név egyeznie kell a fájl nevével.</span><span class="sxs-lookup"><span data-stu-id="3d18d-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="3d18d-109">Ha olyan bemenetet ad meg, amely már létezik, és nem adja meg az *erő* paramétert, akkor a parancsmag azt fogja megkérdezni, hogy lecseréli-e a meglévő bemenetet.</span><span class="sxs-lookup"><span data-stu-id="3d18d-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="3d18d-110">Ha az *erő* paramétert adja meg, és egy meglévő beviteli nevet ad meg, a program megerősítés nélkül lecseréli a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="3d18d-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="3d18d-111">Példák</span><span class="sxs-lookup"><span data-stu-id="3d18d-111">EXAMPLES</span></span>

### <span data-ttu-id="3d18d-112">1. példa: bevitt munka létrehozása egy definícióval egy fájlból</span><span class="sxs-lookup"><span data-stu-id="3d18d-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="3d18d-113">Ez a parancs a fájl Input.jsbeírását hozza létre.</span><span class="sxs-lookup"><span data-stu-id="3d18d-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="3d18d-114">Ha már definiált egy meglévő bemenetet a szövegbeviteli definíciós fájlban megadott névvel, a parancsmag megkérdezi, hogy a program lecseréli-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="3d18d-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="3d18d-115">2. példa: projekt bemenetének létrehozása</span><span class="sxs-lookup"><span data-stu-id="3d18d-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="3d18d-116">Ezzel a paranccsal új adatokat hozhat létre a EntryStream nevű feladathoz.</span><span class="sxs-lookup"><span data-stu-id="3d18d-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="3d18d-117">Ha már meg van határozva egy meglévő bemenet, akkor a parancsmag megkérdezi, hogy lecseréli-e vagy sem.</span><span class="sxs-lookup"><span data-stu-id="3d18d-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="3d18d-118">3. példa: a bevitt munka lecserélése egy definícióval egy fájlból</span><span class="sxs-lookup"><span data-stu-id="3d18d-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="3d18d-119">Ez a parancs felülírja a EntryStream nevű meglévő beviteli forrás definícióját a definíció fájlból megerősítés nélkül.</span><span class="sxs-lookup"><span data-stu-id="3d18d-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="3d18d-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d18d-120">PARAMETERS</span></span>

### <span data-ttu-id="3d18d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d18d-121">-DefaultProfile</span></span>
<span data-ttu-id="3d18d-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3d18d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d18d-123">-Fájl</span><span class="sxs-lookup"><span data-stu-id="3d18d-123">-File</span></span>
<span data-ttu-id="3d18d-124">Annak a JSON-fájlnak az elérési útját adja meg, amely az Azure stream Analytics által létrehozott bemenet JSON-beli képviseletét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3d18d-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="3d18d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="3d18d-125">-Force</span></span>
<span data-ttu-id="3d18d-126">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="3d18d-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3d18d-127">-Feladatnév</span><span class="sxs-lookup"><span data-stu-id="3d18d-127">-JobName</span></span>
<span data-ttu-id="3d18d-128">Annak az Azure stream-elemzési projektnek a nevét adja meg, amely alatt az Azure stream Analytics-adatbevitel hozható létre.</span><span class="sxs-lookup"><span data-stu-id="3d18d-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="3d18d-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3d18d-129">-Name</span></span>
<span data-ttu-id="3d18d-130">A létrehozandó Azure stream Analytics-bemenet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d18d-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="3d18d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d18d-131">-ResourceGroupName</span></span>
<span data-ttu-id="3d18d-132">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az Azure adatfolyam-bevitelt létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="3d18d-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="3d18d-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3d18d-133">-Confirm</span></span>
<span data-ttu-id="3d18d-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3d18d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d18d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d18d-135">-WhatIf</span></span>
<span data-ttu-id="3d18d-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3d18d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d18d-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3d18d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d18d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d18d-138">CommonParameters</span></span>
<span data-ttu-id="3d18d-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d18d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d18d-140">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d18d-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d18d-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d18d-141">INPUTS</span></span>

### <span data-ttu-id="3d18d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3d18d-142">System.String</span></span>

## <span data-ttu-id="3d18d-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d18d-143">OUTPUTS</span></span>

### <span data-ttu-id="3d18d-144">Microsoft. Azure. Command. StreamAnalytics. models. PSInput</span><span class="sxs-lookup"><span data-stu-id="3d18d-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="3d18d-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d18d-145">NOTES</span></span>

## <span data-ttu-id="3d18d-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d18d-146">RELATED LINKS</span></span>

[<span data-ttu-id="3d18d-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3d18d-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="3d18d-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3d18d-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="3d18d-149">Teszt-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="3d18d-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


