---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: f71aef989a26ec5998ee8fd059446a2b05c2e4b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680823"
---
# <span data-ttu-id="a7b85-101">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="a7b85-101">Get-AzureRmAutomationDscNodeReport</span></span>

## <span data-ttu-id="a7b85-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7b85-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b85-103">A DSC csomópontról az automatizálásra küldött jelentéseket kapja.</span><span class="sxs-lookup"><span data-stu-id="a7b85-103">Gets reports sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7b85-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7b85-104">SYNTAX</span></span>

### <span data-ttu-id="a7b85-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a7b85-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7b85-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="a7b85-106">ByLatest</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7b85-107">ById</span><span class="sxs-lookup"><span data-stu-id="a7b85-107">ById</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7b85-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7b85-108">DESCRIPTION</span></span>
<span data-ttu-id="a7b85-109">A **Get-AzureRmAutomationDscNodeReport** PARANCSMAG az APS-nek megfelelő állapotú (DSC) csomópontról az Azure automatizálásra küldött jelentéseket kapja.</span><span class="sxs-lookup"><span data-stu-id="a7b85-109">The **Get-AzureRmAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="a7b85-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a7b85-110">EXAMPLES</span></span>

### <span data-ttu-id="a7b85-111">Példa 1: a DSC-csomópont minden jelentésének beolvasása</span><span class="sxs-lookup"><span data-stu-id="a7b85-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="a7b85-112">Az első parancs a Computer14 nevű számítógép DSC csomópontját kapja a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="a7b85-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="a7b85-113">A parancs az objektumot a $Node változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a7b85-113">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="a7b85-114">A második parancs a Computer14 nevű DSC csomópontról a Contoso17 nevű automatizálási fiókba küldött összes jelentés metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="a7b85-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="a7b85-115">A parancs a csomópontot a $Node objektum **ID** tulajdonságával határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a7b85-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="a7b85-116">2. példa: jelentés kérése DSC-csomóponthoz jelentés-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="a7b85-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="a7b85-117">Az első parancs a Computer14 nevű számítógép DSC csomópontját kapja a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="a7b85-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="a7b85-118">A parancs az objektumot a $Node változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a7b85-118">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="a7b85-119">A második parancs a Computer14 nevű DSC csomóponttól a Contoso17 nevű automatizálási fiókhoz küldött megadott azonosító által azonosított jelentés metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="a7b85-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a7b85-120">3. példa: a legújabb jelentés beszerzése DSC-csomópontról</span><span class="sxs-lookup"><span data-stu-id="a7b85-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="a7b85-121">Az első parancs a Computer14 nevű számítógép DSC csomópontját kapja a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="a7b85-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="a7b85-122">A parancs az objektumot a $Node változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="a7b85-122">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="a7b85-123">A második parancs a Computer14 nevű DSC csomóponttól a Contoso17 nevű automatizálási fiókba küldött legutóbbi jelentés metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="a7b85-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a7b85-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7b85-124">PARAMETERS</span></span>

### <span data-ttu-id="a7b85-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a7b85-125">-AutomationAccountName</span></span>
<span data-ttu-id="a7b85-126">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7b85-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="a7b85-127">Ez a parancsmag olyan DSC csomópontokra exportál jelentéseket, amelyek a paraméter által megadott fiókba tartoznak.</span><span class="sxs-lookup"><span data-stu-id="a7b85-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b85-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b85-128">-DefaultProfile</span></span>
<span data-ttu-id="a7b85-129">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a7b85-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b85-130">-A befejezési időpont</span><span class="sxs-lookup"><span data-stu-id="a7b85-130">-EndTime</span></span>
<span data-ttu-id="a7b85-131">A befejezési időpontot adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7b85-131">Specifies an end time.</span></span>
<span data-ttu-id="a7b85-132">Ez a parancsmag jelentést kap, amely az adott időpont előtt kapott automatizálást.</span><span class="sxs-lookup"><span data-stu-id="a7b85-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b85-133">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="a7b85-133">-Id</span></span>
<span data-ttu-id="a7b85-134">Itt adhatja meg az ehhez a parancsmaghoz készült DSC Node jelentés egyedi AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="a7b85-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b85-135">-Legújabb</span><span class="sxs-lookup"><span data-stu-id="a7b85-135">-Latest</span></span>
<span data-ttu-id="a7b85-136">Jelzi, hogy ez a parancsmag csak a megadott csomópont legújabb DSC-jelentését kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a7b85-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByLatest
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b85-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="a7b85-137">-NodeId</span></span>
<span data-ttu-id="a7b85-138">Annak a DSC-csomópontnak az egyedi azonosítója, amelyhez a parancsmag jelentést kap.</span><span class="sxs-lookup"><span data-stu-id="a7b85-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b85-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7b85-139">-ResourceGroupName</span></span>
<span data-ttu-id="a7b85-140">Annak a DSC-csomópontnak a neve, amelyhez a parancsmag jelentést kap.</span><span class="sxs-lookup"><span data-stu-id="a7b85-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b85-141">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="a7b85-141">-StartTime</span></span>
<span data-ttu-id="a7b85-142">Megadja a kezdés időpontját.</span><span class="sxs-lookup"><span data-stu-id="a7b85-142">Specifies a start time.</span></span>
<span data-ttu-id="a7b85-143">Ez a parancsmag jelentéseket kap, amelyeket az automatizálás után kapott.</span><span class="sxs-lookup"><span data-stu-id="a7b85-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7b85-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b85-144">CommonParameters</span></span>
<span data-ttu-id="a7b85-145">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7b85-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b85-146">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7b85-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b85-147">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7b85-147">INPUTS</span></span>

### <span data-ttu-id="a7b85-148">Nincs</span><span class="sxs-lookup"><span data-stu-id="a7b85-148">None</span></span>
<span data-ttu-id="a7b85-149">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="a7b85-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a7b85-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7b85-150">OUTPUTS</span></span>

### <span data-ttu-id="a7b85-151">Microsoft. Azure. Command. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="a7b85-151">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="a7b85-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7b85-152">NOTES</span></span>

## <span data-ttu-id="a7b85-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7b85-153">RELATED LINKS</span></span>

[<span data-ttu-id="a7b85-154">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a7b85-154">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="a7b85-155">Exportálás – AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="a7b85-155">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)


