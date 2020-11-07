---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 4dd1eee278adcced1dbace9a30e88b5767037746
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667733"
---
# <span data-ttu-id="fc43d-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fc43d-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="fc43d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fc43d-102">SYNOPSIS</span></span>
<span data-ttu-id="fc43d-103">Módosítja a runbook.</span><span class="sxs-lookup"><span data-stu-id="fc43d-103">Modifies a runbook.</span></span>

## <span data-ttu-id="fc43d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fc43d-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc43d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fc43d-105">DESCRIPTION</span></span>
<span data-ttu-id="fc43d-106">A **set-AzAutomationRunbook** parancsmag az Azure automatizálási runbook konfigurációját módosítja az APS-ben.</span><span class="sxs-lookup"><span data-stu-id="fc43d-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="fc43d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fc43d-107">EXAMPLES</span></span>

### <span data-ttu-id="fc43d-108">Példa 1: a runbook részletes naplózásának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="fc43d-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fc43d-109">Ez a parancs lehetővé teszi a részletes naplózást a megadott runbook az Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="fc43d-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="fc43d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fc43d-110">PARAMETERS</span></span>

### <span data-ttu-id="fc43d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fc43d-111">-AutomationAccountName</span></span>
<span data-ttu-id="fc43d-112">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag módosította a runbook.</span><span class="sxs-lookup"><span data-stu-id="fc43d-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="fc43d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc43d-113">-DefaultProfile</span></span>
<span data-ttu-id="fc43d-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fc43d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc43d-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="fc43d-115">-Description</span></span>
<span data-ttu-id="fc43d-116">A runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc43d-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="fc43d-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="fc43d-117">-LogProgress</span></span>
<span data-ttu-id="fc43d-118">Meghatározza, hogy a runbook naplózása folyamatban van-e.</span><span class="sxs-lookup"><span data-stu-id="fc43d-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="fc43d-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="fc43d-119">-LogVerbose</span></span>
<span data-ttu-id="fc43d-120">Meghatározza, hogy a naplózás tartalmaz-e részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="fc43d-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="fc43d-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fc43d-121">-Name</span></span>
<span data-ttu-id="fc43d-122">Annak a runbook a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="fc43d-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fc43d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc43d-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc43d-124">Annak az erőforráscsoport a neve, amelyhez a parancsmag módosított egy runbook.</span><span class="sxs-lookup"><span data-stu-id="fc43d-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="fc43d-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="fc43d-125">-Tag</span></span>
<span data-ttu-id="fc43d-126">A runbook címkék.</span><span class="sxs-lookup"><span data-stu-id="fc43d-126">The runbook tags.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc43d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc43d-127">CommonParameters</span></span>
<span data-ttu-id="fc43d-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fc43d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc43d-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc43d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc43d-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc43d-130">INPUTS</span></span>

### <span data-ttu-id="fc43d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fc43d-131">System.String</span></span>

### <span data-ttu-id="fc43d-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="fc43d-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="fc43d-133">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fc43d-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fc43d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc43d-134">OUTPUTS</span></span>

### <span data-ttu-id="fc43d-135">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="fc43d-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="fc43d-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fc43d-136">NOTES</span></span>

## <span data-ttu-id="fc43d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc43d-137">RELATED LINKS</span></span>

[<span data-ttu-id="fc43d-138">Exportálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fc43d-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="fc43d-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fc43d-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="fc43d-140">Importálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fc43d-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="fc43d-141">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fc43d-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="fc43d-142">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fc43d-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="fc43d-143">Közzététel – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fc43d-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="fc43d-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fc43d-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="fc43d-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fc43d-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


