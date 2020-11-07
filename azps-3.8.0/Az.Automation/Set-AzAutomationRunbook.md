---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847354"
---
# <span data-ttu-id="79f4a-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79f4a-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="79f4a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="79f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="79f4a-103">Módosítja a runbook.</span><span class="sxs-lookup"><span data-stu-id="79f4a-103">Modifies a runbook.</span></span>

## <span data-ttu-id="79f4a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="79f4a-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79f4a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="79f4a-105">DESCRIPTION</span></span>
<span data-ttu-id="79f4a-106">A **set-AzAutomationRunbook** parancsmag az Azure automatizálási runbook konfigurációját módosítja az APS-ben.</span><span class="sxs-lookup"><span data-stu-id="79f4a-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="79f4a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="79f4a-107">EXAMPLES</span></span>

### <span data-ttu-id="79f4a-108">Példa 1: a runbook részletes naplózásának engedélyezése</span><span class="sxs-lookup"><span data-stu-id="79f4a-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="79f4a-109">Ez a parancs lehetővé teszi a részletes naplózást a megadott runbook az Contoso17 nevű Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="79f4a-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="79f4a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="79f4a-110">PARAMETERS</span></span>

### <span data-ttu-id="79f4a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="79f4a-111">-AutomationAccountName</span></span>
<span data-ttu-id="79f4a-112">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag módosította a runbook.</span><span class="sxs-lookup"><span data-stu-id="79f4a-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="79f4a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f4a-113">-DefaultProfile</span></span>
<span data-ttu-id="79f4a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="79f4a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79f4a-115">-Leírás</span><span class="sxs-lookup"><span data-stu-id="79f4a-115">-Description</span></span>
<span data-ttu-id="79f4a-116">A runbook leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="79f4a-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="79f4a-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="79f4a-117">-LogProgress</span></span>
<span data-ttu-id="79f4a-118">Meghatározza, hogy a runbook naplózása folyamatban van-e.</span><span class="sxs-lookup"><span data-stu-id="79f4a-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="79f4a-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="79f4a-119">-LogVerbose</span></span>
<span data-ttu-id="79f4a-120">Meghatározza, hogy a naplózás tartalmaz-e részletes információkat.</span><span class="sxs-lookup"><span data-stu-id="79f4a-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="79f4a-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="79f4a-121">-Name</span></span>
<span data-ttu-id="79f4a-122">Annak a runbook a nevét adja meg, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="79f4a-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="79f4a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79f4a-123">-ResourceGroupName</span></span>
<span data-ttu-id="79f4a-124">Annak az erőforráscsoport a neve, amelyhez a parancsmag módosított egy runbook.</span><span class="sxs-lookup"><span data-stu-id="79f4a-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="79f4a-125">-Címke</span><span class="sxs-lookup"><span data-stu-id="79f4a-125">-Tag</span></span>
<span data-ttu-id="79f4a-126">A runbook címkék.</span><span class="sxs-lookup"><span data-stu-id="79f4a-126">The runbook tags.</span></span>

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

### <span data-ttu-id="79f4a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f4a-127">CommonParameters</span></span>
<span data-ttu-id="79f4a-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="79f4a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f4a-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f4a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f4a-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="79f4a-130">INPUTS</span></span>

### <span data-ttu-id="79f4a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="79f4a-131">System.String</span></span>

### <span data-ttu-id="79f4a-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="79f4a-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="79f4a-133">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="79f4a-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="79f4a-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="79f4a-134">OUTPUTS</span></span>

### <span data-ttu-id="79f4a-135">Microsoft. Azure. Command. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="79f4a-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="79f4a-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="79f4a-136">NOTES</span></span>

## <span data-ttu-id="79f4a-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="79f4a-137">RELATED LINKS</span></span>

[<span data-ttu-id="79f4a-138">Exportálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79f4a-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="79f4a-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79f4a-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="79f4a-140">Importálás – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79f4a-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="79f4a-141">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79f4a-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="79f4a-142">Új – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79f4a-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="79f4a-143">Közzététel – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79f4a-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="79f4a-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79f4a-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="79f4a-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="79f4a-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


