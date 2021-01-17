---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 74145a6d65fdaa9634d7681133e10b2496b5f903
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479342"
---
# <span data-ttu-id="ad6c7-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ad6c7-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="ad6c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad6c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6c7-103">Létrehozza vagy frissíti a munkabemenetet.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="ad6c7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ad6c7-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad6c7-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ad6c7-105">DESCRIPTION</span></span>
<span data-ttu-id="ad6c7-106">A **New-AzStreamAnalyticsInput** parancsmag bemeneti adatokat hoz létre egy Stream Analytics-feladaton belül, vagy frissíti a meglévő bemeneteket.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="ad6c7-107">A bemeneti érték nevét meg lehet adni a JSON-fájlban vagy a parancssorban.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="ad6c7-108">Ha mindkettő meg van adva, a parancssorban található névnek meg kell egyeznie a fájlban található névvel.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="ad6c7-109">Ha olyan bemenetet ad meg, amely már létezik, és nem adja meg a *Force* paramétert, a parancsmag megkérdezi, hogy lecseréli-e a meglévő bemenetet.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="ad6c7-110">Ha megadja az *Kényszerítés* paramétert, és megad egy meglévő bemeneti nevet, a rendszer megerősítés nélkül lecseréli a bemenetet.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="ad6c7-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ad6c7-111">EXAMPLES</span></span>

### <span data-ttu-id="ad6c7-112">1. példa: Fájlból származó definícióval bevitt feladat létrehozása</span><span class="sxs-lookup"><span data-stu-id="ad6c7-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="ad6c7-113">Ez a parancs bemenetet hoz létre a be Input.jsfájlból.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="ad6c7-114">Ha a bemeneti definíciós fájlban megadott nevű meglévő beviteli mező már definiálva van, a parancsmag megkérdezi, hogy lecseréli-e azt.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="ad6c7-115">2. példa: Feladatbevitel létrehozása</span><span class="sxs-lookup"><span data-stu-id="ad6c7-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="ad6c7-116">Ez a parancs új bevitelt hoz létre a EntryStream nevű feladatban.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="ad6c7-117">Ha már definiált egy ilyen nevű meglévő bemenetet, a parancsmag megkérdezi, hogy lecseréli-e azt.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="ad6c7-118">3. példa: Feladatbemenet cseréje egy fájlból származó definícióval</span><span class="sxs-lookup"><span data-stu-id="ad6c7-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="ad6c7-119">Ez a parancs jóváhagyás nélkül lecseréli az EntryStream nevű meglévő bemeneti forrás definícióját a fájlból származó definícióra.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="ad6c7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad6c7-120">PARAMETERS</span></span>

### <span data-ttu-id="ad6c7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6c7-121">-DefaultProfile</span></span>
<span data-ttu-id="ad6c7-122">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad6c7-123">-File</span><span class="sxs-lookup"><span data-stu-id="ad6c7-123">-File</span></span>
<span data-ttu-id="ad6c7-124">Egy JSON-fájl elérési útját adja meg, amely tartalmazza a létrehozni kívánt Azure Stream Analytics-bemenet JSON-ábrázolásait.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="ad6c7-125">-Force</span><span class="sxs-lookup"><span data-stu-id="ad6c7-125">-Force</span></span>
<span data-ttu-id="ad6c7-126">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad6c7-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="ad6c7-127">-JobName</span></span>
<span data-ttu-id="ad6c7-128">Megadja annak az Azure Stream Analytics-feladatnak a nevét, amely alatt létre kell hoznia az Azure Stream Analytics-bemenetet.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="ad6c7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ad6c7-129">-Name</span></span>
<span data-ttu-id="ad6c7-130">Megadja a létrehozni szükséges Azure Stream Analytics-bemenet nevét.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="ad6c7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad6c7-131">-ResourceGroupName</span></span>
<span data-ttu-id="ad6c7-132">Annak az erőforráscsoportnak a nevét adja meg, amely alatt létre kell hoznia az Azure Streaming-bemenetet.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="ad6c7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad6c7-133">-Confirm</span></span>
<span data-ttu-id="ad6c7-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad6c7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad6c7-135">-WhatIf</span></span>
<span data-ttu-id="ad6c7-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad6c7-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad6c7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6c7-138">CommonParameters</span></span>
<span data-ttu-id="ad6c7-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad6c7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6c7-140">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad6c7-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6c7-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad6c7-141">INPUTS</span></span>

### <span data-ttu-id="ad6c7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="ad6c7-142">System.String</span></span>

## <span data-ttu-id="ad6c7-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad6c7-143">OUTPUTS</span></span>

### <span data-ttu-id="ad6c7-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="ad6c7-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="ad6c7-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ad6c7-145">NOTES</span></span>

## <span data-ttu-id="ad6c7-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad6c7-146">RELATED LINKS</span></span>

[<span data-ttu-id="ad6c7-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ad6c7-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="ad6c7-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ad6c7-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="ad6c7-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="ad6c7-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


