---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938273"
---
# <span data-ttu-id="fc84b-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="fc84b-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="fc84b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc84b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc84b-103">Beállítja az operációs rendszer tulajdonságait egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="fc84b-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="fc84b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fc84b-104">SYNTAX</span></span>

### <span data-ttu-id="fc84b-105">Windows (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="fc84b-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc84b-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="fc84b-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc84b-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="fc84b-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc84b-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="fc84b-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc84b-109">Linux</span><span class="sxs-lookup"><span data-stu-id="fc84b-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc84b-110">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fc84b-110">DESCRIPTION</span></span>
<span data-ttu-id="fc84b-111">A **Set-AzVMOperatingSystem** parancsmag beállítja egy virtuális gép operációs rendszerének tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="fc84b-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="fc84b-112">Megadhatja a bejelentkezési hitelesítő adatokat, a számítógép nevét és az operációs rendszer típusát.</span><span class="sxs-lookup"><span data-stu-id="fc84b-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="fc84b-113">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fc84b-113">EXAMPLES</span></span>

### <span data-ttu-id="fc84b-114">1. példa: Az operációs rendszer tulajdonságainak beállítása új virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="fc84b-114">Example 1: Set operating system properties for a new virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="fc84b-115">Az első parancs biztonságos karakterláncra konvertálja a jelszót, majd tárolja azt a $SecurePassword változóban.</span><span class="sxs-lookup"><span data-stu-id="fc84b-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="fc84b-116">További információért írja be a `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="fc84b-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="fc84b-117">A második parancs létrehoz egy hitelesítő adatokat a felhasználó FullerP-hez és a $SecurePassword-ban tárolt jelszóhoz, majd a hitelesítő adatokat a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc84b-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="fc84b-118">További információért írja be a `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="fc84b-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="fc84b-119">A harmadik parancs az Erőforráscsoport11 erőforráscsoportBan az AvailabilitySet03 nevű elérhetőségi halmazt kapja meg, majd az objektumot a $AvailabilitySet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc84b-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="fc84b-120">A negyedik parancs létrehoz egy virtuális gépobjektumot, majd tárolja azt a $VirtualMachine változóban.</span><span class="sxs-lookup"><span data-stu-id="fc84b-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="fc84b-121">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="fc84b-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="fc84b-122">A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="fc84b-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="fc84b-123">A következő négy parancs értékeket rendel a változókhoz, amelyek az alábbi parancsban használhatók.</span><span class="sxs-lookup"><span data-stu-id="fc84b-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="fc84b-124">Mivel ezeket a karakterláncokat közvetlenül a **Set-AzVMOperatingSystem** parancsban is megadhatja, ezt a módszert csak az olvashatóság érdekében használjuk.</span><span class="sxs-lookup"><span data-stu-id="fc84b-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="fc84b-125">A parancsfájlok azonban ehhez hasonló módszert is használhatnak.</span><span class="sxs-lookup"><span data-stu-id="fc84b-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="fc84b-126">Az utolsó parancs beállítja az operációs rendszer tulajdonságait a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fc84b-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="fc84b-127">A parancs a $Credential.</span><span class="sxs-lookup"><span data-stu-id="fc84b-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="fc84b-128">A parancs bizonyos paraméterekhez a korábbi parancsokban hozzárendelt változókat használja.</span><span class="sxs-lookup"><span data-stu-id="fc84b-128">The command uses variables assigned in previous commands for some parameters.</span></span>

### <span data-ttu-id="fc84b-129">2. példa: Új virtuális gép operációs rendszerének tulajdonságainak beállítása engedélyezett gyorsjavítással</span><span class="sxs-lookup"><span data-stu-id="fc84b-129">Example 2: Set operating system properties for a new virtual machine with hot patching enabled</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

