---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationJobOutputRecord.md
ms.openlocfilehash: 18551d6d839991cf0eb9e020c62fa0a24207d1e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497767"
---
# <span data-ttu-id="fe6d3-101">Get-AzureRmAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="fe6d3-101">Get-AzureRmAutomationJobOutputRecord</span></span>

## <span data-ttu-id="fe6d3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe6d3-102">SYNOPSIS</span></span>
<span data-ttu-id="fe6d3-103">Az automatizálási projekt kimeneti rekordjának teljes kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-103">Gets the full output of an Automation job output record.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe6d3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe6d3-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe6d3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe6d3-105">DESCRIPTION</span></span>
<span data-ttu-id="fe6d3-106">A **Get-AzureRmAutomationJobOutputRecord** parancsmag az automatizálási projekt kimeneti rekordjának teljes kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-106">The **Get-AzureRmAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>

<span data-ttu-id="fe6d3-107">Noha a **Get-AzureRmAutomationJobOutput** parancsmag egy vagy több projekt-kimeneti rekordot is felsorol, az eredmény csak egy összesítést ad eredményül, karakterláncként az esetleges kimeneti rekordok értékétől.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-107">Although the **Get-AzureRmAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="fe6d3-108">A Készletrevételi rekord teljes értékét nem adja vissza eredeti típusában.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="fe6d3-109">Az összesítésben a maximális hossz is szerepel, amely az adott parancsmag kimenetének teljes értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="fe6d3-110">A **Get-AzureRmAutomationJobOutput** ellentétben ez a parancsmag az eredetileg kitermelt típus teljes értékét adja eredményül bármely kimeneti rekord kivezetett értékéhez.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-110">Unlike **Get-AzureRmAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="fe6d3-111">Példák</span><span class="sxs-lookup"><span data-stu-id="fe6d3-111">EXAMPLES</span></span>

### <span data-ttu-id="fe6d3-112">Példa 1: automatizálási feladat teljes kimenetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="fe6d3-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzureRmAutomationJobOutputRecord
```

<span data-ttu-id="fe6d3-113">Ez a parancs a megadott AZONOSÍTÓJÚ projekt teljes kimenetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="fe6d3-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe6d3-114">PARAMETERS</span></span>

### <span data-ttu-id="fe6d3-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fe6d3-115">-AutomationAccountName</span></span>
<span data-ttu-id="fe6d3-116">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag a projekt kimeneti rekordját kapja.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="fe6d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe6d3-117">-DefaultProfile</span></span>
<span data-ttu-id="fe6d3-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fe6d3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe6d3-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="fe6d3-119">-Id</span></span>
<span data-ttu-id="fe6d3-120">A lekérdezni kívánt projekt kimeneti rekordjainak AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="fe6d3-121">-JobId</span></span>
<span data-ttu-id="fe6d3-122">Annak a projektnek az AZONOSÍTÓját adja meg, amelyhez ez a parancsmag kimeneti rekordot kap.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe6d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe6d3-124">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag a projekt kimeneti rekordját kapja.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="fe6d3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6d3-125">CommonParameters</span></span>
<span data-ttu-id="fe6d3-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe6d3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6d3-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe6d3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6d3-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe6d3-128">INPUTS</span></span>

### <span data-ttu-id="fe6d3-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="fe6d3-129">None</span></span>
<span data-ttu-id="fe6d3-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="fe6d3-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe6d3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe6d3-131">OUTPUTS</span></span>

### <span data-ttu-id="fe6d3-132">Microsoft. Azure. Command. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="fe6d3-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="fe6d3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe6d3-133">NOTES</span></span>

## <span data-ttu-id="fe6d3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe6d3-134">RELATED LINKS</span></span>

[<span data-ttu-id="fe6d3-135">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="fe6d3-135">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)


