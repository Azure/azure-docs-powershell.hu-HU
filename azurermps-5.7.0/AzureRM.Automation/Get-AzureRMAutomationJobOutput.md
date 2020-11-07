---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: d46dd2e314aa8064b305adb0501ae20480a34418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672177"
---
# <span data-ttu-id="97b61-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="97b61-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="97b61-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="97b61-102">SYNOPSIS</span></span>
<span data-ttu-id="97b61-103">Egy automatizálási feladat eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="97b61-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97b61-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="97b61-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="97b61-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="97b61-105">DESCRIPTION</span></span>
<span data-ttu-id="97b61-106">A **Get-AzureRmAutomationJobOutput** parancsmag az Azure automatizálási feladatok eredményét kapja.</span><span class="sxs-lookup"><span data-stu-id="97b61-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="97b61-107">Példák</span><span class="sxs-lookup"><span data-stu-id="97b61-107">EXAMPLES</span></span>

### <span data-ttu-id="97b61-108">Példa 1: automatizálási feladat kimenetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="97b61-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="97b61-109">Ez a parancs a megadott azonosítót tartalmazó feladat minden eredményét megkapja.</span><span class="sxs-lookup"><span data-stu-id="97b61-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="97b61-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="97b61-110">PARAMETERS</span></span>

### <span data-ttu-id="97b61-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="97b61-111">-AutomationAccountName</span></span>
<span data-ttu-id="97b61-112">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag a projekt kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="97b61-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97b61-113">-DefaultProfile</span></span>
<span data-ttu-id="97b61-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="97b61-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97b61-115">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="97b61-115">-Id</span></span>
<span data-ttu-id="97b61-116">Annak a projektnek az AZONOSÍTÓját adja meg, amelyre a parancsmag kimenetet kap.</span><span class="sxs-lookup"><span data-stu-id="97b61-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b61-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97b61-117">-ResourceGroupName</span></span>
<span data-ttu-id="97b61-118">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag a projekt kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="97b61-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b61-119">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="97b61-119">-StartTime</span></span>
<span data-ttu-id="97b61-120">**DateTimeOffset** -objektum kezdési időpontját adja meg.</span><span class="sxs-lookup"><span data-stu-id="97b61-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="97b61-121">Megadhatja, hogy milyen karakterláncot Konvertáljon érvényes **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="97b61-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="97b61-122">A parancsmag ekkor kikeresi az adott időpont után létrehozott kimenetet.</span><span class="sxs-lookup"><span data-stu-id="97b61-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b61-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="97b61-123">-Stream</span></span>
<span data-ttu-id="97b61-124">A kimenet típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="97b61-124">Specifies the type of output.</span></span>
<span data-ttu-id="97b61-125">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="97b61-125">Valid values are:</span></span> 

- <span data-ttu-id="97b61-126">Bármely</span><span class="sxs-lookup"><span data-stu-id="97b61-126">Any</span></span>
- <span data-ttu-id="97b61-127">Hibakereső</span><span class="sxs-lookup"><span data-stu-id="97b61-127">Debug</span></span>
- <span data-ttu-id="97b61-128">Hiba</span><span class="sxs-lookup"><span data-stu-id="97b61-128">Error</span></span>
- <span data-ttu-id="97b61-129">Kimeneti</span><span class="sxs-lookup"><span data-stu-id="97b61-129">Output</span></span>
- <span data-ttu-id="97b61-130">Haladás</span><span class="sxs-lookup"><span data-stu-id="97b61-130">Progress</span></span>
- <span data-ttu-id="97b61-131">Részletes</span><span class="sxs-lookup"><span data-stu-id="97b61-131">Verbose</span></span>
- <span data-ttu-id="97b61-132">Figyelmeztetés</span><span class="sxs-lookup"><span data-stu-id="97b61-132">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97b61-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b61-133">CommonParameters</span></span>
<span data-ttu-id="97b61-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="97b61-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b61-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b61-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b61-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="97b61-136">INPUTS</span></span>

### <span data-ttu-id="97b61-137">Nincs</span><span class="sxs-lookup"><span data-stu-id="97b61-137">None</span></span>
<span data-ttu-id="97b61-138">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="97b61-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="97b61-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="97b61-139">OUTPUTS</span></span>

### <span data-ttu-id="97b61-140">Microsoft. Azure. Command. Automation. Model. JobStream</span><span class="sxs-lookup"><span data-stu-id="97b61-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="97b61-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="97b61-141">NOTES</span></span>

## <span data-ttu-id="97b61-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="97b61-142">RELATED LINKS</span></span>

[<span data-ttu-id="97b61-143">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97b61-143">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="97b61-144">Önéletrajz – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97b61-144">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="97b61-145">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97b61-145">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="97b61-146">Felfüggesztés – AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="97b61-146">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


