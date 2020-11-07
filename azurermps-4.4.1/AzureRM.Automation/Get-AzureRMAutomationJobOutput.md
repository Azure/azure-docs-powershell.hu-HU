---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: dd80c745c99c98d6ea5b551ab454661d4370cebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680779"
---
# <span data-ttu-id="a114d-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a114d-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="a114d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a114d-102">SYNOPSIS</span></span>
<span data-ttu-id="a114d-103">Egy automatizálási feladat eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="a114d-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a114d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a114d-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a114d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a114d-105">DESCRIPTION</span></span>
<span data-ttu-id="a114d-106">A **Get-AzureRmAutomationJobOutput** parancsmag az Azure automatizálási feladatok eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="a114d-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="a114d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a114d-107">EXAMPLES</span></span>

### <span data-ttu-id="a114d-108">Példa 1: automatizálási feladat kimenetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="a114d-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="a114d-109">Ez a parancs a megadott azonosítót tartalmazó feladat minden eredményét megkapja.</span><span class="sxs-lookup"><span data-stu-id="a114d-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="a114d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a114d-110">PARAMETERS</span></span>

### <span data-ttu-id="a114d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a114d-111">-AutomationAccountName</span></span>
<span data-ttu-id="a114d-112">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag a projekt kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="a114d-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="a114d-113">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a114d-113">-Id</span></span>
<span data-ttu-id="a114d-114">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag kimenetet kap.</span><span class="sxs-lookup"><span data-stu-id="a114d-114">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="a114d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a114d-115">-ResourceGroupName</span></span>
<span data-ttu-id="a114d-116">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag a projekt kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="a114d-116">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="a114d-117">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="a114d-117">-StartTime</span></span>
<span data-ttu-id="a114d-118">**DateTimeOffset** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a114d-118">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="a114d-119">Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="a114d-119">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="a114d-120">A parancsmag ekkor kikeresi az adott időpont után létrehozott kimenetet.</span><span class="sxs-lookup"><span data-stu-id="a114d-120">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="a114d-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="a114d-121">-Stream</span></span>
<span data-ttu-id="a114d-122">A kimenet típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a114d-122">Specifies the type of output.</span></span>
<span data-ttu-id="a114d-123">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="a114d-123">Valid values are:</span></span> 

- <span data-ttu-id="a114d-124">Bármely</span><span class="sxs-lookup"><span data-stu-id="a114d-124">Any</span></span>
- <span data-ttu-id="a114d-125">Hibakereső</span><span class="sxs-lookup"><span data-stu-id="a114d-125">Debug</span></span>
- <span data-ttu-id="a114d-126">Hiba</span><span class="sxs-lookup"><span data-stu-id="a114d-126">Error</span></span>
- <span data-ttu-id="a114d-127">Kimeneti</span><span class="sxs-lookup"><span data-stu-id="a114d-127">Output</span></span>
- <span data-ttu-id="a114d-128">Haladás</span><span class="sxs-lookup"><span data-stu-id="a114d-128">Progress</span></span>
- <span data-ttu-id="a114d-129">Részletes</span><span class="sxs-lookup"><span data-stu-id="a114d-129">Verbose</span></span>
- <span data-ttu-id="a114d-130">Figyelmeztetés</span><span class="sxs-lookup"><span data-stu-id="a114d-130">Warning</span></span>

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

### <span data-ttu-id="a114d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a114d-131">-DefaultProfile</span></span>
<span data-ttu-id="a114d-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a114d-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a114d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a114d-133">CommonParameters</span></span>
<span data-ttu-id="a114d-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a114d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a114d-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a114d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a114d-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a114d-136">INPUTS</span></span>

## <span data-ttu-id="a114d-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a114d-137">OUTPUTS</span></span>

### <span data-ttu-id="a114d-138">Microsoft. Azure. Command. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="a114d-138">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="a114d-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a114d-139">NOTES</span></span>

## <span data-ttu-id="a114d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a114d-140">RELATED LINKS</span></span>

[<span data-ttu-id="a114d-141">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a114d-141">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="a114d-142">Önéletrajz – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a114d-142">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="a114d-143">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a114d-143">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="a114d-144">Felfüggesztés – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a114d-144">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