<span data-ttu-id="fc84b-130">Az első parancs biztonságos karakterláncra konvertálja a jelszót, majd tárolja azt a $SecurePassword változóban.</span><span class="sxs-lookup"><span data-stu-id="fc84b-130">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="fc84b-131">További információért írja be a `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="fc84b-131">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="fc84b-132">A második parancs létrehoz egy hitelesítő adatokat a felhasználó FullerP-hez és a $SecurePassword-ban tárolt jelszóhoz, majd a hitelesítő adatokat a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc84b-132">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="fc84b-133">További információért írja be a `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="fc84b-133">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="fc84b-134">A harmadik parancs az Erőforráscsoport11 erőforráscsoportBan az AvailabilitySet03 nevű elérhetőségi halmazt kapja meg, majd az objektumot a $AvailabilitySet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc84b-134">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="fc84b-135">A negyedik parancs létrehoz egy virtuális gépobjektumot, majd tárolja azt a $VirtualMachine változóban.</span><span class="sxs-lookup"><span data-stu-id="fc84b-135">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="fc84b-136">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="fc84b-136">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="fc84b-137">A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="fc84b-137">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="fc84b-138">A következő négy parancs értékeket rendel a változókhoz, amelyek az alábbi parancsban használhatók.</span><span class="sxs-lookup"><span data-stu-id="fc84b-138">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="fc84b-139">Mivel ezeket a karakterláncokat közvetlenül a **Set-AzVMOperatingSystem** parancsban is megadhatja, ezt a módszert csak az olvashatóság érdekében használjuk.</span><span class="sxs-lookup"><span data-stu-id="fc84b-139">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="fc84b-140">A parancsfájlok azonban ehhez hasonló módszert is használhatnak.</span><span class="sxs-lookup"><span data-stu-id="fc84b-140">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="fc84b-141">Az utolsó parancs beállítja az operációs rendszer tulajdonságait a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fc84b-141">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="fc84b-142">A parancs a $Credential.</span><span class="sxs-lookup"><span data-stu-id="fc84b-142">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="fc84b-143">A parancs bizonyos paraméterekhez a korábbi parancsokban hozzárendelt változókat használja.</span><span class="sxs-lookup"><span data-stu-id="fc84b-143">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="fc84b-144">A parancs engedélyezi a gyorsjavítást a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="fc84b-144">The command enables Hotpatching on the virtual machine.</span></span>

### <span data-ttu-id="fc84b-145">3. példa: Az operációs rendszer tulajdonságainak beállítása új Linux-virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="fc84b-145">Example 3: Set operating system properties for a new Linux virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="fc84b-146">Az első parancs biztonságos karakterláncra konvertálja a jelszót, majd tárolja azt a $SecurePassword változóban.</span><span class="sxs-lookup"><span data-stu-id="fc84b-146">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="fc84b-147">További információért írja be a `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="fc84b-147">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="fc84b-148">A második parancs létrehoz egy hitelesítő adatokat a felhasználó FullerP-hez és a $SecurePassword-ban tárolt jelszóhoz, majd a hitelesítő adatokat a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc84b-148">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="fc84b-149">További információért írja be a `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="fc84b-149">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="fc84b-150">A harmadik parancs az Erőforráscsoport11 erőforráscsoportBan az AvailabilitySet03 nevű elérhetőségi halmazt kapja meg, majd az objektumot a $AvailabilitySet változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="fc84b-150">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="fc84b-151">A negyedik parancs létrehoz egy virtuális gépobjektumot, majd tárolja azt a $VirtualMachine változóban.</span><span class="sxs-lookup"><span data-stu-id="fc84b-151">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="fc84b-152">A parancs nevet és méretet rendel a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="fc84b-152">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="fc84b-153">A virtuális gép a 2016-ban tárolt rendelkezésre állási $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="fc84b-153">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="fc84b-154">A következő két parancs értékeket rendel a változókhoz, amelyek az alábbi parancsban használhatók.</span><span class="sxs-lookup"><span data-stu-id="fc84b-154">The next two commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="fc84b-155">Az utolsó parancs beállítja az operációs rendszer tulajdonságait a $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="fc84b-155">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="fc84b-156">A parancs a $Credential.</span><span class="sxs-lookup"><span data-stu-id="fc84b-156">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="fc84b-157">A parancs bizonyos paraméterekhez a korábbi parancsokban hozzárendelt változókat használja.</span><span class="sxs-lookup"><span data-stu-id="fc84b-157">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="fc84b-158">A parancs beállítja a javítás mód értékét a virtuális gépen az "AutomaticByPlatform" értékre.</span><span class="sxs-lookup"><span data-stu-id="fc84b-158">The command sets the patch mode value on the virtual machine to "AutomaticByPlatform".</span></span>

## <span data-ttu-id="fc84b-159">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc84b-159">PARAMETERS</span></span>

