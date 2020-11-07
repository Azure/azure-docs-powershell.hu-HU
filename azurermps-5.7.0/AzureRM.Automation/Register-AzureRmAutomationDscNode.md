---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
ms.openlocfilehash: 614e954f4e8ec37d24495e766a139eb8a961c743
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680440"
---
# <span data-ttu-id="3d904-101">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3d904-101">Register-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="3d904-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d904-102">SYNOPSIS</span></span>
<span data-ttu-id="3d904-103">Egy Azure Virtual Machine-t DSC-csomópontként regisztrál egy automatizálási fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="3d904-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d904-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d904-104">SYNTAX</span></span>

```
Register-AzureRmAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d904-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d904-105">DESCRIPTION</span></span>
<span data-ttu-id="3d904-106">A **Register-AzureRmAutomationDscNode** parancsmag az Azure Virtual Machine-t APS típusú, APS-es típusú (DSC) csomópontként regisztrálja egy Azure automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="3d904-106">The **Register-AzureRmAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="3d904-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3d904-107">EXAMPLES</span></span>

### <span data-ttu-id="3d904-108">1. példa: az Azure Virtual Machine-t Azure DSC-csomópontként regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="3d904-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="3d904-109">Ez a parancs a VirtualMachine01 nevű Azure virtuális gépet DSC-csomópontként regisztrálja az Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="3d904-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3d904-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d904-110">PARAMETERS</span></span>

### <span data-ttu-id="3d904-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="3d904-111">-ActionAfterReboot</span></span>
<span data-ttu-id="3d904-112">Meghatározza, hogy a virtuális gép milyen műveleteket hajtson végre az újraindítás után.</span><span class="sxs-lookup"><span data-stu-id="3d904-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="3d904-113">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="3d904-113">Valid values are:</span></span> 

- <span data-ttu-id="3d904-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d904-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="3d904-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d904-115">StopConfiguration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="3d904-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="3d904-117">Itt adhatja meg, hogy a DSC-csomópont által az Azure automatizálási kiszolgálóról letöltött új konfigurációk felülírják-e a meglévő, már a cél csomóponton lévő modulokat.</span><span class="sxs-lookup"><span data-stu-id="3d904-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3d904-118">-AutomationAccountName</span></span>
<span data-ttu-id="3d904-119">Annak az automatizálási fióknak a nevét adja meg, amelyben a parancsmag a virtuális gépet regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="3d904-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="3d904-120">-AzureVMLocation</span></span>
<span data-ttu-id="3d904-121">Azt a helyet adja meg, ahol ez a parancsmag virtuális gépet rögzít.</span><span class="sxs-lookup"><span data-stu-id="3d904-121">Specifies the location in which this cmdlet registers a virtual machine.</span></span>
<span data-ttu-id="3d904-122">Ha érvényes helyeket szeretne beolvasni, használja az Get-AzureRMLocation parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3d904-122">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-123">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="3d904-123">-AzureVMName</span></span>
<span data-ttu-id="3d904-124">Annak az Azure virtuális gépnek a nevét adja meg, amelyre a parancsmag a felügyeletet regisztrálja.</span><span class="sxs-lookup"><span data-stu-id="3d904-124">Specifies the name of the Azure virtual machine that this cmdlet registers for management.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-125">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3d904-125">-AzureVMResourceGroup</span></span>
<span data-ttu-id="3d904-126">Annak az Azure Virtual Machine-csoportnak a nevét adja meg, amelyre a parancsmag van regisztrálva.</span><span class="sxs-lookup"><span data-stu-id="3d904-126">Specifies the name of the resource group of the Azure virtual machine that this cmdlet registers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-127">-Állítsa ConfigurationMode kulcsot</span><span class="sxs-lookup"><span data-stu-id="3d904-127">-ConfigurationMode</span></span>
<span data-ttu-id="3d904-128">A DSC konfigurációs üzemmódját adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d904-128">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="3d904-129">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="3d904-129">Valid values are:</span></span> 

- <span data-ttu-id="3d904-130">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="3d904-130">ApplyAndMonitor</span></span> 
- <span data-ttu-id="3d904-131">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="3d904-131">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="3d904-132">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="3d904-132">ApplyOnly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-133">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="3d904-133">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="3d904-134">Annak gyakoriságát adja meg percben, amikor a DSC háttér-alkalmazása megkísérli végrehajtani a jelenlegi konfigurációt a cél csomóponton.</span><span class="sxs-lookup"><span data-stu-id="3d904-134">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d904-135">-DefaultProfile</span></span>
<span data-ttu-id="3d904-136">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="3d904-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-137">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3d904-137">-NodeConfigurationName</span></span>
<span data-ttu-id="3d904-138">Itt adhatja meg annak a csomópont-konfigurációnak a nevét, amelyet a parancsmag a virtuális gépet az Azure automatizálási DSC-ről való kihúzásra állít be.</span><span class="sxs-lookup"><span data-stu-id="3d904-138">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-139">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="3d904-139">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="3d904-140">Megadja, hogy szükség esetén újra kell-e indítani a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="3d904-140">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-141">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="3d904-141">-RefreshFrequencyMins</span></span>
<span data-ttu-id="3d904-142">Annak gyakoriságát adja meg percben, amikor a helyi Konfigurációkezelő az Azure automatizálás DSC lekérési kiszolgálójának segítségével letölti a legújabb csomópont-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="3d904-142">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d904-143">-ResourceGroupName</span></span>
<span data-ttu-id="3d904-144">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d904-144">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3d904-145">Az automatizálási fiók, amellyel a parancsmag a virtuális gépet regisztrálja, a paraméter által megadott erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="3d904-145">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d904-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d904-146">CommonParameters</span></span>
<span data-ttu-id="3d904-147">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d904-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d904-148">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d904-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d904-149">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d904-149">INPUTS</span></span>

### <span data-ttu-id="3d904-150">Nincs</span><span class="sxs-lookup"><span data-stu-id="3d904-150">None</span></span>
<span data-ttu-id="3d904-151">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3d904-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d904-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d904-152">OUTPUTS</span></span>

## <span data-ttu-id="3d904-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d904-153">NOTES</span></span>

## <span data-ttu-id="3d904-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d904-154">RELATED LINKS</span></span>

[<span data-ttu-id="3d904-155">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3d904-155">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="3d904-156">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3d904-156">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="3d904-157">Regisztráció törlése – AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3d904-157">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


