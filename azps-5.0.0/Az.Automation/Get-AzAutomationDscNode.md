---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
ms.openlocfilehash: f1328b71564b0fd839d3481a87b23a2a8b24ab55
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186128"
---
# <span data-ttu-id="d0f7d-101">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d0f7d-101">Get-AzAutomationDscNode</span></span>

## <span data-ttu-id="d0f7d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d0f7d-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f7d-103">Az automatizálásból kapja a DSC csomópontokat.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-103">Gets DSC nodes from Automation.</span></span>

## <span data-ttu-id="d0f7d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d0f7d-104">SYNTAX</span></span>

### <span data-ttu-id="d0f7d-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d0f7d-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0f7d-106">ById</span><span class="sxs-lookup"><span data-stu-id="d0f7d-106">ById</span></span>
```
Get-AzAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0f7d-107">ByName</span><span class="sxs-lookup"><span data-stu-id="d0f7d-107">ByName</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0f7d-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0f7d-108">ByNodeConfiguration</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0f7d-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="d0f7d-109">ByConfiguration</span></span>
```
Get-AzAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0f7d-110">Leírás</span><span class="sxs-lookup"><span data-stu-id="d0f7d-110">DESCRIPTION</span></span>
<span data-ttu-id="d0f7d-111">A **Get-AzAutomationDscNode** parancsmag az Azure automatizálási rendszerének megfelelő állami konfigurációs (DSC) csomópontokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-111">The **Get-AzAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="d0f7d-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d0f7d-112">EXAMPLES</span></span>

### <span data-ttu-id="d0f7d-113">1. példa: az összes DSC csomópont beolvasása</span><span class="sxs-lookup"><span data-stu-id="d0f7d-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d0f7d-114">Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC csomópontjának metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d0f7d-115">2. példa: a DSC-csomópontok beszerzése DSC-konfigurációhoz</span><span class="sxs-lookup"><span data-stu-id="d0f7d-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="d0f7d-116">Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC csomópontjának metaadatait kapja, amelyeket a DSC konfigurációs ContosoConfiguration generált DSC csomópont-konfigurációhoz társítanak.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="d0f7d-117">3. példa: DSC-csomópont beszerzése AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="d0f7d-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="d0f7d-118">Ez a parancs a Contoso17 nevű automatizálási fiókban megadott azonosítót tartalmazó DSC-csomópont metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d0f7d-119">Példa 4: DSC csomópont beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="d0f7d-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="d0f7d-120">Ez a parancs egy DSC-csomópont metaadatait kapja, a Computer14 nevű Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d0f7d-121">Példa 5: az összes DSC csomópont beolvasása DSC-csomópont konfigurációjához</span><span class="sxs-lookup"><span data-stu-id="d0f7d-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="d0f7d-122">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók összes DSC csomópontján, amelyek egy ContosoConfiguration. webszerver nevű DSC csomópont-konfigurációhoz vannak rendelve.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="d0f7d-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d0f7d-123">PARAMETERS</span></span>

### <span data-ttu-id="d0f7d-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d0f7d-124">-AutomationAccountName</span></span>
<span data-ttu-id="d0f7d-125">Itt adhatja meg annak az automatizálási fióknak a nevét, amely a parancsmag által kapott DSC csomópontokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d0f7d-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d0f7d-126">-ConfigurationName</span></span>
<span data-ttu-id="d0f7d-127">A DSC-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="d0f7d-128">Ez a parancsmag olyan DSC csomópontokat kap, amelyek megfelelnek a paraméter által definiált konfigurációból létrehozott csomópont-konfigurációknak.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f7d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f7d-129">-DefaultProfile</span></span>
<span data-ttu-id="d0f7d-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d0f7d-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0f7d-131">-Azonosító</span><span class="sxs-lookup"><span data-stu-id="d0f7d-131">-Id</span></span>
<span data-ttu-id="d0f7d-132">Annak a DSC-csomópontnak az egyedi AZONOSÍTÓját adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f7d-133">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d0f7d-133">-Name</span></span>
<span data-ttu-id="d0f7d-134">Itt adhatja meg annak a DSC-csomópontnak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f7d-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d0f7d-135">-NodeConfigurationName</span></span>
<span data-ttu-id="d0f7d-136">Itt adhatja meg annak a csomópont-konfigurációnak a nevét, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f7d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f7d-137">-ResourceGroupName</span></span>
<span data-ttu-id="d0f7d-138">Annak a csoportnak a nevét adja meg, amelyben ez a parancsmag a DSC csomópontokat kapja.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="d0f7d-139">-Állapot</span><span class="sxs-lookup"><span data-stu-id="d0f7d-139">-Status</span></span>
<span data-ttu-id="d0f7d-140">A parancsmag által kapott DSC csomópontok állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d0f7d-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="d0f7d-141">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d0f7d-141">Valid values are:</span></span> 
- <span data-ttu-id="d0f7d-142">Kompatibilis</span><span class="sxs-lookup"><span data-stu-id="d0f7d-142">Compliant</span></span> 
- <span data-ttu-id="d0f7d-143">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="d0f7d-143">NotCompliant</span></span>
- <span data-ttu-id="d0f7d-144">Sikertelen</span><span class="sxs-lookup"><span data-stu-id="d0f7d-144">Failed</span></span>
- <span data-ttu-id="d0f7d-145">Függőben</span><span class="sxs-lookup"><span data-stu-id="d0f7d-145">Pending</span></span> 
- <span data-ttu-id="d0f7d-146">Kapott</span><span class="sxs-lookup"><span data-stu-id="d0f7d-146">Received</span></span>
- <span data-ttu-id="d0f7d-147">Hűvös</span><span class="sxs-lookup"><span data-stu-id="d0f7d-147">Unresponsive</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases:
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f7d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f7d-148">CommonParameters</span></span>
<span data-ttu-id="d0f7d-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d0f7d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f7d-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f7d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f7d-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0f7d-151">INPUTS</span></span>

### <span data-ttu-id="d0f7d-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d0f7d-152">System.Guid</span></span>

### <span data-ttu-id="d0f7d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d0f7d-153">System.String</span></span>

## <span data-ttu-id="d0f7d-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d0f7d-154">OUTPUTS</span></span>

### <span data-ttu-id="d0f7d-155">Microsoft. Azure. Command. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="d0f7d-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="d0f7d-156">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d0f7d-156">NOTES</span></span>

## <span data-ttu-id="d0f7d-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d0f7d-157">RELATED LINKS</span></span>

[<span data-ttu-id="d0f7d-158">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d0f7d-158">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="d0f7d-159">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d0f7d-159">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="d0f7d-160">Regisztráció törlése – AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d0f7d-160">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)