### <span data-ttu-id="fc84b-160">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="fc84b-160">-ComputerName</span></span>
<span data-ttu-id="fc84b-161">A számítógép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc84b-161">Specifies the name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-162">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="fc84b-162">-Credential</span></span>
<span data-ttu-id="fc84b-163">A virtuális gép felhasználónevét és jelszavát adja meg **PSCredential objektumként.**</span><span class="sxs-lookup"><span data-stu-id="fc84b-163">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="fc84b-164">Hitelesítő adatok beszerzéséhez használja a Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fc84b-164">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="fc84b-165">További információért írja be a `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="fc84b-165">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-166">-CustomData</span><span class="sxs-lookup"><span data-stu-id="fc84b-166">-CustomData</span></span>
<span data-ttu-id="fc84b-167">Megadja a virtuális gépnek át adható karakterláncot.</span><span class="sxs-lookup"><span data-stu-id="fc84b-167">Specifies a string to be passed to the virtual machine.</span></span> <span data-ttu-id="fc84b-168">További információt az [Azure-alapú virtuális gépek egyéni adataiban található.](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data)</span><span class="sxs-lookup"><span data-stu-id="fc84b-168">For more information see [Custom Data on Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data).</span></span>
<span data-ttu-id="fc84b-169">**Megjegyzés: Nem ajánlott bizalmas adatokat egyéni adatokban tárolni.**</span><span class="sxs-lookup"><span data-stu-id="fc84b-169">**Note: It is not recommended to store sensitive information in custom data.**</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc84b-170">-DefaultProfile</span></span>
<span data-ttu-id="fc84b-171">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fc84b-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc84b-172">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="fc84b-172">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="fc84b-173">Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="fc84b-173">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-174">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="fc84b-174">-DisableVMAgent</span></span>
<span data-ttu-id="fc84b-175">Tiltsa le a Virtuális gép kiépítési ügynökének funkcióját.</span><span class="sxs-lookup"><span data-stu-id="fc84b-175">Disable Provision VM Agent.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-176">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="fc84b-176">-EnableAutoUpdate</span></span>
<span data-ttu-id="fc84b-177">Azt jelzi, hogy ez a parancsmag engedélyezi az automatikus frissítést.</span><span class="sxs-lookup"><span data-stu-id="fc84b-177">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-178">-EnableHotpatching</span><span class="sxs-lookup"><span data-stu-id="fc84b-178">-EnableHotpatching</span></span>
<span data-ttu-id="fc84b-179">Lehetővé teszi az ügyfeleknek, hogy újraindítás nélkül javítják az Azure-virtuális gépeiket.</span><span class="sxs-lookup"><span data-stu-id="fc84b-179">Enables customers to patch their Azure VMs without requiring a reboot.</span></span> <span data-ttu-id="fc84b-180">Az enableHotpatching engedélyezéséhez a "provisionVMAgent" értéknek igazra, a "patchMode" pedig az "AutomaticByPlatform" értékre kell állítania.</span><span class="sxs-lookup"><span data-stu-id="fc84b-180">For enableHotpatching, the 'provisionVMAgent' must be set to true and 'patchMode' must be set to 'AutomaticByPlatform'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-181">-Linux</span><span class="sxs-lookup"><span data-stu-id="fc84b-181">-Linux</span></span>
<span data-ttu-id="fc84b-182">Azt jelzi, hogy az operációs rendszer típusa Linux.</span><span class="sxs-lookup"><span data-stu-id="fc84b-182">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-183">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="fc84b-183">-PatchMode</span></span>
<span data-ttu-id="fc84b-184">A vendégen keresztüli javítás módja az IaaS virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="fc84b-184">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="fc84b-185">Lehetséges értékek:</span><span class="sxs-lookup"><span data-stu-id="fc84b-185">Possible values are:</span></span><br>
<span data-ttu-id="fc84b-186">**Kézi** – Ön szabályozhatja a javítások virtuális gépre való alkalmazását.</span><span class="sxs-lookup"><span data-stu-id="fc84b-186">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="fc84b-187">Ehhez manuálisan kell telepítenie a javításokat a VM-en belül.</span><span class="sxs-lookup"><span data-stu-id="fc84b-187">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="fc84b-188">Ebben a módban az automatikus frissítések le vannak tiltva; A WindowsConfiguration.enableAutomaticUpdates tulajdonságnak hamisnak kell lennie</span><span class="sxs-lookup"><span data-stu-id="fc84b-188">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="fc84b-189">**AutomaticByOS** – A virtuális gépet automatikusan frissíti az operációs rendszer.</span><span class="sxs-lookup"><span data-stu-id="fc84b-189">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="fc84b-190">A WindowsConfiguration.enableAutomaticUpdates tulajdonságnak igaznak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="fc84b-190">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="fc84b-191">**AutomaticByPlatform** – a virtuális gépet automatikusan frissíti az operációs rendszer.</span><span class="sxs-lookup"><span data-stu-id="fc84b-191">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="fc84b-192">A provisionVMAgent és a WindowsConfiguration.enableAutomaticUpdates tulajdonságnak teljesülnie kell</span><span class="sxs-lookup"><span data-stu-id="fc84b-192">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

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

