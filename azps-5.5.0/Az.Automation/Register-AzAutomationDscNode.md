---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149395"
---
# <span data-ttu-id="71e2c-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="71e2c-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="71e2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="71e2c-103">Egy Windows operációs rendszert futtató Azure virtuális gépet regisztrál DSC-csomópontként egy automatizálási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="71e2c-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="71e2c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="71e2c-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="71e2c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="71e2c-105">DESCRIPTION</span></span>
<span data-ttu-id="71e2c-106">A **Register-AzAutomationDscNode** parancsmag egy Azure Automation-fiókban APS-beli kívánt államkonfigurációs (DSC) csomópontként regisztrálja az Azure virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="71e2c-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="71e2c-107">Ez a parancsmag csak a Windows operációs rendszert futtató gépeket regisztrálja automatizálási DSC-csomópontként egy fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="71e2c-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="71e2c-108">Ha másik előfizetésben kell regisztrálnia egy csomópontot egy automatizálási fiókban, parancsmagok helyett egy ARM kell használnia.</span><span class="sxs-lookup"><span data-stu-id="71e2c-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="71e2c-109">További [részleteket](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) az Azure Automation dokumentációjában talál.</span><span class="sxs-lookup"><span data-stu-id="71e2c-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="71e2c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="71e2c-110">EXAMPLES</span></span>

### <span data-ttu-id="71e2c-111">1. példa: Azure virtuális gép regisztrálása Azure DSC-csomópontként</span><span class="sxs-lookup"><span data-stu-id="71e2c-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="71e2c-112">Ez a parancs regisztrálja a VirtualMachine01 nevű Azure virtuális gépet DSC-csomópontként a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="71e2c-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="71e2c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71e2c-113">PARAMETERS</span></span>

### <span data-ttu-id="71e2c-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="71e2c-114">-ActionAfterReboot</span></span>
<span data-ttu-id="71e2c-115">A virtuális gép újraindítása után szükséges műveletet adja meg.</span><span class="sxs-lookup"><span data-stu-id="71e2c-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="71e2c-116">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="71e2c-116">Valid values are:</span></span> 
- <span data-ttu-id="71e2c-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="71e2c-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="71e2c-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="71e2c-118">StopConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e2c-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="71e2c-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="71e2c-120">Meghatározza, hogy az új konfigurációk, amelyek ezt a DSC-csomópontot letöltik az Azure Automation DSC letöltő kiszolgálóról, lecserélik-e a célcsomóponton már meglévő modulokat.</span><span class="sxs-lookup"><span data-stu-id="71e2c-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e2c-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="71e2c-121">-AutomationAccountName</span></span>
<span data-ttu-id="71e2c-122">Annak az automatizálási fióknak a nevét adja meg, amelyben ez a parancsmag regisztrál egy virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="71e2c-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="71e2c-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="71e2c-123">-AzureVMLocation</span></span>
<span data-ttu-id="71e2c-124">Az Azure VM-hely.</span><span class="sxs-lookup"><span data-stu-id="71e2c-124">The Azure VM location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e2c-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="71e2c-125">-AzureVMName</span></span>
<span data-ttu-id="71e2c-126">Annak az Azure-virtuális gépnek a neve, amely regisztrál az Azure Automation DSC-val való kezeléshez.</span><span class="sxs-lookup"><span data-stu-id="71e2c-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="71e2c-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71e2c-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="71e2c-128">Az Azure VM erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="71e2c-128">The Azure VM resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e2c-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="71e2c-129">-ConfigurationMode</span></span>
<span data-ttu-id="71e2c-130">A DSC konfigurációs módját adja meg.</span><span class="sxs-lookup"><span data-stu-id="71e2c-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="71e2c-131">Érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="71e2c-131">Valid values are:</span></span> 
- <span data-ttu-id="71e2c-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="71e2c-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="71e2c-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="71e2c-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="71e2c-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="71e2c-134">ApplyOnly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e2c-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="71e2c-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="71e2c-136">Azt adja meg percben, hogy a DSC háttéralkalmazása milyen gyakorisággal kísérli meg implementni az aktuális konfigurációt a célcsomóponton.</span><span class="sxs-lookup"><span data-stu-id="71e2c-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e2c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e2c-137">-DefaultProfile</span></span>
<span data-ttu-id="71e2c-138">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="71e2c-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71e2c-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="71e2c-139">-NodeConfigurationName</span></span>
<span data-ttu-id="71e2c-140">Annak a csomópont-konfigurációnak a nevét adja meg, amelynél ez a parancsmag beállítja a virtuális gépet az Azure Automation DSC-ból.</span><span class="sxs-lookup"><span data-stu-id="71e2c-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e2c-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="71e2c-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="71e2c-142">Megadja, hogy szükség esetén újraindítsa-e a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="71e2c-142">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e2c-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="71e2c-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="71e2c-144">Azt adja meg percben, hogy a helyi Configuration Manager milyen gyakorisággal lép kapcsolatba az Azure Automation DSC letöltőkiszolgálóval a legújabb csomópont-konfiguráció letöltéséhez.</span><span class="sxs-lookup"><span data-stu-id="71e2c-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71e2c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e2c-145">-ResourceGroupName</span></span>
<span data-ttu-id="71e2c-146">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="71e2c-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="71e2c-147">Az az automatizálási fiók, amellyel ez a parancsmag regisztrál egy virtuális gépet, annak az erőforráscsoportnak a tagja, amelyet ez a paraméter megad.</span><span class="sxs-lookup"><span data-stu-id="71e2c-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="71e2c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e2c-148">CommonParameters</span></span>
<span data-ttu-id="71e2c-149">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71e2c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e2c-150">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71e2c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e2c-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="71e2c-151">INPUTS</span></span>

### <span data-ttu-id="71e2c-152">System.String</span><span class="sxs-lookup"><span data-stu-id="71e2c-152">System.String</span></span>

### <span data-ttu-id="71e2c-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="71e2c-153">System.Int32</span></span>

### <span data-ttu-id="71e2c-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71e2c-154">System.Boolean</span></span>

## <span data-ttu-id="71e2c-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71e2c-155">OUTPUTS</span></span>

### <span data-ttu-id="71e2c-156">System.Void</span><span class="sxs-lookup"><span data-stu-id="71e2c-156">System.Void</span></span>

## <span data-ttu-id="71e2c-157">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="71e2c-157">NOTES</span></span>

## <span data-ttu-id="71e2c-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71e2c-158">RELATED LINKS</span></span>

[<span data-ttu-id="71e2c-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="71e2c-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="71e2c-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="71e2c-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="71e2c-161">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="71e2c-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


