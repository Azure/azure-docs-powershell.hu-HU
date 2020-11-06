---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 4285EF77-FA70-4BE7-96E0-89E2E8FC5AD6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscNodeReportContent.md
ms.openlocfilehash: 23c17a0614a28a571b58e19ff2556c45679e6c82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498011"
---
# <span data-ttu-id="4df82-101">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="4df82-101">Export-AzureRmAutomationDscNodeReportContent</span></span>

## <span data-ttu-id="4df82-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4df82-102">SYNOPSIS</span></span>
<span data-ttu-id="4df82-103">Egy DSC-csomópontról az automatizálásra küldött DSC-jelentés nyers tartalmát exportálja.</span><span class="sxs-lookup"><span data-stu-id="4df82-103">Exports the raw content of a DSC report sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4df82-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4df82-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscNodeReportContent -NodeId <Guid> -ReportId <Guid> [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4df82-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4df82-105">DESCRIPTION</span></span>
<span data-ttu-id="4df82-106">Az **export-AzureRmAutomationDscNodeReportContent** parancsmag exportálja egy APS-alapú, a megfelelő állapotú (DSC) jelentés nyers tartalmát.</span><span class="sxs-lookup"><span data-stu-id="4df82-106">The **Export-AzureRmAutomationDscNodeReportContent** cmdlet exports the raw contents of an APS Desired State Configuration (DSC) report.</span></span>
<span data-ttu-id="4df82-107">A DSC-csomópontok DSC-jelentést küldenek az Azure automatizálási szolgáltatásnak.</span><span class="sxs-lookup"><span data-stu-id="4df82-107">A DSC node sends a DSC report to Azure Automation.</span></span>

## <span data-ttu-id="4df82-108">Példák</span><span class="sxs-lookup"><span data-stu-id="4df82-108">EXAMPLES</span></span>

### <span data-ttu-id="4df82-109">1. példa: jelentés exportálása DSC-csomópontról</span><span class="sxs-lookup"><span data-stu-id="4df82-109">Example 1: Export a report from a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "AutomationAccount01" -Name "Computer14"
PS C:\> $Report = Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "ContosoAutomationAccount" -NodeId $Node.Id -Latest
PS C:\> $Report | Export-AzureRmAutomationDscNodeReportContent -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="4df82-110">Ezek a parancsok a Computer14 az asztalra nevű DSC csomópontról exportálják a legújabb jelentést.</span><span class="sxs-lookup"><span data-stu-id="4df82-110">This set of commands exports the latest report from the DSC node named Computer14 to the desktop.</span></span>

## <span data-ttu-id="4df82-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4df82-111">PARAMETERS</span></span>

### <span data-ttu-id="4df82-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4df82-112">-AutomationAccountName</span></span>
<span data-ttu-id="4df82-113">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4df82-113">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="4df82-114">Ez a parancsmag exportálja a jelentés tartalmát egy olyan DSC-csomópontra, amely a paraméter által megadott automatizálási fiókhoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="4df82-114">This cmdlet exports report content for a DSC node that belongs to the Automation account that this parameter specifies.</span></span>

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

### <span data-ttu-id="4df82-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4df82-115">-Force</span></span>
<span data-ttu-id="4df82-116">Azt jelzi, hogy ez a parancsmag egy meglévő helyi fájlt cserél le egy új, azonos nevű fájllal.</span><span class="sxs-lookup"><span data-stu-id="4df82-116">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="4df82-117">-NodeId</span><span class="sxs-lookup"><span data-stu-id="4df82-117">-NodeId</span></span>
<span data-ttu-id="4df82-118">Annak a DSC-csomópontnak az egyedi azonosítója, amelyhez ez a parancsmag exportálja a jelentés tartalmát.</span><span class="sxs-lookup"><span data-stu-id="4df82-118">Specifies the unique ID of the DSC node for which this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="4df82-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="4df82-119">-OutputFolder</span></span>
<span data-ttu-id="4df82-120">Azt a kimeneti mappát adja meg, ahol ez a parancsmag exportálja a jelentés tartalmát.</span><span class="sxs-lookup"><span data-stu-id="4df82-120">Specifies the output folder where this cmdlet exports report contents.</span></span>

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

### <span data-ttu-id="4df82-121">-ReportId</span><span class="sxs-lookup"><span data-stu-id="4df82-121">-ReportId</span></span>
<span data-ttu-id="4df82-122">A parancsmag által exportált DSC csomópont-jelentés egyedi AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4df82-122">Specifies the unique ID of the DSC node report that this cmdlet exports.</span></span>

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

### <span data-ttu-id="4df82-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df82-123">-ResourceGroupName</span></span>
<span data-ttu-id="4df82-124">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4df82-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4df82-125">Ez a parancsmag olyan jelentés tartalmát exportálja a DSC-csomóponthoz, amely a parancsmag által megadott erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="4df82-125">This cmdlet exports the contents of a report for the DSC node that belongs to the resource group that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="4df82-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4df82-126">-Confirm</span></span>
<span data-ttu-id="4df82-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4df82-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4df82-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4df82-128">-WhatIf</span></span>
<span data-ttu-id="4df82-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4df82-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4df82-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4df82-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4df82-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df82-131">-DefaultProfile</span></span>
<span data-ttu-id="4df82-132">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4df82-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4df82-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df82-133">CommonParameters</span></span>
<span data-ttu-id="4df82-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4df82-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df82-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4df82-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df82-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4df82-136">INPUTS</span></span>

## <span data-ttu-id="4df82-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4df82-137">OUTPUTS</span></span>

### <span data-ttu-id="4df82-138">System. IO. DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="4df82-138">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="4df82-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4df82-139">NOTES</span></span>

## <span data-ttu-id="4df82-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4df82-140">RELATED LINKS</span></span>

[<span data-ttu-id="4df82-141">Exportálás – AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="4df82-141">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)

[<span data-ttu-id="4df82-142">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4df82-142">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="4df82-143">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="4df82-143">Get-AzureRmAutomationDscNodeReport</span></span>](./Get-AzureRmAutomationDscNodeReport.md)


