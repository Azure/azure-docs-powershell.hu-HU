---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
ms.openlocfilehash: f1328b71564b0fd839d3481a87b23a2a8b24ab55
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342749"
---
# <span data-ttu-id="f8bf4-101">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f8bf4-101">Get-AzAutomationDscNode</span></span>

## <span data-ttu-id="f8bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="f8bf4-103">DSC-csomópontokat kap az Automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-103">Gets DSC nodes from Automation.</span></span>

## <span data-ttu-id="f8bf4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="f8bf4-104">SYNTAX</span></span>

### <span data-ttu-id="f8bf4-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f8bf4-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8bf4-106">ById</span><span class="sxs-lookup"><span data-stu-id="f8bf4-106">ById</span></span>
```
Get-AzAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8bf4-107">ByName</span><span class="sxs-lookup"><span data-stu-id="f8bf4-107">ByName</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8bf4-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8bf4-108">ByNodeConfiguration</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8bf4-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8bf4-109">ByConfiguration</span></span>
```
Get-AzAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8bf4-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="f8bf4-110">DESCRIPTION</span></span>
<span data-ttu-id="f8bf4-111">A **Get-AzAutomationDscNode** parancsmag az APS kívánt államkonfigurációs (DSC) csomópontokat kap az Azure Automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-111">The **Get-AzAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="f8bf4-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="f8bf4-112">EXAMPLES</span></span>

### <span data-ttu-id="f8bf4-113">1. példa: Az összes DSC-csomópont lekérte</span><span class="sxs-lookup"><span data-stu-id="f8bf4-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f8bf4-114">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók összes DSC-csomópontjára.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f8bf4-115">2. példa: Az összes DSC-csomópont lekérte a DSC-konfigurációt</span><span class="sxs-lookup"><span data-stu-id="f8bf4-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="f8bf4-116">Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC-csomópontjának metaadatait kapja, amelyek a ContosoConfiguration nevű DSC-konfigurációval létrehozott DSC-csomópont-konfigurációhoz vannak hozzárendelve.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="f8bf4-117">3. példa: DSC-csomópont lekérte azonosító szerint</span><span class="sxs-lookup"><span data-stu-id="f8bf4-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="f8bf4-118">Ez a parancs metaadatokat kap egy Olyan DSC-csomóponton, amely a Contoso17 nevű automatizálási fiókban megadott azonosítóval van megadva.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f8bf4-119">4. példa: DSC-csomópont lekérte név szerint</span><span class="sxs-lookup"><span data-stu-id="f8bf4-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="f8bf4-120">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók Számítógép14 nevű DSC-csomópontján.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f8bf4-121">5. példa: Az összes DSC-csomópont DSC-csomópont-konfigurációnak megfeleltetve</span><span class="sxs-lookup"><span data-stu-id="f8bf4-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="f8bf4-122">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók összes DSC-csomópontján, amelyek a ContosoConfiguration.webserver nevű DSC-csomópont-konfigurációnak vannak megfeleltetve.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="f8bf4-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8bf4-123">PARAMETERS</span></span>

### <span data-ttu-id="f8bf4-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f8bf4-124">-AutomationAccountName</span></span>
<span data-ttu-id="f8bf4-125">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag DSC-csomópontját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f8bf4-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f8bf4-126">-ConfigurationName</span></span>
<span data-ttu-id="f8bf4-127">Egy DSC-konfiguráció nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="f8bf4-128">Ez a parancsmag olyan DSC-csomópontokat kap, amelyek megfelelnek a paraméter által megadott konfigurációból generált csomópont-konfigurációnak.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

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

### <span data-ttu-id="f8bf4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8bf4-129">-DefaultProfile</span></span>
<span data-ttu-id="f8bf4-130">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="f8bf4-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8bf4-131">-Id</span><span class="sxs-lookup"><span data-stu-id="f8bf4-131">-Id</span></span>
<span data-ttu-id="f8bf4-132">A parancsmag DSC-csomópontjának egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f8bf4-133">-Name</span><span class="sxs-lookup"><span data-stu-id="f8bf4-133">-Name</span></span>
<span data-ttu-id="f8bf4-134">Annak a DSC-csomópontnak a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f8bf4-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f8bf4-135">-NodeConfigurationName</span></span>
<span data-ttu-id="f8bf4-136">Annak a csomópont-konfigurációnak a nevét adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f8bf4-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8bf4-137">-ResourceGroupName</span></span>
<span data-ttu-id="f8bf4-138">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag DSC-csomópontokat kap.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="f8bf4-139">-Állapot</span><span class="sxs-lookup"><span data-stu-id="f8bf4-139">-Status</span></span>
<span data-ttu-id="f8bf4-140">A parancsmag DSC-csomópontjainak állapotát adja meg.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="f8bf4-141">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="f8bf4-141">Valid values are:</span></span> 
- <span data-ttu-id="f8bf4-142">Kompatibilis</span><span class="sxs-lookup"><span data-stu-id="f8bf4-142">Compliant</span></span> 
- <span data-ttu-id="f8bf4-143">NotComp lesz</span><span class="sxs-lookup"><span data-stu-id="f8bf4-143">NotCompliant</span></span>
- <span data-ttu-id="f8bf4-144">Nem sikerült</span><span class="sxs-lookup"><span data-stu-id="f8bf4-144">Failed</span></span>
- <span data-ttu-id="f8bf4-145">Függőben</span><span class="sxs-lookup"><span data-stu-id="f8bf4-145">Pending</span></span> 
- <span data-ttu-id="f8bf4-146">Érkezett</span><span class="sxs-lookup"><span data-stu-id="f8bf4-146">Received</span></span>
- <span data-ttu-id="f8bf4-147">Nem válaszol</span><span class="sxs-lookup"><span data-stu-id="f8bf4-147">Unresponsive</span></span>

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

### <span data-ttu-id="f8bf4-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8bf4-148">CommonParameters</span></span>
<span data-ttu-id="f8bf4-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8bf4-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8bf4-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8bf4-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8bf4-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8bf4-151">INPUTS</span></span>

### <span data-ttu-id="f8bf4-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f8bf4-152">System.Guid</span></span>

### <span data-ttu-id="f8bf4-153">System.String</span><span class="sxs-lookup"><span data-stu-id="f8bf4-153">System.String</span></span>

## <span data-ttu-id="f8bf4-154">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f8bf4-154">OUTPUTS</span></span>

### <span data-ttu-id="f8bf4-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="f8bf4-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="f8bf4-156">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="f8bf4-156">NOTES</span></span>

## <span data-ttu-id="f8bf4-157">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f8bf4-157">RELATED LINKS</span></span>

[<span data-ttu-id="f8bf4-158">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f8bf4-158">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="f8bf4-159">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f8bf4-159">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="f8bf4-160">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f8bf4-160">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


