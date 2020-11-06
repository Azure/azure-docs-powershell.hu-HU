---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 664bfb83be4394c5aa50213177eda9f16f5ec6b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497960"
---
# <span data-ttu-id="dcbb3-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dcbb3-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="dcbb3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dcbb3-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbb3-103">Automatizálási runbook hoz létre.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcbb3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dcbb3-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcbb3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dcbb3-105">DESCRIPTION</span></span>
<span data-ttu-id="dcbb3-106">A **New-AzureRmAutomationRunbook** parancsmag üres Azure automatizálási runbook hoz létre az APS használatával.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="dcbb3-107">Adja meg a runbook nevét.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="dcbb3-108">Példák</span><span class="sxs-lookup"><span data-stu-id="dcbb3-108">EXAMPLES</span></span>

### <span data-ttu-id="dcbb3-109">Példa 1: runbook létrehozása</span><span class="sxs-lookup"><span data-stu-id="dcbb3-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dcbb3-110">Ez a parancs létrehoz egy Runbook02 nevű runbook a Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="dcbb3-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dcbb3-111">PARAMETERS</span></span>

### <span data-ttu-id="dcbb3-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dcbb3-112">-AutomationAccountName</span></span>
<span data-ttu-id="dcbb3-113">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag létrehoz egy runbook.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="dcbb3-114">-Leírás</span><span class="sxs-lookup"><span data-stu-id="dcbb3-114">-Description</span></span>
<span data-ttu-id="dcbb3-115">A runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-115">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="dcbb3-116">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="dcbb3-116">-LogProgress</span></span>
<span data-ttu-id="dcbb3-117">Meghatározza, hogy a runbook naplózása folyamatban van-e.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-117">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="dcbb3-118">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="dcbb3-118">-LogVerbose</span></span>
<span data-ttu-id="dcbb3-119">Meghatározza, hogy a naplózás tartalmaz-e részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-119">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="dcbb3-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dcbb3-120">-Name</span></span>
<span data-ttu-id="dcbb3-121">A runbook nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-121">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="dcbb3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcbb3-122">-ResourceGroupName</span></span>
<span data-ttu-id="dcbb3-123">Annak az erőforráscsoport a neve, amelyhez a parancsmag létrehoz egy runbook.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-123">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="dcbb3-124">-Címkék</span><span class="sxs-lookup"><span data-stu-id="dcbb3-124">-Tags</span></span>
<span data-ttu-id="dcbb3-125">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dcbb3-126">Példa:</span><span class="sxs-lookup"><span data-stu-id="dcbb3-126">For example:</span></span>

<span data-ttu-id="dcbb3-127">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="dcbb3-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="dcbb3-128">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="dcbb3-128">-Type</span></span>
<span data-ttu-id="dcbb3-129">A parancsmag által létrehozott runbook adja meg.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-129">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="dcbb3-130">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="dcbb3-130">Valid values are:</span></span>

- <span data-ttu-id="dcbb3-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="dcbb3-131">PowerShell</span></span>
- <span data-ttu-id="dcbb3-132">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="dcbb3-132">GraphicalPowerShell</span></span>
- <span data-ttu-id="dcbb3-133">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="dcbb3-133">PowerShellWorkflow</span></span>
- <span data-ttu-id="dcbb3-134">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="dcbb3-134">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="dcbb3-135">Graph</span><span class="sxs-lookup"><span data-stu-id="dcbb3-135">Graph</span></span>

<span data-ttu-id="dcbb3-136">Az érték gráf elavult.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-136">The value Graph is obsolete.</span></span>
<span data-ttu-id="dcbb3-137">Egyenértékű a GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="dcbb3-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcbb3-138">-DefaultProfile</span></span>
<span data-ttu-id="dcbb3-139">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dcbb3-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dcbb3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbb3-140">CommonParameters</span></span>
<span data-ttu-id="dcbb3-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dcbb3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbb3-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcbb3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbb3-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcbb3-143">INPUTS</span></span>

## <span data-ttu-id="dcbb3-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dcbb3-144">OUTPUTS</span></span>

### <span data-ttu-id="dcbb3-145">Microsoft. Azure. Command. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="dcbb3-145">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="dcbb3-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dcbb3-146">NOTES</span></span>

## <span data-ttu-id="dcbb3-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dcbb3-147">RELATED LINKS</span></span>

[<span data-ttu-id="dcbb3-148">Exportálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dcbb3-148">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dcbb3-149">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dcbb3-149">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dcbb3-150">Importálás – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dcbb3-150">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dcbb3-151">Közzététel – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dcbb3-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dcbb3-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dcbb3-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dcbb3-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dcbb3-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="dcbb3-154">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="dcbb3-154">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)
