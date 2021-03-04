---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: bb88bc38f6102f18b4d45b3b80902886975e2628
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936330"
---
# <span data-ttu-id="f83bd-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="f83bd-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="f83bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f83bd-102">SYNOPSIS</span></span>
<span data-ttu-id="f83bd-103">Egy DSC-csomópontról az Automatizálásnak küldött jelentéseket kap.</span><span class="sxs-lookup"><span data-stu-id="f83bd-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="f83bd-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f83bd-104">SYNTAX</span></span>

### <span data-ttu-id="f83bd-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f83bd-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f83bd-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="f83bd-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f83bd-107">ById</span><span class="sxs-lookup"><span data-stu-id="f83bd-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f83bd-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f83bd-108">DESCRIPTION</span></span>
<span data-ttu-id="f83bd-109">A **Get-AzAutomationDscNodeReport** parancsmag az APS kívánt államkonfigurációs (DSC) csomópontja által az Azure Automationnek küldött jelentéseket kapja.</span><span class="sxs-lookup"><span data-stu-id="f83bd-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="f83bd-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f83bd-110">EXAMPLES</span></span>

### <span data-ttu-id="f83bd-111">1. példa: A DSC-csomópontok összes jelentésének be szerezze</span><span class="sxs-lookup"><span data-stu-id="f83bd-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="f83bd-112">Az első parancs a Számítógép14 nevű számítógép DSC-csomópontját kapja meg a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="f83bd-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f83bd-113">A parancs ezt az objektumot a $Node tárolja.</span><span class="sxs-lookup"><span data-stu-id="f83bd-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="f83bd-114">A második parancs a Számítógép14 nevű DSC-csomópontról a Contoso17 nevű automatizálási fiókba küldött összes jelentés metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="f83bd-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="f83bd-115">A parancs a csomópontot  az objektum Id $Node határozza meg.</span><span class="sxs-lookup"><span data-stu-id="f83bd-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="f83bd-116">2. példa: DSC-csomópont jelentése jelentésazonosító alapján</span><span class="sxs-lookup"><span data-stu-id="f83bd-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="f83bd-117">Az első parancs a Számítógép14 nevű számítógép DSC-csomópontját kapja meg a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="f83bd-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f83bd-118">A parancs ezt az objektumot a $Node tárolja.</span><span class="sxs-lookup"><span data-stu-id="f83bd-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="f83bd-119">A második parancs a Számítógép14 nevű DSC-csomópontból a Contoso17 nevű automatizálási fiókba küldött megadott azonosítóval azonosított jelentés metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="f83bd-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f83bd-120">3. példa: A DSC-csomópontok legújabb jelentésének lekérte</span><span class="sxs-lookup"><span data-stu-id="f83bd-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="f83bd-121">Az első parancs a Számítógép14 nevű számítógép DSC-csomópontját kapja meg a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="f83bd-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="f83bd-122">A parancs ezt az objektumot a $Node tárolja.</span><span class="sxs-lookup"><span data-stu-id="f83bd-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="f83bd-123">A második parancs a Számítógép14 nevű DSC-csomópontról a Contoso17 nevű automatizálási fiókba küldött legújabb jelentés metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="f83bd-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f83bd-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f83bd-124">PARAMETERS</span></span>

### <span data-ttu-id="f83bd-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f83bd-125">-AutomationAccountName</span></span>
<span data-ttu-id="f83bd-126">Egy automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f83bd-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="f83bd-127">Ez a parancsmag a paraméter által megadott fiókhoz tartozó DSC-csomópont jelentéseit exportálja.</span><span class="sxs-lookup"><span data-stu-id="f83bd-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="f83bd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f83bd-128">-DefaultProfile</span></span>
<span data-ttu-id="f83bd-129">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f83bd-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f83bd-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="f83bd-130">-EndTime</span></span>
<span data-ttu-id="f83bd-131">A záró időpont megadása.</span><span class="sxs-lookup"><span data-stu-id="f83bd-131">Specifies an end time.</span></span>
<span data-ttu-id="f83bd-132">Ez a parancsmag olyan jelentéseket kap, amelyek szerint az automatizálás a jelen időpont előtt érkezett.</span><span class="sxs-lookup"><span data-stu-id="f83bd-132">This cmdlet gets reports that Automation received before this time.</span></span>

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

### <span data-ttu-id="f83bd-133">-Id</span><span class="sxs-lookup"><span data-stu-id="f83bd-133">-Id</span></span>
<span data-ttu-id="f83bd-134">A lekért parancsmag DSC-csomópontjelentésének egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f83bd-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

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

### <span data-ttu-id="f83bd-135">-Latest</span><span class="sxs-lookup"><span data-stu-id="f83bd-135">-Latest</span></span>
<span data-ttu-id="f83bd-136">Azt jelzi, hogy ez a parancsmag csak a megadott csomópont legújabb DSC-jelentését kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f83bd-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

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

### <span data-ttu-id="f83bd-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="f83bd-137">-NodeId</span></span>
<span data-ttu-id="f83bd-138">Annak a DSC-csomópontnak az egyedi azonosítója, amelyhez a parancsmag jelentéseket kap.</span><span class="sxs-lookup"><span data-stu-id="f83bd-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="f83bd-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f83bd-139">-ResourceGroupName</span></span>
<span data-ttu-id="f83bd-140">Annak az erőforráscsoportnak a nevét adja meg, amely tartalmazza azt a DSC-csomópontot, amelyhez a parancsmag jelentéseket kap.</span><span class="sxs-lookup"><span data-stu-id="f83bd-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="f83bd-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f83bd-141">-StartTime</span></span>
<span data-ttu-id="f83bd-142">Megadja a kezdési időt.</span><span class="sxs-lookup"><span data-stu-id="f83bd-142">Specifies a start time.</span></span>
<span data-ttu-id="f83bd-143">Ez a parancsmag olyan jelentéseket kap, amelyek szerint az automatizálás ezt követően érkezett.</span><span class="sxs-lookup"><span data-stu-id="f83bd-143">This cmdlet gets reports that Automation received after this time.</span></span>

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

### <span data-ttu-id="f83bd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f83bd-144">CommonParameters</span></span>
<span data-ttu-id="f83bd-145">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f83bd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f83bd-146">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f83bd-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f83bd-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f83bd-147">INPUTS</span></span>

### <span data-ttu-id="f83bd-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f83bd-148">System.Guid</span></span>

### <span data-ttu-id="f83bd-149">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f83bd-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f83bd-150">System.String</span><span class="sxs-lookup"><span data-stu-id="f83bd-150">System.String</span></span>

## <span data-ttu-id="f83bd-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f83bd-151">OUTPUTS</span></span>

### <span data-ttu-id="f83bd-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="f83bd-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="f83bd-153">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f83bd-153">NOTES</span></span>

## <span data-ttu-id="f83bd-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f83bd-154">RELATED LINKS</span></span>

[<span data-ttu-id="f83bd-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f83bd-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="f83bd-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="f83bd-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


