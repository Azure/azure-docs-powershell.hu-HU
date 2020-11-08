---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024926"
---
# <span data-ttu-id="82126-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="82126-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="82126-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="82126-102">SYNOPSIS</span></span>
<span data-ttu-id="82126-103">Egy, a Windows operációs rendszert futtató Azure Virtual Machine-t DSC-csomópontként regisztrál egy automatizálási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="82126-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="82126-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="82126-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82126-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="82126-105">DESCRIPTION</span></span>
<span data-ttu-id="82126-106">A **Register-AzAutomationDscNode** parancsmag az Azure Virtual Machine-t APS típusú, APS-es típusú (DSC) csomópontként regisztrálja egy Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="82126-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="82126-107">Ez a parancsmag csak a Windows operációs rendszert futtató virtuális gépeket rögzíti automatizálási DSC-csomópontként egy fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="82126-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="82126-108">Ha egy másik előfizetésbe egy automatizálási fiókba kell beiktatnia egy csomópontot, a parancsmag helyett egy ARM sablont kell használnia.</span><span class="sxs-lookup"><span data-stu-id="82126-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="82126-109">További részletekért tekintse meg az Azure Automation [dokumentációját](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) .</span><span class="sxs-lookup"><span data-stu-id="82126-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="82126-110">Példák</span><span class="sxs-lookup"><span data-stu-id="82126-110">EXAMPLES</span></span>

### <span data-ttu-id="82126-111">1. példa: az Azure Virtual Machine-t Azure DSC-csomópontként regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="82126-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="82126-112">Ez a parancs a VirtualMachine01 nevű Azure virtuális gépet DSC-csomópontként regisztrálja az Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="82126-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="82126-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="82126-113">PARAMETERS</span></span>

### <span data-ttu-id="82126-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="82126-114">-ActionAfterReboot</span></span>
<span data-ttu-id="82126-115">Meghatározza, hogy a virtuális gép milyen műveleteket hajtson végre az újraindítás után.</span><span class="sxs-lookup"><span data-stu-id="82126-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="82126-116">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="82126-116">Valid values are:</span></span> 
- <span data-ttu-id="82126-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="82126-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="82126-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="82126-118">StopConfiguration</span></span>

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

### <span data-ttu-id="82126-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="82126-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="82126-120">Itt adhatja meg, hogy a DSC-csomópont által az Azure automatizálási kiszolgálóról letöltött új konfigurációk felülírják-e a meglévő, már a cél csomóponton lévő modulokat.</span><span class="sxs-lookup"><span data-stu-id="82126-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="82126-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="82126-121">-AutomationAccountName</span></span>
<span data-ttu-id="82126-122">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag a virtuális gépet regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="82126-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="82126-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="82126-123">-AzureVMLocation</span></span>
<span data-ttu-id="82126-124">Az Azure VM helyszíne.</span><span class="sxs-lookup"><span data-stu-id="82126-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="82126-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="82126-125">-AzureVMName</span></span>
<span data-ttu-id="82126-126">Annak az Azure Virtual Machine-gépnek a neve, amely az Azure Automation DSC-vel való kezelésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="82126-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="82126-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="82126-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="82126-128">Az Azure VM-erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="82126-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="82126-129">-Állítsa ConfigurationMode kulcsot</span><span class="sxs-lookup"><span data-stu-id="82126-129">-ConfigurationMode</span></span>
<span data-ttu-id="82126-130">A DSC konfigurációs üzemmódját adja meg.</span><span class="sxs-lookup"><span data-stu-id="82126-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="82126-131">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="82126-131">Valid values are:</span></span> 
- <span data-ttu-id="82126-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="82126-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="82126-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="82126-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="82126-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="82126-134">ApplyOnly</span></span>

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

### <span data-ttu-id="82126-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="82126-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="82126-136">Annak gyakoriságát adja meg percben, amikor a DSC háttér-alkalmazása megkísérli végrehajtani a jelenlegi konfigurációt a cél csomóponton.</span><span class="sxs-lookup"><span data-stu-id="82126-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="82126-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82126-137">-DefaultProfile</span></span>
<span data-ttu-id="82126-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="82126-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82126-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="82126-139">-NodeConfigurationName</span></span>
<span data-ttu-id="82126-140">Itt adhatja meg annak a csomópont-konfigurációnak a nevét, amelyet a parancsmag a virtuális gépet az Azure automatizálási DSC-ről való kihúzásra állít be.</span><span class="sxs-lookup"><span data-stu-id="82126-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="82126-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="82126-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="82126-142">Megadja, hogy szükség esetén újra kell-e indítani a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="82126-142">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="82126-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="82126-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="82126-144">Annak gyakoriságát adja meg percben, amikor a helyi Konfigurációkezelő az Azure automatizálás DSC lekérési kiszolgálójának segítségével letölti a legújabb csomópont-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="82126-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="82126-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82126-145">-ResourceGroupName</span></span>
<span data-ttu-id="82126-146">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="82126-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="82126-147">Az automatizálási fiók, amellyel a parancsmag a virtuális gépet regisztrálja, a paraméter által megadott erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="82126-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="82126-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82126-148">CommonParameters</span></span>
<span data-ttu-id="82126-149">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="82126-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82126-150">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82126-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82126-151">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="82126-151">INPUTS</span></span>

### <span data-ttu-id="82126-152">System. String</span><span class="sxs-lookup"><span data-stu-id="82126-152">System.String</span></span>

### <span data-ttu-id="82126-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="82126-153">System.Int32</span></span>

### <span data-ttu-id="82126-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="82126-154">System.Boolean</span></span>

## <span data-ttu-id="82126-155">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="82126-155">OUTPUTS</span></span>

### <span data-ttu-id="82126-156">System. Void</span><span class="sxs-lookup"><span data-stu-id="82126-156">System.Void</span></span>

## <span data-ttu-id="82126-157">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="82126-157">NOTES</span></span>

## <span data-ttu-id="82126-158">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="82126-158">RELATED LINKS</span></span>

[<span data-ttu-id="82126-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="82126-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="82126-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="82126-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="82126-161">Regisztráció törlése – AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="82126-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


