---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationdscnodereportcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
ms.openlocfilehash: 52ed2c5925758a4d40fdf39dcdadf73eb2fc53b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492052"
---
# <span data-ttu-id="e0ab8-101">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="e0ab8-101">Export-AzureRmAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="e0ab8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e0ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ab8-103">Egy DSC-csomópontról az automatizálásra küldött DSC-jelentés nyers tartalmát exportálja.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0ab8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e0ab8-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0ab8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e0ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="e0ab8-106">Az **export-AzureRmAutomationDscNodeReportContent** parancsmag exportálja egy APS-alapú, a megfelelő állapotú (DSC) jelentés nyers tartalmát.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-106">The **Export-AzureRmAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="e0ab8-107">A DSC-csomópontok DSC-jelentést küldenek az Azure automatizálási szolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="e0ab8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e0ab8-108">EXAMPLES</span></span>

### <span data-ttu-id="e0ab8-109">1. példa: jelentés exportálása DSC-csomópontról</span><span class="sxs-lookup"><span data-stu-id="e0ab8-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzureRmAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="e0ab8-110">Ezek a parancsok a Computer14 az asztalra nevű DSC csomópontról exportálják a legújabb jelentést.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="e0ab8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e0ab8-111">PARAMETERS</span></span>

### <span data-ttu-id="e0ab8-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e0ab8-112">-AutomationAccountName</span></span>
<span data-ttu-id="e0ab8-113">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="e0ab8-114">Ez a parancsmag exportálja a jelentés tartalmát egy olyan DSC-csomópontra, amely a paraméter által megadott automatizálási fiókhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="e0ab8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ab8-115">-DefaultProfile</span></span>
<span data-ttu-id="e0ab8-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e0ab8-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0ab8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e0ab8-117">-Force</span></span>
<span data-ttu-id="e0ab8-118">Azt jelzi, hogy ez a parancsmag egy meglévő helyi fájlt cserél le egy új, azonos nevű fájllal.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-118">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="e0ab8-119">-NodeId</span><span class="sxs-lookup"><span data-stu-id="e0ab8-119">-NodeId</span></span>
<span data-ttu-id="e0ab8-120">Annak a DSC-csomópontnak az egyedi azonosítója, amelyhez ez a parancsmag exportálja a jelentés tartalmát.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-120">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="e0ab8-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="e0ab8-121">-OutputFolder</span></span>
<span data-ttu-id="e0ab8-122">Azt a kimeneti mappát adja meg, ahol ez a parancsmag exportálja a jelentés tartalmát.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-122">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="e0ab8-123">-ReportId</span><span class="sxs-lookup"><span data-stu-id="e0ab8-123">-ReportId</span></span>
<span data-ttu-id="e0ab8-124">A parancsmag által exportált DSC csomópont-jelentés egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-124">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="e0ab8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ab8-125">-ResourceGroupName</span></span>
<span data-ttu-id="e0ab8-126">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="e0ab8-127">Ez a parancsmag olyan jelentés tartalmát exportálja a DSC-csomóponthoz, amely a parancsmag által megadott erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-127">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="e0ab8-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e0ab8-128">-Confirm</span></span>
<span data-ttu-id="e0ab8-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0ab8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0ab8-130">-WhatIf</span></span>
<span data-ttu-id="e0ab8-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0ab8-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e0ab8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0ab8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ab8-133">CommonParameters</span></span>
<span data-ttu-id="e0ab8-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e0ab8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ab8-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0ab8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ab8-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0ab8-136">INPUTS</span></span>

### <span data-ttu-id="e0ab8-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e0ab8-137">System.Guid</span></span>

### <span data-ttu-id="e0ab8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e0ab8-138">System.String</span></span>

## <span data-ttu-id="e0ab8-139">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e0ab8-139">OUTPUTS</span></span>

### <span data-ttu-id="e0ab8-140">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="e0ab8-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="e0ab8-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e0ab8-141">NOTES</span></span>

## <span data-ttu-id="e0ab8-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e0ab8-142">RELATED LINKS</span></span>

[<span data-ttu-id="e0ab8-143">Exportálás – AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="e0ab8-143">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)

[<span data-ttu-id="e0ab8-144">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="e0ab8-144">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="e0ab8-145">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="e0ab8-145">Get-AzureRmAutomationDscNodeReport</span></span>](./Get-AzureRmAutomationDscNodeReport.md)


