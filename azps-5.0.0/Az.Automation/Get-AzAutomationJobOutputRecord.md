---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194826"
---
# <span data-ttu-id="ffd44-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="ffd44-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="ffd44-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ffd44-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd44-103">Az automatizálási projekt kimeneti rekordjának teljes kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="ffd44-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="ffd44-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ffd44-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffd44-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ffd44-105">DESCRIPTION</span></span>
<span data-ttu-id="ffd44-106">A **Get-AzAutomationJobOutputRecord** parancsmag az automatizálási projekt kimeneti rekordjának teljes kimenetét kapja.</span><span class="sxs-lookup"><span data-stu-id="ffd44-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="ffd44-107">Noha a **Get-AzAutomationJobOutput** parancsmag egy vagy több projekt-kimeneti rekordot is felsorol, az eredmény csak egy összesítést ad eredményül, karakterláncként az esetleges kimeneti rekordok értékétől.</span><span class="sxs-lookup"><span data-stu-id="ffd44-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="ffd44-108">A Készletrevételi rekord teljes értékét nem adja vissza eredeti típusában.</span><span class="sxs-lookup"><span data-stu-id="ffd44-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="ffd44-109">Az összesítésben a maximális hossz is szerepel, amely az adott parancsmag kimenetének teljes értékét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffd44-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="ffd44-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ffd44-110">EXAMPLES</span></span>

### <span data-ttu-id="ffd44-111">Példa 1: automatizálási feladat teljes kimenetének beszerzése</span><span class="sxs-lookup"><span data-stu-id="ffd44-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="ffd44-112">Ez a parancs a megadott AZONOSÍTÓJÚ projekt teljes kimenetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ffd44-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="ffd44-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ffd44-113">PARAMETERS</span></span>

### <span data-ttu-id="ffd44-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ffd44-114">-AutomationAccountName</span></span>
<span data-ttu-id="ffd44-115">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag a projekt kimeneti rekordját kapja.</span><span class="sxs-lookup"><span data-stu-id="ffd44-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="ffd44-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd44-116">-DefaultProfile</span></span>
<span data-ttu-id="ffd44-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ffd44-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffd44-118">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="ffd44-118">-Id</span></span>
<span data-ttu-id="ffd44-119">A lekérdezni kívánt projekt kimeneti rekordjainak AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ffd44-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="ffd44-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="ffd44-120">-JobId</span></span>
<span data-ttu-id="ffd44-121">Annak a projektnek az AZONOSÍTÓját adja meg, amelyhez ez a parancsmag kimeneti rekordot kap.</span><span class="sxs-lookup"><span data-stu-id="ffd44-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="ffd44-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffd44-122">-ResourceGroupName</span></span>
<span data-ttu-id="ffd44-123">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag a projekt kimeneti rekordját kapja.</span><span class="sxs-lookup"><span data-stu-id="ffd44-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="ffd44-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd44-124">CommonParameters</span></span>
<span data-ttu-id="ffd44-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ffd44-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd44-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffd44-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd44-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffd44-127">INPUTS</span></span>

### <span data-ttu-id="ffd44-128">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ffd44-128">System.Guid</span></span>

### <span data-ttu-id="ffd44-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ffd44-129">System.String</span></span>

## <span data-ttu-id="ffd44-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffd44-130">OUTPUTS</span></span>

### <span data-ttu-id="ffd44-131">Microsoft. Azure. Command. Automation. Model. JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="ffd44-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="ffd44-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ffd44-132">NOTES</span></span>

## <span data-ttu-id="ffd44-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffd44-133">RELATED LINKS</span></span>

[<span data-ttu-id="ffd44-134">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="ffd44-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


