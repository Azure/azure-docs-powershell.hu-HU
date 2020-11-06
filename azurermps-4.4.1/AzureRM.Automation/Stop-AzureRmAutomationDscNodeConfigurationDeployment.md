---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3ddaf0d4ae609305bf9740fbbe38a5fddd414e18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503272"
---
# <span data-ttu-id="6401d-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="6401d-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="6401d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6401d-102">SYNOPSIS</span></span>
<span data-ttu-id="6401d-103">A DSC csomópontok konfigurációjának leállítása az automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="6401d-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="6401d-104">Csak a jelenlegi központi telepítés feladatát állítja le, de nem rendeli hozzá a már hozzárendelt csomópont-konfigurációkat.</span><span class="sxs-lookup"><span data-stu-id="6401d-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6401d-105">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6401d-105">SYNTAX</span></span>

### <span data-ttu-id="6401d-106">ByJobId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="6401d-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6401d-107">ByByInputObject</span><span class="sxs-lookup"><span data-stu-id="6401d-107">ByByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6401d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="6401d-108">DESCRIPTION</span></span>
<span data-ttu-id="6401d-109">A **stop-AzureRmAutomationDscNodeConfigurationDeployment** parancsmag leállítja a megfelelő állapot-konfiguráció (DSC) csomópont-konfigurációjának telepítését az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="6401d-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="6401d-110">A csomópont-konfiguráció hozzárendelését leállítja a csomópontok csoportjaira, ha a program még nem rendeli hozzá a csomópontokat, de a már hozzárendelt csomópontokat nem.</span><span class="sxs-lookup"><span data-stu-id="6401d-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="6401d-111">Ha egy ütemezett feladatot szeretne regisztrálni, kérjük, használja a [regisztráció nélküli AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) a JobScheduleId a meglévő ütemezett feladatok hozzárendelésének visszavonásához.</span><span class="sxs-lookup"><span data-stu-id="6401d-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="6401d-112">Példák</span><span class="sxs-lookup"><span data-stu-id="6401d-112">EXAMPLES</span></span>

### <span data-ttu-id="6401d-113">1. példa: Azure DSC csomópont-konfiguráció telepítése automatizálással</span><span class="sxs-lookup"><span data-stu-id="6401d-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="6401d-114">A fenti parancs leállítja a DSC Node Configuration telepítő feladatát az átadott jobId.</span><span class="sxs-lookup"><span data-stu-id="6401d-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="6401d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6401d-115">PARAMETERS</span></span>

### <span data-ttu-id="6401d-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6401d-116">-AutomationAccountName</span></span>
<span data-ttu-id="6401d-117">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag által lefordított DSC-konfigurációt tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="6401d-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6401d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6401d-118">-ResourceGroupName</span></span>
<span data-ttu-id="6401d-119">Annak a csoportnak a nevét adja meg, amelyben a parancsmag egy konfigurációt összeállít.</span><span class="sxs-lookup"><span data-stu-id="6401d-119">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="6401d-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="6401d-120">-JobId</span></span>
<span data-ttu-id="6401d-121">A meglévő központi telepítés feladatának munkaazonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6401d-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="6401d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6401d-122">-PassThru</span></span>
<span data-ttu-id="6401d-123">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="6401d-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6401d-124">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="6401d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6401d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6401d-125">-Force</span></span>
<span data-ttu-id="6401d-126">ps_force</span><span class="sxs-lookup"><span data-stu-id="6401d-126">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6401d-127">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6401d-127">-Confirm</span></span>
<span data-ttu-id="6401d-128">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6401d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6401d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6401d-129">-WhatIf</span></span>
<span data-ttu-id="6401d-130">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6401d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6401d-131">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6401d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6401d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6401d-132">-DefaultProfile</span></span>
<span data-ttu-id="6401d-133">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6401d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6401d-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6401d-134">-InputObject</span></span>
<span data-ttu-id="6401d-135">A csővezeték beviteli objektuma.</span><span class="sxs-lookup"><span data-stu-id="6401d-135">Input object for Piping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6401d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6401d-136">CommonParameters</span></span>
<span data-ttu-id="6401d-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6401d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6401d-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6401d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6401d-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6401d-139">INPUTS</span></span>

## <span data-ttu-id="6401d-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6401d-140">OUTPUTS</span></span>

## <span data-ttu-id="6401d-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6401d-141">NOTES</span></span>

## <span data-ttu-id="6401d-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6401d-142">RELATED LINKS</span></span>

[<span data-ttu-id="6401d-143">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="6401d-143">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="6401d-144">Importálás – AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="6401d-144">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="6401d-145">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="6401d-145">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="6401d-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="6401d-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="6401d-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="6401d-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
