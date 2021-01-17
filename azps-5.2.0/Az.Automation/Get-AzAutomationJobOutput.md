---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373840"
---
# <span data-ttu-id="08cc2-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="08cc2-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="08cc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08cc2-102">SYNOPSIS</span></span>
<span data-ttu-id="08cc2-103">Egy automatizálási feladat kimenetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="08cc2-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="08cc2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="08cc2-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08cc2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="08cc2-105">DESCRIPTION</span></span>
<span data-ttu-id="08cc2-106">A **Get-AzAutomation JobOutput** parancsmag egy Azure Automation-feladat kimenetét kapja meg.</span><span class="sxs-lookup"><span data-stu-id="08cc2-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="08cc2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="08cc2-107">EXAMPLES</span></span>

### <span data-ttu-id="08cc2-108">1. példa: Automatizálási feladat kimenetének lekérte</span><span class="sxs-lookup"><span data-stu-id="08cc2-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="08cc2-109">Ez a parancs a megadott azonosítójú feladat összes kimenetét beveszi.</span><span class="sxs-lookup"><span data-stu-id="08cc2-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="08cc2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08cc2-110">PARAMETERS</span></span>

### <span data-ttu-id="08cc2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="08cc2-111">-AutomationAccountName</span></span>
<span data-ttu-id="08cc2-112">Annak az automatizálási fióknak a nevét adja meg, amelynek a parancsmagja kimeneti feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="08cc2-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="08cc2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08cc2-113">-DefaultProfile</span></span>
<span data-ttu-id="08cc2-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="08cc2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08cc2-115">-Id</span><span class="sxs-lookup"><span data-stu-id="08cc2-115">-Id</span></span>
<span data-ttu-id="08cc2-116">Annak a feladatnak az azonosítóját adja meg, amelynek kimenetét ez a parancsmag kapja.</span><span class="sxs-lookup"><span data-stu-id="08cc2-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="08cc2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08cc2-117">-ResourceGroupName</span></span>
<span data-ttu-id="08cc2-118">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja kimeneti feladatot kap.</span><span class="sxs-lookup"><span data-stu-id="08cc2-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="08cc2-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="08cc2-119">-StartTime</span></span>
<span data-ttu-id="08cc2-120">Kezdő időpontot ad meg **DateTimeOffset** objektumként.</span><span class="sxs-lookup"><span data-stu-id="08cc2-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="08cc2-121">Megadhat egy olyan karakterláncot, amely érvényes **DateTimeOffset** formátumba alakítható.</span><span class="sxs-lookup"><span data-stu-id="08cc2-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="08cc2-122">A parancsmag beolvassa az ezt követően létrehozott kimenetet.</span><span class="sxs-lookup"><span data-stu-id="08cc2-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="08cc2-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="08cc2-123">-Stream</span></span>
<span data-ttu-id="08cc2-124">A kimenet típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="08cc2-124">Specifies the type of output.</span></span>
<span data-ttu-id="08cc2-125">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="08cc2-125">Valid values are:</span></span> 
- <span data-ttu-id="08cc2-126">Bármely</span><span class="sxs-lookup"><span data-stu-id="08cc2-126">Any</span></span>
- <span data-ttu-id="08cc2-127">Hibakeresés</span><span class="sxs-lookup"><span data-stu-id="08cc2-127">Debug</span></span>
- <span data-ttu-id="08cc2-128">Hiba</span><span class="sxs-lookup"><span data-stu-id="08cc2-128">Error</span></span>
- <span data-ttu-id="08cc2-129">Kimenet</span><span class="sxs-lookup"><span data-stu-id="08cc2-129">Output</span></span>
- <span data-ttu-id="08cc2-130">Haladás</span><span class="sxs-lookup"><span data-stu-id="08cc2-130">Progress</span></span>
- <span data-ttu-id="08cc2-131">Verbose</span><span class="sxs-lookup"><span data-stu-id="08cc2-131">Verbose</span></span>
- <span data-ttu-id="08cc2-132">Figyelmeztetés</span><span class="sxs-lookup"><span data-stu-id="08cc2-132">Warning</span></span>

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

### <span data-ttu-id="08cc2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08cc2-133">CommonParameters</span></span>
<span data-ttu-id="08cc2-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08cc2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08cc2-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08cc2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08cc2-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08cc2-136">INPUTS</span></span>

### <span data-ttu-id="08cc2-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="08cc2-137">System.Guid</span></span>

### <span data-ttu-id="08cc2-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span><span class="sxs-lookup"><span data-stu-id="08cc2-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="08cc2-139">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="08cc2-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="08cc2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="08cc2-140">System.String</span></span>

## <span data-ttu-id="08cc2-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08cc2-141">OUTPUTS</span></span>

### <span data-ttu-id="08cc2-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="08cc2-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="08cc2-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="08cc2-143">NOTES</span></span>

## <span data-ttu-id="08cc2-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08cc2-144">RELATED LINKS</span></span>

[<span data-ttu-id="08cc2-145">Get-AzAutomation Azerbajdzsán</span><span class="sxs-lookup"><span data-stu-id="08cc2-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="08cc2-146">Resume-AzAutomation Azerbajdzsán</span><span class="sxs-lookup"><span data-stu-id="08cc2-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="08cc2-147">Stop-AzAutomationJobra</span><span class="sxs-lookup"><span data-stu-id="08cc2-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="08cc2-148">Suspend-AzAutomationJobra</span><span class="sxs-lookup"><span data-stu-id="08cc2-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


