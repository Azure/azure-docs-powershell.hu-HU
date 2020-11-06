---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
ms.openlocfilehash: 45deca60451f79dd0d20a0b1238f32e91d8ef2ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496291"
---
# <span data-ttu-id="26070-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="26070-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="26070-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="26070-102">SYNOPSIS</span></span>
<span data-ttu-id="26070-103">Beállítja a VMSS operációs rendszer profiljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="26070-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26070-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="26070-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26070-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="26070-105">DESCRIPTION</span></span>
<span data-ttu-id="26070-106">A **set-AzureRmVmssOsProfile** parancsmag a virtuális gép méretarányának beállítása operációs rendszer profiljának tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="26070-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="26070-107">Példák</span><span class="sxs-lookup"><span data-stu-id="26070-107">EXAMPLES</span></span>

### <span data-ttu-id="26070-108">Példa 1: az operációs rendszer profiljának tulajdonságainak beállítása VMSS</span><span class="sxs-lookup"><span data-stu-id="26070-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="26070-109">Ez a parancs beállítja az operációs rendszer profiljának tulajdonságait a ContosoVMSS nevű VMSS tartozó virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="26070-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="26070-110">A parancs a VMSS a virtuálisgép-példányok számítógép nevének előtagját állítja be a rendszergazda felhasználónevének és jelszavának teszteléséhez és ellátásához.</span><span class="sxs-lookup"><span data-stu-id="26070-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="26070-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="26070-111">PARAMETERS</span></span>

### <span data-ttu-id="26070-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="26070-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="26070-113">Egy felügyelet nélküli tartalom-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="26070-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="26070-114">Az objektum létrehozásához használhatja a Add-AzureRmVMAdditionalUnattendContent.</span><span class="sxs-lookup"><span data-stu-id="26070-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="26070-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="26070-115">-AdminPassword</span></span>
<span data-ttu-id="26070-116">A VMSS lévő összes virtuálisgép-példányhoz használt rendszergazdai jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="26070-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="26070-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="26070-117">-AdminUsername</span></span>
<span data-ttu-id="26070-118">Annak a rendszergazdai fióknak a nevét adja meg, amelyet a VMSS minden virtuális gép példányához használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="26070-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="26070-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="26070-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="26070-120">A VMSS a virtuálisgép-példányok számítógép nevének előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="26070-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="26070-121">A számítógépek nevének 1 – 15 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="26070-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="26070-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="26070-122">-CustomData</span></span>
<span data-ttu-id="26070-123">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="26070-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="26070-124">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="26070-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="26070-125">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="26070-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="26070-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26070-126">-DefaultProfile</span></span>
<span data-ttu-id="26070-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="26070-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26070-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="26070-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="26070-129">Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="26070-129">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="26070-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="26070-130">-Listener</span></span>
<span data-ttu-id="26070-131">A Windows Remote Management (WinRM) figyelőit adja meg.</span><span class="sxs-lookup"><span data-stu-id="26070-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="26070-132">Ez engedélyezi a távoli Windows PowerShellt.</span><span class="sxs-lookup"><span data-stu-id="26070-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="26070-133">A figyelő létrehozásához használhatja a Add-AzureRmVmssWinRMListener parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="26070-133">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="26070-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="26070-134">-PublicKey</span></span>
<span data-ttu-id="26070-135">A biztonságos rendszerhéj (SSH) nyilvánoskulcs-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="26070-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="26070-136">Az objektum létrehozásához az Add-AzureRmVMSshPublicKey parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="26070-136">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="26070-137">-Secret</span><span class="sxs-lookup"><span data-stu-id="26070-137">-Secret</span></span>
<span data-ttu-id="26070-138">Megadja a titok objektumot, amely a virtuális gépen elhelyezni kívánt tanúsítványra mutató hivatkozásokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="26070-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="26070-139">A Secrets objektumot a Add-AzureRmVmssSecret parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="26070-139">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="26070-140">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="26070-140">-TimeZone</span></span>
<span data-ttu-id="26070-141">A virtuális gép időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="26070-141">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="26070-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="26070-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="26070-143">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="26070-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="26070-144">Az objektum létrehozásához az New-AzureRmVmssConfig parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="26070-144">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="26070-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="26070-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="26070-146">Azt jelzi, hogy a VMSS lévő virtuális gépek engedélyezve vannak-e az automatikus frissítésekhez.</span><span class="sxs-lookup"><span data-stu-id="26070-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="26070-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="26070-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="26070-148">Azt jelzi, hogy a virtuális gép ügynököt kell-e kiépíteni a VMSS lévő virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="26070-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="26070-149">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="26070-149">-Confirm</span></span>
<span data-ttu-id="26070-150">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="26070-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26070-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26070-151">-WhatIf</span></span>
<span data-ttu-id="26070-152">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="26070-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26070-153">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="26070-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26070-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26070-154">CommonParameters</span></span>
<span data-ttu-id="26070-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="26070-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26070-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26070-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26070-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="26070-157">INPUTS</span></span>

### <span data-ttu-id="26070-158">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="26070-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="26070-159">System. String</span><span class="sxs-lookup"><span data-stu-id="26070-159">System.String</span></span>

### <span data-ttu-id="26070-160">System. null ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="26070-160">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="26070-161">Microsoft. Azure. Management. számítás. models. AdditionalUnattendContent []</span><span class="sxs-lookup"><span data-stu-id="26070-161">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="26070-162">Microsoft. Azure. Management. számítás. models. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="26070-162">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="26070-163">Microsoft. Azure. Management. számítás. models. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="26070-163">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="26070-164">Microsoft. Azure. Management. számítás. models. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="26070-164">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="26070-165">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26070-165">OUTPUTS</span></span>

### <span data-ttu-id="26070-166">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="26070-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="26070-167">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="26070-167">NOTES</span></span>

## <span data-ttu-id="26070-168">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26070-168">RELATED LINKS</span></span>

[<span data-ttu-id="26070-169">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="26070-169">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="26070-170">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="26070-170">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="26070-171">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="26070-171">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="26070-172">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="26070-172">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="26070-173">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="26070-173">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


