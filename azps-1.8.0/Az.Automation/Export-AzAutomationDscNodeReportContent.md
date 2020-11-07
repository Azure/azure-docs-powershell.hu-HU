---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscNodeReportContent.md
ms.openlocfilehash: 6d9abefee1f787ea26f7f10b106900af0be31d3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671642"
---
# <span data-ttu-id="bb8d5-101">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="bb8d5-101">Export-AzAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="bb8d5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bb8d5-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8d5-103">Egy DSC-csomópontról az automatizálásra küldött DSC-jelentés nyers tartalmát exportálja.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="bb8d5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bb8d5-104">SYNTAX</span></span>

```
Export-AzAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb8d5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bb8d5-105">DESCRIPTION</span></span>
<span data-ttu-id="bb8d5-106">Az **export-AzAutomationDscNodeReportContent** parancsmag exportálja egy APS-alapú, a megfelelő állapotú (DSC) jelentés nyers tartalmát.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-106">The **Export-AzAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="bb8d5-107">A DSC-csomópontok DSC-jelentést küldenek az Azure automatizálási szolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="bb8d5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="bb8d5-108">EXAMPLES</span></span>

### <span data-ttu-id="bb8d5-109">1. példa: jelentés exportálása DSC-csomópontról</span><span class="sxs-lookup"><span data-stu-id="bb8d5-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="bb8d5-110">Ezek a parancsok a Computer14 az asztalra nevű DSC csomópontról exportálják a legújabb jelentést.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="bb8d5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bb8d5-111">PARAMETERS</span></span>

### <span data-ttu-id="bb8d5-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bb8d5-112">-AutomationAccountName</span></span>
<span data-ttu-id="bb8d5-113">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="bb8d5-114">Ez a parancsmag exportálja a jelentés tartalmát egy olyan DSC-csomópontra, amely a paraméter által megadott automatizálási fiókhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="bb8d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8d5-115">-DefaultProfile</span></span>
<span data-ttu-id="bb8d5-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bb8d5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bb8d5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bb8d5-117">-Force</span></span>
<span data-ttu-id="bb8d5-118">Azt jelzi, hogy ez a parancsmag egy meglévő helyi fájlt cserél le egy új, azonos nevű fájllal.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="bb8d5-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="bb8d5-119">-NodeId</span></span>
<span data-ttu-id="bb8d5-120">Annak a DSC-csomópontnak az egyedi azonosítója, amelyhez ez a parancsmag exportálja a jelentés tartalmát.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="bb8d5-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="bb8d5-121">-OutputFolder</span></span>
<span data-ttu-id="bb8d5-122">Azt a kimeneti mappát adja meg, ahol ez a parancsmag exportálja a jelentés tartalmát.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="bb8d5-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="bb8d5-123">-ReportId</span></span>
<span data-ttu-id="bb8d5-124">A parancsmag által exportált DSC csomópont-jelentés egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="bb8d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb8d5-125">-ResourceGroupName</span></span>
<span data-ttu-id="bb8d5-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="bb8d5-127">Ez a parancsmag olyan jelentés tartalmát exportálja a DSC-csomóponthoz, amely a parancsmag által megadott erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="bb8d5-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bb8d5-128">-Confirm</span></span>
<span data-ttu-id="bb8d5-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb8d5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb8d5-130">-WhatIf</span></span>
<span data-ttu-id="bb8d5-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb8d5-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bb8d5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb8d5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8d5-133">CommonParameters</span></span>
<span data-ttu-id="bb8d5-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bb8d5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8d5-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb8d5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8d5-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb8d5-136">INPUTS</span></span>

### <span data-ttu-id="bb8d5-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="bb8d5-137">System.Guid</span></span>

### <span data-ttu-id="bb8d5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bb8d5-138">System.String</span></span>

## <span data-ttu-id="bb8d5-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bb8d5-139">OUTPUTS</span></span>

### <span data-ttu-id="bb8d5-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="bb8d5-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="bb8d5-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bb8d5-141">NOTES</span></span>

## <span data-ttu-id="bb8d5-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bb8d5-142">RELATED LINKS</span></span>

[<span data-ttu-id="bb8d5-143">Exportálás – AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="bb8d5-143">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)

[<span data-ttu-id="bb8d5-144">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="bb8d5-144">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="bb8d5-145">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="bb8d5-145">Get-AzAutomationDscNodeReport</span></span>](./Get-AzAutomationDscNodeReport.md)


