---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 60de6b852d516cd4742ed253d149ea031449548b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671616"
---
# <span data-ttu-id="69071-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="69071-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="69071-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="69071-102">SYNOPSIS</span></span>
<span data-ttu-id="69071-103">Egy automatizálási feladat eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="69071-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="69071-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="69071-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69071-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="69071-105">DESCRIPTION</span></span>
<span data-ttu-id="69071-106">A **Get-AzAutomationJobOutput** parancsmag az Azure automatizálási feladatok eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="69071-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="69071-107">Példák</span><span class="sxs-lookup"><span data-stu-id="69071-107">EXAMPLES</span></span>

### <span data-ttu-id="69071-108">Példa 1: automatizálási feladat kimenetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="69071-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="69071-109">Ez a parancs a megadott azonosítót tartalmazó feladat minden eredményét megkapja.</span><span class="sxs-lookup"><span data-stu-id="69071-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="69071-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="69071-110">PARAMETERS</span></span>

### <span data-ttu-id="69071-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="69071-111">-AutomationAccountName</span></span>
<span data-ttu-id="69071-112">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag a projekt kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="69071-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="69071-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69071-113">-DefaultProfile</span></span>
<span data-ttu-id="69071-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="69071-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69071-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="69071-115">-Id</span></span>
<span data-ttu-id="69071-116">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag kimenetet kap.</span><span class="sxs-lookup"><span data-stu-id="69071-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69071-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69071-117">-ResourceGroupName</span></span>
<span data-ttu-id="69071-118">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag a projekt kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="69071-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="69071-119">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="69071-119">-StartTime</span></span>
<span data-ttu-id="69071-120">**DateTimeOffset** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="69071-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="69071-121">Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="69071-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="69071-122">A parancsmag ekkor kikeresi az adott időpont után létrehozott kimenetet.</span><span class="sxs-lookup"><span data-stu-id="69071-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69071-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="69071-123">-Stream</span></span>
<span data-ttu-id="69071-124">A kimenet típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="69071-124">Specifies the type of output.</span></span>
<span data-ttu-id="69071-125">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="69071-125">Valid values are:</span></span> 
- <span data-ttu-id="69071-126">Bármely</span><span class="sxs-lookup"><span data-stu-id="69071-126">Any</span></span>
- <span data-ttu-id="69071-127">Hibakereső</span><span class="sxs-lookup"><span data-stu-id="69071-127">Debug</span></span>
- <span data-ttu-id="69071-128">Hiba</span><span class="sxs-lookup"><span data-stu-id="69071-128">Error</span></span>
- <span data-ttu-id="69071-129">Kimeneti</span><span class="sxs-lookup"><span data-stu-id="69071-129">Output</span></span>
- <span data-ttu-id="69071-130">Haladás</span><span class="sxs-lookup"><span data-stu-id="69071-130">Progress</span></span>
- <span data-ttu-id="69071-131">Részletes</span><span class="sxs-lookup"><span data-stu-id="69071-131">Verbose</span></span>
- <span data-ttu-id="69071-132">Figyelmeztetés</span><span class="sxs-lookup"><span data-stu-id="69071-132">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Progress, Output, Warning, Error, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69071-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69071-133">CommonParameters</span></span>
<span data-ttu-id="69071-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="69071-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69071-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69071-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69071-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="69071-136">INPUTS</span></span>

### <span data-ttu-id="69071-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="69071-137">System.Guid</span></span>

### <span data-ttu-id="69071-138">Microsoft. Azure. Command. Automation. Common. StreamType</span><span class="sxs-lookup"><span data-stu-id="69071-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="69071-139">System. null ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="69071-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="69071-140">System. String</span><span class="sxs-lookup"><span data-stu-id="69071-140">System.String</span></span>

## <span data-ttu-id="69071-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="69071-141">OUTPUTS</span></span>

### <span data-ttu-id="69071-142">Microsoft. Azure. Command. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="69071-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="69071-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="69071-143">NOTES</span></span>

## <span data-ttu-id="69071-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="69071-144">RELATED LINKS</span></span>

[<span data-ttu-id="69071-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="69071-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="69071-146">Önéletrajz – AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="69071-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="69071-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="69071-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="69071-148">Felfüggesztés – AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="69071-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


