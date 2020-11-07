---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 588e6bd1789eafeab6109d6d53ffcfa6671bb410
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671218"
---
# <span data-ttu-id="bf168-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="bf168-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="bf168-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf168-102">SYNOPSIS</span></span>
<span data-ttu-id="bf168-103">Beállítja a VMSS operációs rendszer profiljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="bf168-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="bf168-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf168-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf168-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf168-105">DESCRIPTION</span></span>
<span data-ttu-id="bf168-106">A **set-AzVmssOsProfile** parancsmag a virtuális gép méretarányának beállítása operációs rendszer profiljának tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf168-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="bf168-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf168-107">EXAMPLES</span></span>

### <span data-ttu-id="bf168-108">Példa 1: az operációs rendszer profiljának tulajdonságainak beállítása VMSS</span><span class="sxs-lookup"><span data-stu-id="bf168-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="bf168-109">Ez a parancs beállítja az operációs rendszer profiljának tulajdonságait a ContosoVMSS nevű VMSS tartozó virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="bf168-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="bf168-110">A parancs a VMSS a virtuálisgép-példányok számítógép nevének előtagját állítja be a rendszergazda felhasználónevének és jelszavának teszteléséhez és ellátásához.</span><span class="sxs-lookup"><span data-stu-id="bf168-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="bf168-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf168-111">PARAMETERS</span></span>

### <span data-ttu-id="bf168-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="bf168-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="bf168-113">Egy felügyelet nélküli tartalom-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="bf168-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="bf168-114">Az objektum létrehozásához használhatja a Add-AzVMAdditionalUnattendContent.</span><span class="sxs-lookup"><span data-stu-id="bf168-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="bf168-115">-AdminPassword</span></span>
<span data-ttu-id="bf168-116">A VMSS lévő összes virtuálisgép-példányhoz használt rendszergazdai jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf168-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="bf168-117">-AdminUsername</span></span>
<span data-ttu-id="bf168-118">Annak a rendszergazdai fióknak a nevét adja meg, amelyet a VMSS minden virtuális gép példányához használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="bf168-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="bf168-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="bf168-120">A VMSS a virtuálisgép-példányok számítógép nevének előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf168-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="bf168-121">A számítógépek nevének 1 – 15 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="bf168-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="bf168-122">-CustomData</span></span>
<span data-ttu-id="bf168-123">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="bf168-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="bf168-124">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="bf168-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="bf168-125">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="bf168-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="bf168-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf168-126">-DefaultProfile</span></span>
<span data-ttu-id="bf168-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf168-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf168-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="bf168-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="bf168-129">Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="bf168-129">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="bf168-130">-Listener</span></span>
<span data-ttu-id="bf168-131">A Windows Remote Management (WinRM) figyelőit adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf168-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="bf168-132">Ez engedélyezi a távoli Windows PowerShellt.</span><span class="sxs-lookup"><span data-stu-id="bf168-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="bf168-133">A figyelő létrehozásához használhatja a Add-AzVmssWinRMListener parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bf168-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="bf168-134">-PublicKey</span></span>
<span data-ttu-id="bf168-135">A biztonságos rendszerhéj (SSH) nyilvánoskulcs-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf168-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="bf168-136">Az objektum létrehozásához az Add-AzVMSshPublicKey parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="bf168-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-137">-Secret</span><span class="sxs-lookup"><span data-stu-id="bf168-137">-Secret</span></span>
<span data-ttu-id="bf168-138">Megadja a titok objektumot, amely a virtuális gépen elhelyezni kívánt tanúsítványra mutató hivatkozásokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="bf168-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="bf168-139">A Secrets objektumot a Add-AzVmssSecret parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="bf168-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-140">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="bf168-140">-TimeZone</span></span>
<span data-ttu-id="bf168-141">A virtuális gép időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf168-141">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bf168-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bf168-143">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf168-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="bf168-144">Az objektum létrehozásához az New-AzVmssConfig parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="bf168-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="bf168-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="bf168-146">Azt jelzi, hogy a VMSS lévő virtuális gépek engedélyezve vannak-e az automatikus frissítésekhez.</span><span class="sxs-lookup"><span data-stu-id="bf168-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="bf168-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="bf168-148">Azt jelzi, hogy a virtuális gép ügynököt kell-e kiépíteni a VMSS lévő virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="bf168-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf168-149">-Confirm</span></span>
<span data-ttu-id="bf168-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf168-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf168-151">-WhatIf</span></span>
<span data-ttu-id="bf168-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf168-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf168-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf168-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf168-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf168-154">CommonParameters</span></span>
<span data-ttu-id="bf168-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf168-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf168-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf168-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf168-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf168-157">INPUTS</span></span>

### <span data-ttu-id="bf168-158">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bf168-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="bf168-159">System. String</span><span class="sxs-lookup"><span data-stu-id="bf168-159">System.String</span></span>

### <span data-ttu-id="bf168-160">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bf168-160">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bf168-161">Microsoft. Azure. Management. számítás. models. AdditionalUnattendContent []</span><span class="sxs-lookup"><span data-stu-id="bf168-161">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="bf168-162">Microsoft. Azure. Management. számítás. models. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="bf168-162">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="bf168-163">Microsoft. Azure. Management. számítás. models. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="bf168-163">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="bf168-164">Microsoft. Azure. Management. számítás. models. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="bf168-164">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="bf168-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf168-165">OUTPUTS</span></span>

### <span data-ttu-id="bf168-166">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bf168-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="bf168-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf168-167">NOTES</span></span>

## <span data-ttu-id="bf168-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf168-168">RELATED LINKS</span></span>

[<span data-ttu-id="bf168-169">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="bf168-169">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="bf168-170">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="bf168-170">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="bf168-171">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="bf168-171">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="bf168-172">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="bf168-172">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="bf168-173">Új – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="bf168-173">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


