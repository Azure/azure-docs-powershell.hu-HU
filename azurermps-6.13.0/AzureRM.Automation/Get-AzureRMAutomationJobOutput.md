---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: e2b965800c4f8307edaedf25b032767ca1784049
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502268"
---
# <span data-ttu-id="a5f50-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a5f50-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="a5f50-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5f50-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f50-103">Egy automatizálási feladat eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="a5f50-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5f50-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5f50-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5f50-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5f50-105">DESCRIPTION</span></span>
<span data-ttu-id="a5f50-106">A **Get-AzureRmAutomationJobOutput** parancsmag az Azure automatizálási feladatok eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="a5f50-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="a5f50-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a5f50-107">EXAMPLES</span></span>

### <span data-ttu-id="a5f50-108">Példa 1: automatizálási feladat kimenetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="a5f50-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="a5f50-109">Ez a parancs a megadott azonosítót tartalmazó feladat minden eredményét megkapja.</span><span class="sxs-lookup"><span data-stu-id="a5f50-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="a5f50-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5f50-110">PARAMETERS</span></span>

### <span data-ttu-id="a5f50-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a5f50-111">-AutomationAccountName</span></span>
<span data-ttu-id="a5f50-112">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag a projekt kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="a5f50-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="a5f50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f50-113">-DefaultProfile</span></span>
<span data-ttu-id="a5f50-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a5f50-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f50-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a5f50-115">-Id</span></span>
<span data-ttu-id="a5f50-116">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag kimenetet kap.</span><span class="sxs-lookup"><span data-stu-id="a5f50-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="a5f50-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5f50-117">-ResourceGroupName</span></span>
<span data-ttu-id="a5f50-118">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag a projekt kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="a5f50-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="a5f50-119">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="a5f50-119">-StartTime</span></span>
<span data-ttu-id="a5f50-120">**DateTimeOffset** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5f50-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="a5f50-121">Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="a5f50-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="a5f50-122">A parancsmag ekkor kikeresi az adott időpont után létrehozott kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a5f50-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="a5f50-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="a5f50-123">-Stream</span></span>
<span data-ttu-id="a5f50-124">A kimenet típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5f50-124">Specifies the type of output.</span></span>
<span data-ttu-id="a5f50-125">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="a5f50-125">Valid values are:</span></span> 
- <span data-ttu-id="a5f50-126">Bármely</span><span class="sxs-lookup"><span data-stu-id="a5f50-126">Any</span></span>
- <span data-ttu-id="a5f50-127">Hibakereső</span><span class="sxs-lookup"><span data-stu-id="a5f50-127">Debug</span></span>
- <span data-ttu-id="a5f50-128">Hiba</span><span class="sxs-lookup"><span data-stu-id="a5f50-128">Error</span></span>
- <span data-ttu-id="a5f50-129">Kimeneti</span><span class="sxs-lookup"><span data-stu-id="a5f50-129">Output</span></span>
- <span data-ttu-id="a5f50-130">Haladás</span><span class="sxs-lookup"><span data-stu-id="a5f50-130">Progress</span></span>
- <span data-ttu-id="a5f50-131">Részletes</span><span class="sxs-lookup"><span data-stu-id="a5f50-131">Verbose</span></span>
- <span data-ttu-id="a5f50-132">Figyelmeztetés</span><span class="sxs-lookup"><span data-stu-id="a5f50-132">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5f50-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f50-133">CommonParameters</span></span>
<span data-ttu-id="a5f50-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5f50-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f50-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5f50-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f50-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5f50-136">INPUTS</span></span>

### <span data-ttu-id="a5f50-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a5f50-137">System.Guid</span></span>

### <span data-ttu-id="a5f50-138">Microsoft. Azure. Command. Automation. Common. StreamType</span><span class="sxs-lookup"><span data-stu-id="a5f50-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="a5f50-139">System. null ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a5f50-139">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a5f50-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a5f50-140">System.String</span></span>

## <span data-ttu-id="a5f50-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5f50-141">OUTPUTS</span></span>

### <span data-ttu-id="a5f50-142">Microsoft. Azure. Command. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="a5f50-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="a5f50-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5f50-143">NOTES</span></span>

## <span data-ttu-id="a5f50-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5f50-144">RELATED LINKS</span></span>

[<span data-ttu-id="a5f50-145">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a5f50-145">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="a5f50-146">Önéletrajz – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a5f50-146">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="a5f50-147">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a5f50-147">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="a5f50-148">Felfüggesztés – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a5f50-148">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


