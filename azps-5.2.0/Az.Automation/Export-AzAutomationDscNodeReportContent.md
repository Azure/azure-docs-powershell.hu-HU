---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: dd29a092ec0ca3b24614b363147d4c50bf14dcbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342474"
---
# <span data-ttu-id="cc232-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="cc232-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="cc232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc232-102">SYNOPSIS</span></span>
<span data-ttu-id="cc232-103">Egy DSC-csomópontról az Automatizálásba küldött DSC-jelentés nyers tartalmát exportálja.</span><span class="sxs-lookup"><span data-stu-id="cc232-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="cc232-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cc232-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc232-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cc232-105">DESCRIPTION</span></span>
<span data-ttu-id="cc232-106">Az **Export-AzAutomationDscNodeReportContent** parancsmag exportálja egy APS–kívánt állapotkonfigurációs (DSC) jelentés nyers tartalmát.</span><span class="sxs-lookup"><span data-stu-id="cc232-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="cc232-107">Egy DSC-csomópont DSC-jelentést küld az Azure Automation szolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="cc232-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="cc232-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cc232-108">EXAMPLES</span></span>

### <span data-ttu-id="cc232-109">1. példa: Jelentés exportálása DSC-csomópontból</span><span class="sxs-lookup"><span data-stu-id="cc232-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="cc232-110">Ez a parancskészlet exportálja a legújabb jelentést a Számítógép14 nevű DSC-csomópontból az asztalra.</span><span class="sxs-lookup"><span data-stu-id="cc232-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="cc232-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc232-111">PARAMETERS</span></span>

### <span data-ttu-id="cc232-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cc232-112">-AutomationAccountName</span></span>
<span data-ttu-id="cc232-113">Egy automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc232-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="cc232-114">Ez a parancsmag a paraméter által megadott Automatizálási fiókhoz tartozó DSC-csomópont jelentéstartalmait exportálja.</span><span class="sxs-lookup"><span data-stu-id="cc232-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="cc232-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc232-115">-DefaultProfile</span></span>
<span data-ttu-id="cc232-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="cc232-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc232-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cc232-117">-Force</span></span>
<span data-ttu-id="cc232-118">Azt jelzi, hogy ez a parancsmag lecserél egy meglévő helyi fájlt egy új, azonos nevű fájlra.</span><span class="sxs-lookup"><span data-stu-id="cc232-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc232-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="cc232-119">-NodeId</span></span>
<span data-ttu-id="cc232-120">Annak a DSC-csomópontnak az egyedi azonosítója, amelynek a parancsmagja exportálja a jelentés tartalmát.</span><span class="sxs-lookup"><span data-stu-id="cc232-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc232-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="cc232-121">-OutputFolder</span></span>
<span data-ttu-id="cc232-122">Azt a kimeneti mappát adja meg, amelybe a parancsmag exportálja a jelentés tartalmát.</span><span class="sxs-lookup"><span data-stu-id="cc232-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="cc232-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="cc232-123">-ReportId</span></span>
<span data-ttu-id="cc232-124">Az a DSC-csomópontjelentés egyedi azonosítója, amelyből a parancsmag exportálva van.</span><span class="sxs-lookup"><span data-stu-id="cc232-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc232-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc232-125">-ResourceGroupName</span></span>
<span data-ttu-id="cc232-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cc232-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cc232-127">Ez a parancsmag a parancsmag által megadott erőforráscsoporthoz tartozó DSC-csomópont jelentésének tartalmát exportálja.</span><span class="sxs-lookup"><span data-stu-id="cc232-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="cc232-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc232-128">-Confirm</span></span>
<span data-ttu-id="cc232-129">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="cc232-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc232-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc232-130">-WhatIf</span></span>
<span data-ttu-id="cc232-131">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="cc232-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc232-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cc232-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc232-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc232-133">CommonParameters</span></span>
<span data-ttu-id="cc232-134">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc232-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc232-135">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc232-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc232-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc232-136">INPUTS</span></span>

### <span data-ttu-id="cc232-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="cc232-137">System.Guid</span></span>

### <span data-ttu-id="cc232-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cc232-138">System.String</span></span>

## <span data-ttu-id="cc232-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cc232-139">OUTPUTS</span></span>

### <span data-ttu-id="cc232-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="cc232-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="cc232-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cc232-141">NOTES</span></span>

## <span data-ttu-id="cc232-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cc232-142">RELATED LINKS</span></span>

[<span data-ttu-id="cc232-143">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="cc232-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="cc232-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cc232-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="cc232-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="cc232-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


