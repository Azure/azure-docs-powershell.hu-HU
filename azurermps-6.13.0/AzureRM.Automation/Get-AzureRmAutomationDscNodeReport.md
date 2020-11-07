---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: 747ffdb9df955609a38718016af50bb5434c0224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679203"
---
# <span data-ttu-id="1de52-101">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="1de52-101">Get-AzureRmAutomationDscNodeReport</span></span>

## <span data-ttu-id="1de52-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1de52-102">SYNOPSIS</span></span>
<span data-ttu-id="1de52-103">A DSC csomópontról az automatizálásra küldött jelentéseket kapja.</span><span class="sxs-lookup"><span data-stu-id="1de52-103">Gets reports sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1de52-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1de52-104">SYNTAX</span></span>

### <span data-ttu-id="1de52-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1de52-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1de52-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="1de52-106">ByLatest</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1de52-107">ById</span><span class="sxs-lookup"><span data-stu-id="1de52-107">ById</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1de52-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="1de52-108">DESCRIPTION</span></span>
<span data-ttu-id="1de52-109">A **Get-AzureRmAutomationDscNodeReport** PARANCSMAG az APS-nek megfelelő állapotú (DSC) csomópontról az Azure automatizálásra küldött jelentéseket kapja.</span><span class="sxs-lookup"><span data-stu-id="1de52-109">The **Get-AzureRmAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="1de52-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1de52-110">EXAMPLES</span></span>

### <span data-ttu-id="1de52-111">Példa 1: a DSC-csomópont minden jelentésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="1de52-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="1de52-112">Az első parancs a Computer14 nevű számítógép DSC csomópontját kapja a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="1de52-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="1de52-113">A parancs az objektumot a $Node változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1de52-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="1de52-114">A második parancs a Computer14 nevű DSC csomópontról a Contoso17 nevű automatizálási fiókba küldött összes jelentés metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="1de52-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="1de52-115">A parancs a csomópontot a $Node objektum **ID** tulajdonságával határozza meg.</span><span class="sxs-lookup"><span data-stu-id="1de52-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="1de52-116">2. példa: jelentés kérése DSC-csomóponthoz jelentés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="1de52-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="1de52-117">Az első parancs a Computer14 nevű számítógép DSC csomópontját kapja a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="1de52-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="1de52-118">A parancs az objektumot a $Node változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1de52-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="1de52-119">A második parancs a Computer14 nevű DSC csomóponttól a Contoso17 nevű automatizálási fiókhoz küldött megadott azonosító által azonosított jelentés metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="1de52-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1de52-120">3. példa: a legújabb jelentés beszerzése DSC-csomópontról</span><span class="sxs-lookup"><span data-stu-id="1de52-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="1de52-121">Az első parancs a Computer14 nevű számítógép DSC csomópontját kapja a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="1de52-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="1de52-122">A parancs az objektumot a $Node változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="1de52-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="1de52-123">A második parancs a Computer14 nevű DSC csomóponttól a Contoso17 nevű automatizálási fiókba küldött legutóbbi jelentés metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="1de52-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1de52-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1de52-124">PARAMETERS</span></span>

### <span data-ttu-id="1de52-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1de52-125">-AutomationAccountName</span></span>
<span data-ttu-id="1de52-126">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1de52-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="1de52-127">Ez a parancsmag olyan DSC csomópontokra exportál jelentéseket, amelyek a paraméter által megadott fiókba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="1de52-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="1de52-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de52-128">-DefaultProfile</span></span>
<span data-ttu-id="1de52-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="1de52-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1de52-130">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="1de52-130">-EndTime</span></span>
<span data-ttu-id="1de52-131">A befejezési időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="1de52-131">Specifies an end time.</span></span>
<span data-ttu-id="1de52-132">Ez a parancsmag jelentést kap, amely az adott időpont előtt kapott automatizálást.</span><span class="sxs-lookup"><span data-stu-id="1de52-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de52-133">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="1de52-133">-Id</span></span>
<span data-ttu-id="1de52-134">Itt adhatja meg az ehhez a parancsmaghoz készült DSC Node jelentés egyedi AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="1de52-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de52-135">-Legújabb</span><span class="sxs-lookup"><span data-stu-id="1de52-135">-Latest</span></span>
<span data-ttu-id="1de52-136">Jelzi, hogy ez a parancsmag csak a megadott csomópont legújabb DSC-jelentését kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1de52-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1de52-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="1de52-137">-NodeId</span></span>
<span data-ttu-id="1de52-138">Annak a DSC-csomópontnak az egyedi azonosítója, amelyhez a parancsmag jelentést kap.</span><span class="sxs-lookup"><span data-stu-id="1de52-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="1de52-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1de52-139">-ResourceGroupName</span></span>
<span data-ttu-id="1de52-140">Annak a DSC-csomópontnak a neve, amelyhez a parancsmag jelentést kap.</span><span class="sxs-lookup"><span data-stu-id="1de52-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="1de52-141">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="1de52-141">-StartTime</span></span>
<span data-ttu-id="1de52-142">Megadja a kezdés időpontját.</span><span class="sxs-lookup"><span data-stu-id="1de52-142">Specifies a start time.</span></span>
<span data-ttu-id="1de52-143">Ez a parancsmag jelentéseket kap, amelyeket az automatizálás után kapott.</span><span class="sxs-lookup"><span data-stu-id="1de52-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1de52-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de52-144">CommonParameters</span></span>
<span data-ttu-id="1de52-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1de52-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de52-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1de52-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de52-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1de52-147">INPUTS</span></span>

### <span data-ttu-id="1de52-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="1de52-148">System.Guid</span></span>

### <span data-ttu-id="1de52-149">System. null ' 1 [[System. DateTimeOffset, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1de52-149">System.Nullable\`1[[System.DateTimeOffset, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1de52-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1de52-150">System.String</span></span>

## <span data-ttu-id="1de52-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1de52-151">OUTPUTS</span></span>

### <span data-ttu-id="1de52-152">Microsoft. Azure. Command. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="1de52-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="1de52-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1de52-153">NOTES</span></span>

## <span data-ttu-id="1de52-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1de52-154">RELATED LINKS</span></span>

[<span data-ttu-id="1de52-155">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="1de52-155">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="1de52-156">Exportálás – AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="1de52-156">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)