### <span data-ttu-id="fc84b-193">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="fc84b-193">-ProvisionVMAgent</span></span>
<span data-ttu-id="fc84b-194">Azt jelzi, hogy a beállításokhoz telepíteni kell a virtuális gép ügynökét a virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="fc84b-194">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-195">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="fc84b-195">-TimeZone</span></span>
<span data-ttu-id="fc84b-196">A virtuális gép időzónáját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="fc84b-196">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="fc84b-197">például a \" csendes-óceáni téli \" idő.</span><span class="sxs-lookup"><span data-stu-id="fc84b-197">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="fc84b-198">A lehetséges értékek a [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones) [által visszaadott](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) időzónákból származó TimeZoneInfo.Id is beállíthatók.</span><span class="sxs-lookup"><span data-stu-id="fc84b-198">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-199">-VM</span><span class="sxs-lookup"><span data-stu-id="fc84b-199">-VM</span></span>
<span data-ttu-id="fc84b-200">Azt a helyi virtuális gépobjektumot adja meg, amelyen meg kell állítani az operációs rendszer tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="fc84b-200">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="fc84b-201">Virtuális gépi objektum beszerzéséhez használja a Get-AzVM parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="fc84b-201">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="fc84b-202">Virtuális gépi objektum létrehozása a New-AzVMConfig parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="fc84b-202">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-203">-Windows</span><span class="sxs-lookup"><span data-stu-id="fc84b-203">-Windows</span></span>
<span data-ttu-id="fc84b-204">Azt jelzi, hogy az operációs rendszer típusa Windows.</span><span class="sxs-lookup"><span data-stu-id="fc84b-204">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-205">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="fc84b-205">-WinRMCertificateUrl</span></span>
<span data-ttu-id="fc84b-206">Egy WinRM-tanúsítvány URI-ját adja meg.</span><span class="sxs-lookup"><span data-stu-id="fc84b-206">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="fc84b-207">Ezt egy kulcstárolóban kell tárolni.</span><span class="sxs-lookup"><span data-stu-id="fc84b-207">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-208">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="fc84b-208">-WinRMHttp</span></span>
<span data-ttu-id="fc84b-209">Azt jelzi, hogy az operációs rendszer HTTP WinRM-et használ.</span><span class="sxs-lookup"><span data-stu-id="fc84b-209">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-210">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="fc84b-210">-WinRMHttps</span></span>
<span data-ttu-id="fc84b-211">Azt jelzi, hogy ez az operációs rendszer HTTPS WinRM-et használ.</span><span class="sxs-lookup"><span data-stu-id="fc84b-211">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc84b-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc84b-212">CommonParameters</span></span>
<span data-ttu-id="fc84b-213">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc84b-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc84b-214">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc84b-214">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc84b-215">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fc84b-215">INPUTS</span></span>

### <span data-ttu-id="fc84b-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fc84b-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="fc84b-217">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fc84b-217">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fc84b-218">System.String</span><span class="sxs-lookup"><span data-stu-id="fc84b-218">System.String</span></span>

### <span data-ttu-id="fc84b-219">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="fc84b-219">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="fc84b-220">System.Uri</span><span class="sxs-lookup"><span data-stu-id="fc84b-220">System.Uri</span></span>

## <span data-ttu-id="fc84b-221">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fc84b-221">OUTPUTS</span></span>

### <span data-ttu-id="fc84b-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="fc84b-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="fc84b-223">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fc84b-223">NOTES</span></span>

## <span data-ttu-id="fc84b-224">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fc84b-224">RELATED LINKS</span></span>

[<span data-ttu-id="fc84b-225">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="fc84b-225">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="fc84b-226">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="fc84b-226">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


