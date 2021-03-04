---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
ms.openlocfilehash: 790c280d139f2770f08d5ecfed64acf42d0fc1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938337"
---
# <span data-ttu-id="38eac-101">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="38eac-101">Get-AzAutomationDscNode</span></span>

## <span data-ttu-id="38eac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38eac-102">SYNOPSIS</span></span>
<span data-ttu-id="38eac-103">DSC-csomópontokat kap az Automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="38eac-103">Gets DSC nodes from Automation.</span></span>

## <span data-ttu-id="38eac-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="38eac-104">SYNTAX</span></span>

### <span data-ttu-id="38eac-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38eac-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38eac-106">ById</span><span class="sxs-lookup"><span data-stu-id="38eac-106">ById</span></span>
```
Get-AzAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38eac-107">ByName</span><span class="sxs-lookup"><span data-stu-id="38eac-107">ByName</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38eac-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="38eac-108">ByNodeConfiguration</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38eac-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="38eac-109">ByConfiguration</span></span>
```
Get-AzAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38eac-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="38eac-110">DESCRIPTION</span></span>
<span data-ttu-id="38eac-111">A **Get-AzAutomationDscNode** parancsmag az APS kívánt államkonfigurációs (DSC) csomópontokat kap az Azure Automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="38eac-111">The **Get-AzAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="38eac-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="38eac-112">EXAMPLES</span></span>

### <span data-ttu-id="38eac-113">1. példa: Az összes DSC-csomópont lekérte</span><span class="sxs-lookup"><span data-stu-id="38eac-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="38eac-114">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók összes DSC-csomópontjára.</span><span class="sxs-lookup"><span data-stu-id="38eac-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="38eac-115">2. példa: Az összes DSC-csomópont lekérte a DSC-konfigurációt</span><span class="sxs-lookup"><span data-stu-id="38eac-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="38eac-116">Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC-csomópontjának metaadatait kapja, amelyek a ContosoConfiguration nevű DSC-konfigurációval létrehozott DSC-csomópont-konfigurációhoz vannak hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="38eac-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="38eac-117">3. példa: DSC-csomópont lekérte azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="38eac-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="38eac-118">Ez a parancs metaadatokat kap egy Olyan DSC-csomóponton, amely a Contoso17 nevű automatizálási fiókban megadott azonosítóval van megadva.</span><span class="sxs-lookup"><span data-stu-id="38eac-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="38eac-119">4. példa: DSC-csomópont lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="38eac-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="38eac-120">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók Számítógép14 nevű DSC-csomópontján.</span><span class="sxs-lookup"><span data-stu-id="38eac-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="38eac-121">5. példa: Az összes DSC-csomópont DSC-csomópont-konfigurációnak megfeleltetve</span><span class="sxs-lookup"><span data-stu-id="38eac-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="38eac-122">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók összes DSC-csomópontján, amelyek a ContosoConfiguration.webserver nevű DSC-csomópont-konfigurációnak vannak megfeleltetve.</span><span class="sxs-lookup"><span data-stu-id="38eac-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="38eac-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38eac-123">PARAMETERS</span></span>

### <span data-ttu-id="38eac-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="38eac-124">-AutomationAccountName</span></span>
<span data-ttu-id="38eac-125">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag DSC-csomópontját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="38eac-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="38eac-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="38eac-126">-ConfigurationName</span></span>
<span data-ttu-id="38eac-127">Egy DSC-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38eac-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="38eac-128">Ez a parancsmag olyan DSC-csomópontokat kap, amelyek megfelelnek a paraméter által megadott konfigurációból generált csomópont-konfigurációnak.</span><span class="sxs-lookup"><span data-stu-id="38eac-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

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

### <span data-ttu-id="38eac-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38eac-129">-DefaultProfile</span></span>
<span data-ttu-id="38eac-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="38eac-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38eac-131">-Id</span><span class="sxs-lookup"><span data-stu-id="38eac-131">-Id</span></span>
<span data-ttu-id="38eac-132">A parancsmag DSC-csomópontjának egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="38eac-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="38eac-133">-Name</span><span class="sxs-lookup"><span data-stu-id="38eac-133">-Name</span></span>
<span data-ttu-id="38eac-134">Annak a DSC-csomópontnak a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="38eac-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="38eac-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="38eac-135">-NodeConfigurationName</span></span>
<span data-ttu-id="38eac-136">Annak a csomópont-konfigurációnak a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="38eac-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="38eac-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38eac-137">-ResourceGroupName</span></span>
<span data-ttu-id="38eac-138">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag DSC-csomópontokat kap.</span><span class="sxs-lookup"><span data-stu-id="38eac-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="38eac-139">-Állapot</span><span class="sxs-lookup"><span data-stu-id="38eac-139">-Status</span></span>
<span data-ttu-id="38eac-140">A parancsmag DSC-csomópontjainak állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="38eac-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="38eac-141">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="38eac-141">Valid values are:</span></span> 
- <span data-ttu-id="38eac-142">Kompatibilis</span><span class="sxs-lookup"><span data-stu-id="38eac-142">Compliant</span></span> 
- <span data-ttu-id="38eac-143">NotComp lesz</span><span class="sxs-lookup"><span data-stu-id="38eac-143">NotCompliant</span></span>
- <span data-ttu-id="38eac-144">Nem sikerült</span><span class="sxs-lookup"><span data-stu-id="38eac-144">Failed</span></span>
- <span data-ttu-id="38eac-145">Függőben</span><span class="sxs-lookup"><span data-stu-id="38eac-145">Pending</span></span> 
- <span data-ttu-id="38eac-146">Érkezett</span><span class="sxs-lookup"><span data-stu-id="38eac-146">Received</span></span>
- <span data-ttu-id="38eac-147">Nem válaszol</span><span class="sxs-lookup"><span data-stu-id="38eac-147">Unresponsive</span></span>

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

### <span data-ttu-id="38eac-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38eac-148">CommonParameters</span></span>
<span data-ttu-id="38eac-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38eac-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38eac-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38eac-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38eac-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38eac-151">INPUTS</span></span>

### <span data-ttu-id="38eac-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="38eac-152">System.Guid</span></span>

### <span data-ttu-id="38eac-153">System.String</span><span class="sxs-lookup"><span data-stu-id="38eac-153">System.String</span></span>

## <span data-ttu-id="38eac-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38eac-154">OUTPUTS</span></span>

### <span data-ttu-id="38eac-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="38eac-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="38eac-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="38eac-156">NOTES</span></span>

## <span data-ttu-id="38eac-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38eac-157">RELATED LINKS</span></span>

[<span data-ttu-id="38eac-158">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="38eac-158">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="38eac-159">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="38eac-159">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="38eac-160">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="38eac-160">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


