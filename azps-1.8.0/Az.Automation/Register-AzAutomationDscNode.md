---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5dc2682597be6f05a65bafc38424139e9707578f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671548"
---
# <span data-ttu-id="6f1c6-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="6f1c6-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="6f1c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f1c6-102">SYNOPSIS</span></span>
<span data-ttu-id="6f1c6-103">Egy Azure Virtual Machine-t DSC-csomópontként regisztrál egy automatizálási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="6f1c6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f1c6-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f1c6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f1c6-105">DESCRIPTION</span></span>
<span data-ttu-id="6f1c6-106">A **Register-AzAutomationDscNode** parancsmag az Azure Virtual Machine-t APS típusú, APS-es típusú (DSC) csomópontként regisztrálja egy Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="6f1c6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6f1c6-107">EXAMPLES</span></span>

### <span data-ttu-id="6f1c6-108">1. példa: az Azure Virtual Machine-t Azure DSC-csomópontként regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="6f1c6-109">Ez a parancs a VirtualMachine01 nevű Azure virtuális gépet DSC-csomópontként regisztrálja az Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6f1c6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f1c6-110">PARAMETERS</span></span>

### <span data-ttu-id="6f1c6-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="6f1c6-111">-ActionAfterReboot</span></span>
<span data-ttu-id="6f1c6-112">Meghatározza, hogy a virtuális gép milyen műveleteket hajtson végre az újraindítás után.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="6f1c6-113">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="6f1c6-113">Valid values are:</span></span> 
- <span data-ttu-id="6f1c6-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f1c6-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="6f1c6-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f1c6-115">StopConfiguration</span></span>

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

### <span data-ttu-id="6f1c6-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="6f1c6-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="6f1c6-117">Itt adhatja meg, hogy a DSC-csomópont által az Azure automatizálási kiszolgálóról letöltött új konfigurációk felülírják-e a meglévő, már a cél csomóponton lévő modulokat.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="6f1c6-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f1c6-118">-AutomationAccountName</span></span>
<span data-ttu-id="6f1c6-119">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag a virtuális gépet regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="6f1c6-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="6f1c6-120">-AzureVMLocation</span></span>
<span data-ttu-id="6f1c6-121">Az Azure VM helyszíne.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-121">The Azure VM location.</span></span>

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

### <span data-ttu-id="6f1c6-122">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="6f1c6-122">-AzureVMName</span></span>
<span data-ttu-id="6f1c6-123">Annak az Azure Virtual Machine-gépnek a neve, amely az Azure Automation DSC-vel való kezelésre szolgál.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-123">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="6f1c6-124">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6f1c6-124">-AzureVMResourceGroup</span></span>
<span data-ttu-id="6f1c6-125">Az Azure VM-erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-125">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="6f1c6-126">-Állítsa ConfigurationMode kulcsot</span><span class="sxs-lookup"><span data-stu-id="6f1c6-126">-ConfigurationMode</span></span>
<span data-ttu-id="6f1c6-127">A DSC konfigurációs üzemmódját adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-127">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="6f1c6-128">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="6f1c6-128">Valid values are:</span></span> 
- <span data-ttu-id="6f1c6-129">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="6f1c6-129">ApplyAndMonitor</span></span> 
- <span data-ttu-id="6f1c6-130">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="6f1c6-130">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="6f1c6-131">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="6f1c6-131">ApplyOnly</span></span>

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

### <span data-ttu-id="6f1c6-132">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="6f1c6-132">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="6f1c6-133">Annak gyakoriságát adja meg percben, amikor a DSC háttér-alkalmazása megkísérli végrehajtani a jelenlegi konfigurációt a cél csomóponton.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-133">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="6f1c6-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f1c6-134">-DefaultProfile</span></span>
<span data-ttu-id="6f1c6-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="6f1c6-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f1c6-136">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6f1c6-136">-NodeConfigurationName</span></span>
<span data-ttu-id="6f1c6-137">Itt adhatja meg annak a csomópont-konfigurációnak a nevét, amelyet a parancsmag a virtuális gépet az Azure automatizálási DSC-ről való kihúzásra állít be.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-137">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="6f1c6-138">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="6f1c6-138">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="6f1c6-139">Megadja, hogy szükség esetén újra kell-e indítani a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-139">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="6f1c6-140">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="6f1c6-140">-RefreshFrequencyMins</span></span>
<span data-ttu-id="6f1c6-141">Annak gyakoriságát adja meg percben, amikor a helyi Konfigurációkezelő az Azure automatizálás DSC lekérési kiszolgálójának segítségével letölti a legújabb csomópont-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-141">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="6f1c6-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f1c6-142">-ResourceGroupName</span></span>
<span data-ttu-id="6f1c6-143">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6f1c6-144">Az automatizálási fiók, amellyel a parancsmag a virtuális gépet regisztrálja, a paraméter által megadott erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="6f1c6-144">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="6f1c6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f1c6-145">CommonParameters</span></span>
<span data-ttu-id="6f1c6-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f1c6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f1c6-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f1c6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f1c6-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f1c6-148">INPUTS</span></span>

### <span data-ttu-id="6f1c6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6f1c6-149">System.String</span></span>

### <span data-ttu-id="6f1c6-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6f1c6-150">System.Int32</span></span>

### <span data-ttu-id="6f1c6-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f1c6-151">System.Boolean</span></span>

## <span data-ttu-id="6f1c6-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f1c6-152">OUTPUTS</span></span>

### <span data-ttu-id="6f1c6-153">System. Void</span><span class="sxs-lookup"><span data-stu-id="6f1c6-153">System.Void</span></span>

## <span data-ttu-id="6f1c6-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f1c6-154">NOTES</span></span>

## <span data-ttu-id="6f1c6-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f1c6-155">RELATED LINKS</span></span>

[<span data-ttu-id="6f1c6-156">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="6f1c6-156">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="6f1c6-157">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="6f1c6-157">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="6f1c6-158">Regisztráció törlése – AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="6f1c6-158">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


