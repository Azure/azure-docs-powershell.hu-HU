---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 73945c02c5c5802e169e0868908874374080b344
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498504"
---
# <span data-ttu-id="d61c9-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d61c9-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="d61c9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d61c9-102">SYNOPSIS</span></span>
<span data-ttu-id="d61c9-103">Automatizálási runbook hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d61c9-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d61c9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d61c9-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d61c9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d61c9-105">DESCRIPTION</span></span>
<span data-ttu-id="d61c9-106">A **New-AzureRmAutomationRunbook** parancsmag üres Azure automatizálási runbook hoz létre az APS használatával.</span><span class="sxs-lookup"><span data-stu-id="d61c9-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="d61c9-107">Adja meg a runbook nevét.</span><span class="sxs-lookup"><span data-stu-id="d61c9-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="d61c9-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d61c9-108">EXAMPLES</span></span>

### <span data-ttu-id="d61c9-109">Példa 1: runbook létrehozása</span><span class="sxs-lookup"><span data-stu-id="d61c9-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d61c9-110">Ez a parancs létrehoz egy Runbook02 nevű runbook a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="d61c9-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d61c9-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d61c9-111">PARAMETERS</span></span>

### <span data-ttu-id="d61c9-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d61c9-112">-AutomationAccountName</span></span>
<span data-ttu-id="d61c9-113">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag létrehoz egy runbook.</span><span class="sxs-lookup"><span data-stu-id="d61c9-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="d61c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d61c9-114">-DefaultProfile</span></span>
<span data-ttu-id="d61c9-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d61c9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d61c9-116">-Leírás</span><span class="sxs-lookup"><span data-stu-id="d61c9-116">-Description</span></span>
<span data-ttu-id="d61c9-117">A runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="d61c9-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="d61c9-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="d61c9-118">-LogProgress</span></span>
<span data-ttu-id="d61c9-119">Meghatározza, hogy a runbook naplózása folyamatban van-e.</span><span class="sxs-lookup"><span data-stu-id="d61c9-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="d61c9-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="d61c9-120">-LogVerbose</span></span>
<span data-ttu-id="d61c9-121">Meghatározza, hogy a naplózás tartalmaz-e részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="d61c9-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="d61c9-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d61c9-122">-Name</span></span>
<span data-ttu-id="d61c9-123">A runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d61c9-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="d61c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d61c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="d61c9-125">Annak az erőforráscsoport a neve, amelyhez a parancsmag létrehoz egy runbook.</span><span class="sxs-lookup"><span data-stu-id="d61c9-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="d61c9-126">-Címkék</span><span class="sxs-lookup"><span data-stu-id="d61c9-126">-Tags</span></span>
<span data-ttu-id="d61c9-127">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="d61c9-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d61c9-128">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="d61c9-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d61c9-129">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="d61c9-129">-Type</span></span>
<span data-ttu-id="d61c9-130">A parancsmag által létrehozott runbook adja meg.</span><span class="sxs-lookup"><span data-stu-id="d61c9-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="d61c9-131">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d61c9-131">Valid values are:</span></span>
- <span data-ttu-id="d61c9-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d61c9-132">PowerShell</span></span>
- <span data-ttu-id="d61c9-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="d61c9-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="d61c9-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="d61c9-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="d61c9-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="d61c9-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="d61c9-136">Gráf: az érték grafikonja elavult.</span><span class="sxs-lookup"><span data-stu-id="d61c9-136">Graph The value Graph is obsolete.</span></span>
<span data-ttu-id="d61c9-137">Egyenértékű a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="d61c9-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d61c9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d61c9-138">CommonParameters</span></span>
<span data-ttu-id="d61c9-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d61c9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d61c9-140">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d61c9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d61c9-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d61c9-141">INPUTS</span></span>

### <span data-ttu-id="d61c9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d61c9-142">System.String</span></span>

### <span data-ttu-id="d61c9-143">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="d61c9-143">System.Collections.IDictionary</span></span>

### <span data-ttu-id="d61c9-144">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d61c9-144">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d61c9-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d61c9-145">OUTPUTS</span></span>

### <span data-ttu-id="d61c9-146">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="d61c9-146">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="d61c9-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d61c9-147">NOTES</span></span>

## <span data-ttu-id="d61c9-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d61c9-148">RELATED LINKS</span></span>

[<span data-ttu-id="d61c9-149">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d61c9-149">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d61c9-150">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d61c9-150">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d61c9-151">Importálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d61c9-151">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d61c9-152">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d61c9-152">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d61c9-153">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d61c9-153">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d61c9-154">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d61c9-154">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="d61c9-155">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d61c9-155">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
