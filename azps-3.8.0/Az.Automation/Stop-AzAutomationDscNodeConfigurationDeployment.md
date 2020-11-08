---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94002922"
---
# <span data-ttu-id="7c46a-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="7c46a-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="7c46a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7c46a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c46a-103">A DSC csomópontok konfigurációjának leállítása az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="7c46a-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="7c46a-104">Csak a jelenlegi központi telepítés feladatát állítja le, de nem rendeli hozzá a már hozzárendelt csomópont-konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="7c46a-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="7c46a-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7c46a-105">SYNTAX</span></span>

### <span data-ttu-id="7c46a-106">ByJobId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="7c46a-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c46a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7c46a-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c46a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="7c46a-108">DESCRIPTION</span></span>
<span data-ttu-id="7c46a-109">A **stop-AzAutomationDscNodeConfigurationDeployment** parancsmag leállítja a megfelelő állapot-konfiguráció (DSC) csomópont-konfigurációjának telepítését az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="7c46a-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="7c46a-110">A csomópont-konfiguráció hozzárendelését leállítja a csomópontok csoportjaira, ha a program még nem rendeli hozzá a csomópontokat, de a már hozzárendelt csomópontokat nem.</span><span class="sxs-lookup"><span data-stu-id="7c46a-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="7c46a-111">Ha egy ütemezett feladatot szeretne regisztrálni, kérjük, használja a [regisztráció nélküli AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) a JobScheduleId a meglévő ütemezett feladatok hozzárendelésének visszavonásához.</span><span class="sxs-lookup"><span data-stu-id="7c46a-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="7c46a-112">Példák</span><span class="sxs-lookup"><span data-stu-id="7c46a-112">EXAMPLES</span></span>

### <span data-ttu-id="7c46a-113">1. példa: Azure DSC csomópont-konfiguráció telepítése automatizálással</span><span class="sxs-lookup"><span data-stu-id="7c46a-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="7c46a-114">A fenti parancs leállítja a DSC Node Configuration telepítő feladatát az átadott jobId.</span><span class="sxs-lookup"><span data-stu-id="7c46a-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="7c46a-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7c46a-115">PARAMETERS</span></span>

### <span data-ttu-id="7c46a-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7c46a-116">-AutomationAccountName</span></span>
<span data-ttu-id="7c46a-117">Annak az automatizálási fióknak a neve, amely a parancsmag által lefordítható DSC-konfigurációt tartalmazza</span><span class="sxs-lookup"><span data-stu-id="7c46a-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="7c46a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c46a-118">-DefaultProfile</span></span>
<span data-ttu-id="7c46a-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="7c46a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c46a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7c46a-120">-Force</span></span>
<span data-ttu-id="7c46a-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="7c46a-121">ps_force</span></span>

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

### <span data-ttu-id="7c46a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c46a-122">-InputObject</span></span>
<span data-ttu-id="7c46a-123">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="7c46a-123">Input object for Piping</span></span>

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

### <span data-ttu-id="7c46a-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="7c46a-124">-JobId</span></span>
<span data-ttu-id="7c46a-125">A meglévő központi telepítés feladatának munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="7c46a-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="7c46a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c46a-126">-PassThru</span></span>
<span data-ttu-id="7c46a-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="7c46a-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7c46a-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="7c46a-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7c46a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c46a-129">-ResourceGroupName</span></span>
<span data-ttu-id="7c46a-130">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="7c46a-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="7c46a-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7c46a-131">-Confirm</span></span>
<span data-ttu-id="7c46a-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7c46a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c46a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c46a-133">-WhatIf</span></span>
<span data-ttu-id="7c46a-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7c46a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c46a-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7c46a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c46a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c46a-136">CommonParameters</span></span>
<span data-ttu-id="7c46a-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7c46a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c46a-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c46a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c46a-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c46a-139">INPUTS</span></span>

### <span data-ttu-id="7c46a-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7c46a-140">System.Guid</span></span>

### <span data-ttu-id="7c46a-141">Microsoft. Azure. Command. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="7c46a-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="7c46a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7c46a-142">System.String</span></span>

## <span data-ttu-id="7c46a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7c46a-143">OUTPUTS</span></span>

### <span data-ttu-id="7c46a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c46a-144">System.Boolean</span></span>

## <span data-ttu-id="7c46a-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7c46a-145">NOTES</span></span>

## <span data-ttu-id="7c46a-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7c46a-146">RELATED LINKS</span></span>

[<span data-ttu-id="7c46a-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="7c46a-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="7c46a-148">Importálás – AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c46a-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="7c46a-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="7c46a-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="7c46a-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="7c46a-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="7c46a-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="7c46a-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
