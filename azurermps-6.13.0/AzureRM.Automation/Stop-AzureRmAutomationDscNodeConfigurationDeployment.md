---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 466cb31bd5e05235085fbc4f9045cf201a806e11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492880"
---
# <span data-ttu-id="692db-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="692db-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="692db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="692db-102">SYNOPSIS</span></span>
<span data-ttu-id="692db-103">A DSC csomópontok konfigurációjának leállítása az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="692db-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="692db-104">Csak a jelenlegi központi telepítés feladatát állítja le, de nem rendeli hozzá a már hozzárendelt csomópont-konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="692db-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="692db-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="692db-105">SYNTAX</span></span>

### <span data-ttu-id="692db-106">ByJobId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="692db-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="692db-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="692db-107">ByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="692db-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="692db-108">DESCRIPTION</span></span>
<span data-ttu-id="692db-109">A **stop-AzureRmAutomationDscNodeConfigurationDeployment** parancsmag leállítja a megfelelő állapot-konfiguráció (DSC) csomópont-konfigurációjának telepítését az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="692db-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="692db-110">A csomópont-konfiguráció hozzárendelését leállítja a csomópontok csoportjaira, ha a program még nem rendeli hozzá a csomópontokat, de a már hozzárendelt csomópontokat nem.</span><span class="sxs-lookup"><span data-stu-id="692db-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="692db-111">Ha egy ütemezett feladatot szeretne regisztrálni, kérjük, használja a [regisztráció nélküli AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) a JobScheduleId a meglévő ütemezett feladatok hozzárendelésének visszavonásához.</span><span class="sxs-lookup"><span data-stu-id="692db-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="692db-112">Példák</span><span class="sxs-lookup"><span data-stu-id="692db-112">EXAMPLES</span></span>

### <span data-ttu-id="692db-113">1. példa: Azure DSC csomópont-konfiguráció telepítése automatizálással</span><span class="sxs-lookup"><span data-stu-id="692db-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="692db-114">A fenti parancs leállítja a DSC Node Configuration telepítő feladatát az átadott jobId.</span><span class="sxs-lookup"><span data-stu-id="692db-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="692db-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="692db-115">PARAMETERS</span></span>

### <span data-ttu-id="692db-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="692db-116">-AutomationAccountName</span></span>
<span data-ttu-id="692db-117">Annak az automatizálási fióknak a neve, amely a parancsmag által lefordítható DSC-konfigurációt tartalmazza</span><span class="sxs-lookup"><span data-stu-id="692db-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="692db-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="692db-118">-DefaultProfile</span></span>
<span data-ttu-id="692db-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="692db-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="692db-120">-Force</span><span class="sxs-lookup"><span data-stu-id="692db-120">-Force</span></span>
<span data-ttu-id="692db-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="692db-121">ps_force</span></span>

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

### <span data-ttu-id="692db-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="692db-122">-InputObject</span></span>
<span data-ttu-id="692db-123">A csővezeték beviteli objektuma</span><span class="sxs-lookup"><span data-stu-id="692db-123">Input object for Piping</span></span>

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

### <span data-ttu-id="692db-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="692db-124">-JobId</span></span>
<span data-ttu-id="692db-125">A meglévő központi telepítés feladatának munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="692db-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="692db-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="692db-126">-PassThru</span></span>
<span data-ttu-id="692db-127">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="692db-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="692db-128">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="692db-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="692db-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="692db-129">-ResourceGroupName</span></span>
<span data-ttu-id="692db-130">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="692db-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="692db-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="692db-131">-Confirm</span></span>
<span data-ttu-id="692db-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="692db-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="692db-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="692db-133">-WhatIf</span></span>
<span data-ttu-id="692db-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="692db-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="692db-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="692db-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="692db-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="692db-136">CommonParameters</span></span>
<span data-ttu-id="692db-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="692db-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="692db-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="692db-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="692db-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="692db-139">INPUTS</span></span>

### <span data-ttu-id="692db-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="692db-140">System.Guid</span></span>

### <span data-ttu-id="692db-141">Microsoft. Azure. Command. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="692db-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>
<span data-ttu-id="692db-142">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="692db-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="692db-143">System. String</span><span class="sxs-lookup"><span data-stu-id="692db-143">System.String</span></span>

## <span data-ttu-id="692db-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="692db-144">OUTPUTS</span></span>

### <span data-ttu-id="692db-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="692db-145">System.Boolean</span></span>

## <span data-ttu-id="692db-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="692db-146">NOTES</span></span>

## <span data-ttu-id="692db-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="692db-147">RELATED LINKS</span></span>

[<span data-ttu-id="692db-148">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="692db-148">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="692db-149">Importálás – AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="692db-149">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="692db-150">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="692db-150">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="692db-151">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="692db-151">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="692db-152">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="692db-152">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
