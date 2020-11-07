---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
ms.openlocfilehash: bbf86c6744e064b2958acaf5fe7928d537548805
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671564"
---
# <span data-ttu-id="8d83f-101">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d83f-101">New-AzAutomationRunbook</span></span>

## <span data-ttu-id="8d83f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d83f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d83f-103">Automatizálási runbook hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8d83f-103">Creates an Automation runbook.</span></span>

## <span data-ttu-id="8d83f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d83f-104">SYNTAX</span></span>

```
New-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d83f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d83f-105">DESCRIPTION</span></span>
<span data-ttu-id="8d83f-106">A **New-AzAutomationRunbook** parancsmag üres Azure automatizálási runbook hoz létre az APS használatával.</span><span class="sxs-lookup"><span data-stu-id="8d83f-106">The **New-AzAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="8d83f-107">Adja meg a runbook nevét.</span><span class="sxs-lookup"><span data-stu-id="8d83f-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="8d83f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8d83f-108">EXAMPLES</span></span>

### <span data-ttu-id="8d83f-109">Példa 1: runbook létrehozása</span><span class="sxs-lookup"><span data-stu-id="8d83f-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8d83f-110">Ez a parancs létrehoz egy Runbook02 nevű runbook a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="8d83f-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="8d83f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d83f-111">PARAMETERS</span></span>

### <span data-ttu-id="8d83f-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8d83f-112">-AutomationAccountName</span></span>
<span data-ttu-id="8d83f-113">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag létrehoz egy runbook.</span><span class="sxs-lookup"><span data-stu-id="8d83f-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="8d83f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d83f-114">-DefaultProfile</span></span>
<span data-ttu-id="8d83f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="8d83f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d83f-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="8d83f-116">-Description</span></span>
<span data-ttu-id="8d83f-117">A runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d83f-117">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d83f-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="8d83f-118">-LogProgress</span></span>
<span data-ttu-id="8d83f-119">Meghatározza, hogy a runbook naplózása folyamatban van-e.</span><span class="sxs-lookup"><span data-stu-id="8d83f-119">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d83f-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="8d83f-120">-LogVerbose</span></span>
<span data-ttu-id="8d83f-121">Meghatározza, hogy a naplózás tartalmaz-e részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="8d83f-121">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d83f-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8d83f-122">-Name</span></span>
<span data-ttu-id="8d83f-123">A runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d83f-123">Specifies a name for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d83f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d83f-124">-ResourceGroupName</span></span>
<span data-ttu-id="8d83f-125">Annak az erőforráscsoport a neve, amelyhez a parancsmag létrehoz egy runbook.</span><span class="sxs-lookup"><span data-stu-id="8d83f-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="8d83f-126">-Címkék</span><span class="sxs-lookup"><span data-stu-id="8d83f-126">-Tags</span></span>
<span data-ttu-id="8d83f-127">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="8d83f-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8d83f-128">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="8d83f-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d83f-129">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="8d83f-129">-Type</span></span>
<span data-ttu-id="8d83f-130">A parancsmag által létrehozott runbook adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d83f-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="8d83f-131">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="8d83f-131">Valid values are:</span></span>
- <span data-ttu-id="8d83f-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d83f-132">PowerShell</span></span>
- <span data-ttu-id="8d83f-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="8d83f-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="8d83f-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="8d83f-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="8d83f-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="8d83f-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="8d83f-136">Graph</span><span class="sxs-lookup"><span data-stu-id="8d83f-136">Graph</span></span>
- <span data-ttu-id="8d83f-137">Python2 az érték grafikonja elavult.</span><span class="sxs-lookup"><span data-stu-id="8d83f-137">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="8d83f-138">Egyenértékű a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="8d83f-138">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d83f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d83f-139">CommonParameters</span></span>
<span data-ttu-id="8d83f-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d83f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d83f-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d83f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d83f-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d83f-142">INPUTS</span></span>

### <span data-ttu-id="8d83f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8d83f-143">System.String</span></span>

### <span data-ttu-id="8d83f-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="8d83f-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="8d83f-145">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8d83f-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8d83f-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d83f-146">OUTPUTS</span></span>

### <span data-ttu-id="8d83f-147">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="8d83f-147">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="8d83f-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d83f-148">NOTES</span></span>

## <span data-ttu-id="8d83f-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d83f-149">RELATED LINKS</span></span>

[<span data-ttu-id="8d83f-150">Exportálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d83f-150">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="8d83f-151">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d83f-151">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="8d83f-152">Importálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d83f-152">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="8d83f-153">Közzététel – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d83f-153">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="8d83f-154">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d83f-154">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="8d83f-155">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d83f-155">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="8d83f-156">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="8d83f-156">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)
