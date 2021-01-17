---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478454"
---
# <span data-ttu-id="2c830-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="2c830-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="2c830-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c830-102">SYNOPSIS</span></span>
<span data-ttu-id="2c830-103">Leállítja a DSC-csomópont konfigurációjának telepítését az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="2c830-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="2c830-104">Ez csak leállítja az aktuális telepítési feladatot, de nem rendeli hozzá a már hozzárendelt csomópont-konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="2c830-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="2c830-105">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2c830-105">SYNTAX</span></span>

### <span data-ttu-id="2c830-106">ByJobId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2c830-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c830-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2c830-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c830-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2c830-108">DESCRIPTION</span></span>
<span data-ttu-id="2c830-109">A **Stop-AzAutomationDscNodeConfigurationDeployment parancsmag** leállítja a kívánt állapotkonfiguráció (DSC) csomópont-konfigurációjának telepítését az Azure Automationben.</span><span class="sxs-lookup"><span data-stu-id="2c830-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="2c830-110">Leállítja a csomópont-konfiguráció hozzárendelését csomópontcsoportokhoz, ha vannak még hozzárendelhető csomópontok, de nem rendeli hozzá a már hozzárendelt csomópontokat.</span><span class="sxs-lookup"><span data-stu-id="2c830-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="2c830-111">Egy ütemezett feladat regisztrációjának a visszalépéshez használja a [Unregister-AzAutomationScheduledRunbookot](./Unregister-AzAutomationScheduledRunbook.md) a JobScheduleId fájllal egy meglévő ütemezett feladat hozzárendelésének a visszalépésére.</span><span class="sxs-lookup"><span data-stu-id="2c830-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="2c830-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2c830-112">EXAMPLES</span></span>

### <span data-ttu-id="2c830-113">1. példa: Azure DSC-csomópont konfigurációjának üzembe helyezése az Automatizálásban</span><span class="sxs-lookup"><span data-stu-id="2c830-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="2c830-114">A fenti parancs leállítja a DSC-csomópont konfigurációs telepítési feladatát úgy, hogy a jobId át lesz edve.</span><span class="sxs-lookup"><span data-stu-id="2c830-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="2c830-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c830-115">PARAMETERS</span></span>

### <span data-ttu-id="2c830-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2c830-116">-AutomationAccountName</span></span>
<span data-ttu-id="2c830-117">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza</span><span class="sxs-lookup"><span data-stu-id="2c830-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="2c830-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c830-118">-DefaultProfile</span></span>
<span data-ttu-id="2c830-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2c830-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c830-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2c830-120">-Force</span></span>
<span data-ttu-id="2c830-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="2c830-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c830-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c830-122">-InputObject</span></span>
<span data-ttu-id="2c830-123">Input object for Piping</span><span class="sxs-lookup"><span data-stu-id="2c830-123">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c830-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="2c830-124">-JobId</span></span>
<span data-ttu-id="2c830-125">Egy meglévő üzembe helyezési feladat feladatazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2c830-125">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c830-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c830-126">-PassThru</span></span>
<span data-ttu-id="2c830-127">Egy objektumot ad vissza, amely azt az elemet tartalmazza, amellyel dolgozik.</span><span class="sxs-lookup"><span data-stu-id="2c830-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2c830-128">Ez a parancsmag alapértelmezés szerint nem hoz létre kimenetet.</span><span class="sxs-lookup"><span data-stu-id="2c830-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2c830-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c830-129">-ResourceGroupName</span></span>
<span data-ttu-id="2c830-130">Annak az erőforráscsoportnak a nevét adja meg, amelyben ez a parancsmag konfigurációt fordít.</span><span class="sxs-lookup"><span data-stu-id="2c830-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="2c830-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c830-131">-Confirm</span></span>
<span data-ttu-id="2c830-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2c830-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c830-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c830-133">-WhatIf</span></span>
<span data-ttu-id="2c830-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2c830-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c830-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c830-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c830-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c830-136">CommonParameters</span></span>
<span data-ttu-id="2c830-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c830-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c830-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c830-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c830-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c830-139">INPUTS</span></span>

### <span data-ttu-id="2c830-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="2c830-140">System.Guid</span></span>

### <span data-ttu-id="2c830-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="2c830-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="2c830-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2c830-142">System.String</span></span>

## <span data-ttu-id="2c830-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c830-143">OUTPUTS</span></span>

### <span data-ttu-id="2c830-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2c830-144">System.Boolean</span></span>

## <span data-ttu-id="2c830-145">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2c830-145">NOTES</span></span>

## <span data-ttu-id="2c830-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c830-146">RELATED LINKS</span></span>

[<span data-ttu-id="2c830-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="2c830-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="2c830-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c830-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="2c830-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="2c830-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="2c830-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="2c830-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="2c830-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="2c830-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
