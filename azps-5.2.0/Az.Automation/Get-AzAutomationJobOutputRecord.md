---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 38BB4F4E-B72B-460E-8DF2-2A7A9CACDB41
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutputrecord
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutputRecord.md
ms.openlocfilehash: 7bece0fd2a9de822a5fa2a513fc06d4d20d96e4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373839"
---
# <span data-ttu-id="b80e3-101">Get-AzAutomationJobOutputRecord</span><span class="sxs-lookup"><span data-stu-id="b80e3-101">Get-AzAutomationJobOutputRecord</span></span>

## <span data-ttu-id="b80e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b80e3-102">SYNOPSIS</span></span>
<span data-ttu-id="b80e3-103">Egy automatizálási kimeneti rekord teljes kimenetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b80e3-103">Gets the full output of an Automation job output record.</span></span>

## <span data-ttu-id="b80e3-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b80e3-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutputRecord [-JobId] <Guid> [-Id] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b80e3-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b80e3-105">DESCRIPTION</span></span>
<span data-ttu-id="b80e3-106">A **Get-AzAutomation JobOutputRecord** parancsmag az Automatizálási kimeneti rekord teljes kimenetét megkapja.</span><span class="sxs-lookup"><span data-stu-id="b80e3-106">The **Get-AzAutomationJobOutputRecord** cmdlet gets the full output of an Automation job output record.</span></span>
<span data-ttu-id="b80e3-107">Bár a **Get-AzAutomation JobOutput** parancsmag egy vagy több kimeneti rekordot tartalmaz, karakterláncként csak a kimeneti rekordok értékének összegzését adja vissza.</span><span class="sxs-lookup"><span data-stu-id="b80e3-107">Although the **Get-AzAutomationJobOutput** cmdlet lists one or more job output records, it returns only a summary, as a string, of the value of any output record.</span></span>
<span data-ttu-id="b80e3-108">Nem adja vissza a kimeneti rekord kimenetként megadott értékének teljes értékét az eredeti típusában.</span><span class="sxs-lookup"><span data-stu-id="b80e3-108">It does not return the full value of an output record's outputted value in its original type.</span></span>
<span data-ttu-id="b80e3-109">Ezenkívül az összegzés maximális hosszát is megadhatja, amely túllépheti a parancsmag kimenetének teljes értékét.</span><span class="sxs-lookup"><span data-stu-id="b80e3-109">In addition, the summary has a maximum length, which the full value that this cmdlet outputs may exceed.</span></span>

## <span data-ttu-id="b80e3-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b80e3-110">EXAMPLES</span></span>

### <span data-ttu-id="b80e3-111">1. példa: Automatizálási feladat teljes eredményének lekérte</span><span class="sxs-lookup"><span data-stu-id="b80e3-111">Example 1: Get the full output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any" | Get-AzAutomationJobOutputRecord
```

<span data-ttu-id="b80e3-112">Ez a parancs annak a feladatnak a teljes kimenetét kapja meg, amely a megadott feladatazonosítóval rendelkezik.</span><span class="sxs-lookup"><span data-stu-id="b80e3-112">This command gets the full output of the job that has the specified job ID.</span></span>

## <span data-ttu-id="b80e3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b80e3-113">PARAMETERS</span></span>

### <span data-ttu-id="b80e3-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b80e3-114">-AutomationAccountName</span></span>
<span data-ttu-id="b80e3-115">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag feladatkimeneti rekordot kap.</span><span class="sxs-lookup"><span data-stu-id="b80e3-115">Specifies the name of an Automation account for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="b80e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b80e3-116">-DefaultProfile</span></span>
<span data-ttu-id="b80e3-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="b80e3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b80e3-118">-Id</span><span class="sxs-lookup"><span data-stu-id="b80e3-118">-Id</span></span>
<span data-ttu-id="b80e3-119">Annak a feladatkimeneti rekordnak az azonosítóját adja meg, amelyből a parancsmagot lekéri.</span><span class="sxs-lookup"><span data-stu-id="b80e3-119">Specifies the ID of a job output record for this cmdlet to retrieve.</span></span>

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

### <span data-ttu-id="b80e3-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="b80e3-120">-JobId</span></span>
<span data-ttu-id="b80e3-121">Megadja annak a feladatnak az azonosítóját, amelyhez a parancsmag kimeneti rekordot kap.</span><span class="sxs-lookup"><span data-stu-id="b80e3-121">Specifies the ID of a job for which this cmdlet gets an output record.</span></span>

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

### <span data-ttu-id="b80e3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b80e3-122">-ResourceGroupName</span></span>
<span data-ttu-id="b80e3-123">Annak az erőforráscsoportnak a nevét adja meg, amelyhez ez a parancsmag feladatkimeneti rekordot kap.</span><span class="sxs-lookup"><span data-stu-id="b80e3-123">Specifies the name of a resource group for which this cmdlet gets a job output record.</span></span>

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

### <span data-ttu-id="b80e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b80e3-124">CommonParameters</span></span>
<span data-ttu-id="b80e3-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b80e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b80e3-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b80e3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b80e3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b80e3-127">INPUTS</span></span>

### <span data-ttu-id="b80e3-128">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b80e3-128">System.Guid</span></span>

### <span data-ttu-id="b80e3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b80e3-129">System.String</span></span>

## <span data-ttu-id="b80e3-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b80e3-130">OUTPUTS</span></span>

### <span data-ttu-id="b80e3-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span><span class="sxs-lookup"><span data-stu-id="b80e3-131">Microsoft.Azure.Commands.Automation.Model.JobStreamRecord</span></span>

## <span data-ttu-id="b80e3-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b80e3-132">NOTES</span></span>

## <span data-ttu-id="b80e3-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b80e3-133">RELATED LINKS</span></span>

[<span data-ttu-id="b80e3-134">Get-AzAutomationOutput</span><span class="sxs-lookup"><span data-stu-id="b80e3-134">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)


