---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194827"
---
# <span data-ttu-id="ab5f1-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="ab5f1-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="ab5f1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ab5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ab5f1-103">Egy automatizálási feladat eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="ab5f1-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="ab5f1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ab5f1-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab5f1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ab5f1-105">DESCRIPTION</span></span>
<span data-ttu-id="ab5f1-106">A **Get-AzAutomationJobOutput** parancsmag az Azure automatizálási feladatok eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="ab5f1-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="ab5f1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ab5f1-107">EXAMPLES</span></span>

### <span data-ttu-id="ab5f1-108">Példa 1: automatizálási feladat kimenetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ab5f1-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="ab5f1-109">Ez a parancs a megadott azonosítót tartalmazó feladat minden eredményét megkapja.</span><span class="sxs-lookup"><span data-stu-id="ab5f1-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="ab5f1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ab5f1-110">PARAMETERS</span></span>

### <span data-ttu-id="ab5f1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ab5f1-111">-AutomationAccountName</span></span>
<span data-ttu-id="ab5f1-112">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag a projekt kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="ab5f1-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="ab5f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab5f1-113">-DefaultProfile</span></span>
<span data-ttu-id="ab5f1-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ab5f1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab5f1-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ab5f1-115">-Id</span></span>
<span data-ttu-id="ab5f1-116">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag kimenetet kap.</span><span class="sxs-lookup"><span data-stu-id="ab5f1-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="ab5f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab5f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="ab5f1-118">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag a projekt kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="ab5f1-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="ab5f1-119">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="ab5f1-119">-StartTime</span></span>
<span data-ttu-id="ab5f1-120">**DateTimeOffset** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab5f1-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="ab5f1-121">Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="ab5f1-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="ab5f1-122">A parancsmag ekkor kikeresi az adott időpont után létrehozott kimenetet.</span><span class="sxs-lookup"><span data-stu-id="ab5f1-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="ab5f1-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="ab5f1-123">-Stream</span></span>
<span data-ttu-id="ab5f1-124">A kimenet típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="ab5f1-124">Specifies the type of output.</span></span>
<span data-ttu-id="ab5f1-125">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="ab5f1-125">Valid values are:</span></span> 
- <span data-ttu-id="ab5f1-126">Bármely</span><span class="sxs-lookup"><span data-stu-id="ab5f1-126">Any</span></span>
- <span data-ttu-id="ab5f1-127">Hibakereső</span><span class="sxs-lookup"><span data-stu-id="ab5f1-127">Debug</span></span>
- <span data-ttu-id="ab5f1-128">Hiba</span><span class="sxs-lookup"><span data-stu-id="ab5f1-128">Error</span></span>
- <span data-ttu-id="ab5f1-129">Kimeneti</span><span class="sxs-lookup"><span data-stu-id="ab5f1-129">Output</span></span>
- <span data-ttu-id="ab5f1-130">Haladás</span><span class="sxs-lookup"><span data-stu-id="ab5f1-130">Progress</span></span>
- <span data-ttu-id="ab5f1-131">Részletes</span><span class="sxs-lookup"><span data-stu-id="ab5f1-131">Verbose</span></span>
- <span data-ttu-id="ab5f1-132">Figyelmeztetés</span><span class="sxs-lookup"><span data-stu-id="ab5f1-132">Warning</span></span>

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

### <span data-ttu-id="ab5f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab5f1-133">CommonParameters</span></span>
<span data-ttu-id="ab5f1-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ab5f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab5f1-135">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab5f1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab5f1-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab5f1-136">INPUTS</span></span>

### <span data-ttu-id="ab5f1-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ab5f1-137">System.Guid</span></span>

### <span data-ttu-id="ab5f1-138">Microsoft. Azure. Command. Automation. Common. StreamType</span><span class="sxs-lookup"><span data-stu-id="ab5f1-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="ab5f1-139">System. null ' 1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ab5f1-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ab5f1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ab5f1-140">System.String</span></span>

## <span data-ttu-id="ab5f1-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ab5f1-141">OUTPUTS</span></span>

### <span data-ttu-id="ab5f1-142">Microsoft. Azure. Command. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="ab5f1-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="ab5f1-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ab5f1-143">NOTES</span></span>

## <span data-ttu-id="ab5f1-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ab5f1-144">RELATED LINKS</span></span>

[<span data-ttu-id="ab5f1-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ab5f1-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="ab5f1-146">Önéletrajz – AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ab5f1-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="ab5f1-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ab5f1-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="ab5f1-148">Felfüggesztés – AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ab5f1-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


