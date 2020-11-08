---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: e43cb76db410752aef0a0cffc72d3d5bb6f8e28f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012675"
---
# <span data-ttu-id="04476-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="04476-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="04476-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="04476-102">SYNOPSIS</span></span>
<span data-ttu-id="04476-103">Az automatizálási projekt kimeneti rekordjának teljes kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="04476-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="04476-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="04476-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04476-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="04476-105">DESCRIPTION</span></span>
<span data-ttu-id="04476-106">A **Get-AzAutomationJobOutputRecord** parancsmag az automatizálási projekt kimeneti rekordjának teljes kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="04476-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="04476-107">Noha a **Get-AzAutomationJobOutput** parancsmag egy vagy több projekt-kimeneti rekordot is felsorol, az eredmény csak egy összesítést ad eredményül, karakterláncként az esetleges kimeneti rekordok értékétől.</span><span class="sxs-lookup"><span data-stu-id="04476-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="04476-108">A Készletrevételi rekord teljes értékét nem adja vissza eredeti típusában.</span><span class="sxs-lookup"><span data-stu-id="04476-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="04476-109">Az összesítésben a maximális hossz is szerepel, amely az adott parancsmag kimenetének teljes értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="04476-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="04476-110">A **Get-AzAutomationJobOutput** ellentétben ez a parancsmag az eredetileg kitermelt típus teljes értékét adja eredményül bármely kimeneti rekord kivezetett értékéhez.</span><span class="sxs-lookup"><span data-stu-id="04476-110">Unlike **Get-AzAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="04476-111">Példák</span><span class="sxs-lookup"><span data-stu-id="04476-111">EXAMPLES</span></span>

### <span data-ttu-id="04476-112">Példa 1: automatizálási feladat teljes kimenetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="04476-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="04476-113">Ez a parancs a megadott AZONOSÍTÓJÚ projekt teljes kimenetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="04476-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="04476-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="04476-114">PARAMETERS</span></span>

### <span data-ttu-id="04476-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="04476-115">-AutomationAccountName</span></span>
<span data-ttu-id="04476-116">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag a projekt kimeneti rekordját kapja.</span><span class="sxs-lookup"><span data-stu-id="04476-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="04476-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04476-117">-DefaultProfile</span></span>
<span data-ttu-id="04476-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="04476-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04476-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="04476-119">-Id</span></span>
<span data-ttu-id="04476-120">A lekérdezni kívánt projekt kimeneti rekordjainak AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="04476-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StreamRecordId

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04476-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="04476-121">-JobId</span></span>
<span data-ttu-id="04476-122">Annak a projektnek az AZONOSÍTÓját adja meg, amelyhez ez a parancsmag kimeneti rekordot kap.</span><span class="sxs-lookup"><span data-stu-id="04476-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04476-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04476-123">-ResourceGroupName</span></span>
<span data-ttu-id="04476-124">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag a projekt kimeneti rekordját kapja.</span><span class="sxs-lookup"><span data-stu-id="04476-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="04476-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04476-125">CommonParameters</span></span>
<span data-ttu-id="04476-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="04476-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04476-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04476-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04476-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="04476-128">INPUTS</span></span>

### <span data-ttu-id="04476-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="04476-129">System.Guid</span></span>

### <span data-ttu-id="04476-130">System. String</span><span class="sxs-lookup"><span data-stu-id="04476-130">System.String</span></span>

## <span data-ttu-id="04476-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="04476-131">OUTPUTS</span></span>

### <span data-ttu-id="04476-132">Microsoft. Azure. Command. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="04476-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="04476-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="04476-133">NOTES</span></span>

## <span data-ttu-id="04476-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="04476-134">RELATED LINKS</span></span>

[<span data-ttu-id="04476-135">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="04476-135">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


