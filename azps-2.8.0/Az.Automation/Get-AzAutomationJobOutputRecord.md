---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: f5c6976ca1fa398c38f642cef757f0e7956f40c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667843"
---
# <span data-ttu-id="2b33f-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="2b33f-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="2b33f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2b33f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b33f-103">Az automatizálási projekt kimeneti rekordjának teljes kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="2b33f-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="2b33f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2b33f-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b33f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2b33f-105">DESCRIPTION</span></span>
<span data-ttu-id="2b33f-106">A **Get-AzAutomationJobOutputRecord** parancsmag az automatizálási projekt kimeneti rekordjának teljes kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="2b33f-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="2b33f-107">Noha a **Get-AzAutomationJobOutput** parancsmag egy vagy több projekt-kimeneti rekordot is felsorol, az eredmény csak egy összesítést ad eredményül, karakterláncként az esetleges kimeneti rekordok értékétől.</span><span class="sxs-lookup"><span data-stu-id="2b33f-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="2b33f-108">A Készletrevételi rekord teljes értékét nem adja vissza eredeti típusában.</span><span class="sxs-lookup"><span data-stu-id="2b33f-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="2b33f-109">Az összesítésben a maximális hossz is szerepel, amely az adott parancsmag kimenetének teljes értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b33f-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>
<span data-ttu-id="2b33f-110">A **Get-AzAutomationJobOutput** ellentétben ez a parancsmag az eredetileg kitermelt típus teljes értékét adja eredményül bármely kimeneti rekord kivezetett értékéhez.</span><span class="sxs-lookup"><span data-stu-id="2b33f-110">Unlike **Get-AzAutomationJobOutput** , this cmdlet returns the full value in its originally outputted type, for any output record's outputted value.</span></span>

## <span data-ttu-id="2b33f-111">Példák</span><span class="sxs-lookup"><span data-stu-id="2b33f-111">EXAMPLES</span></span>

### <span data-ttu-id="2b33f-112">Példa 1: automatizálási feladat teljes kimenetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="2b33f-112">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="2b33f-113">Ez a parancs a megadott AZONOSÍTÓJÚ projekt teljes kimenetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2b33f-113">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="2b33f-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2b33f-114">PARAMETERS</span></span>

### <span data-ttu-id="2b33f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2b33f-115">-AutomationAccountName</span></span>
<span data-ttu-id="2b33f-116">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag a projekt kimeneti rekordját kapja.</span><span class="sxs-lookup"><span data-stu-id="2b33f-116">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="2b33f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b33f-117">-DefaultProfile</span></span>
<span data-ttu-id="2b33f-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2b33f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b33f-119">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="2b33f-119">-Id</span></span>
<span data-ttu-id="2b33f-120">A lekérdezni kívánt projekt kimeneti rekordjainak AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2b33f-120">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="2b33f-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="2b33f-121">-JobId</span></span>
<span data-ttu-id="2b33f-122">Annak a projektnek az AZONOSÍTÓját adja meg, amelyhez ez a parancsmag kimeneti rekordot kap.</span><span class="sxs-lookup"><span data-stu-id="2b33f-122">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="2b33f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b33f-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b33f-124">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag a projekt kimeneti rekordját kapja.</span><span class="sxs-lookup"><span data-stu-id="2b33f-124">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="2b33f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b33f-125">CommonParameters</span></span>
<span data-ttu-id="2b33f-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2b33f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b33f-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b33f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b33f-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b33f-128">INPUTS</span></span>

### <span data-ttu-id="2b33f-129">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2b33f-129">System.Guid</span></span>

### <span data-ttu-id="2b33f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2b33f-130">System.String</span></span>

## <span data-ttu-id="2b33f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2b33f-131">OUTPUTS</span></span>

### <span data-ttu-id="2b33f-132">Microsoft. Azure. Command. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="2b33f-132">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="2b33f-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2b33f-133">NOTES</span></span>

## <span data-ttu-id="2b33f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2b33f-134">RELATED LINKS</span></span>

[<span data-ttu-id="2b33f-135">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="2b33f-135">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


