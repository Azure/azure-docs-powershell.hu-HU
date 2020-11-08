---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025716"
---
# <span data-ttu-id="65032-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="65032-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="65032-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65032-102">SYNOPSIS</span></span>
<span data-ttu-id="65032-103">Beállítja a VMSS operációs rendszer profiljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="65032-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="65032-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65032-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65032-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="65032-105">DESCRIPTION</span></span>
<span data-ttu-id="65032-106">A **set-AzVmssOsProfile** parancsmag a virtuális gép méretarányának beállítása operációs rendszer profiljának tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="65032-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="65032-107">Példák</span><span class="sxs-lookup"><span data-stu-id="65032-107">EXAMPLES</span></span>

### <span data-ttu-id="65032-108">Példa 1: az operációs rendszer profiljának tulajdonságainak beállítása VMSS</span><span class="sxs-lookup"><span data-stu-id="65032-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="65032-109">Ez a parancs beállítja az operációs rendszer profiljának tulajdonságait a ContosoVMSS nevű VMSS tartozó virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="65032-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="65032-110">A parancs a VMSS a virtuálisgép-példányok számítógép nevének előtagját állítja be a rendszergazda felhasználónevének és jelszavának teszteléséhez és ellátásához.</span><span class="sxs-lookup"><span data-stu-id="65032-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="65032-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65032-111">PARAMETERS</span></span>

### <span data-ttu-id="65032-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="65032-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="65032-113">Egy felügyelet nélküli tartalom-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="65032-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="65032-114">Az objektum létrehozásához használhatja a Add-AzVMAdditionalUnattendContent.</span><span class="sxs-lookup"><span data-stu-id="65032-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="65032-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="65032-115">-AdminPassword</span></span>
<span data-ttu-id="65032-116">A VMSS lévő összes virtuálisgép-példányhoz használt rendszergazdai jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="65032-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="65032-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="65032-117">-AdminUsername</span></span>
<span data-ttu-id="65032-118">Annak a rendszergazdai fióknak a nevét adja meg, amelyet a VMSS minden virtuális gép példányához használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="65032-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="65032-119">**Csak Windows korlátozás:** Nem lehet befejezni \" .\"</span><span class="sxs-lookup"><span data-stu-id="65032-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="65032-120">Nem **engedélyezett értékek:** \" rendszergazda \" , \" rendszergazda \" , \" felhasználó \" , \" Felhasználó1 \" , \" teszt \" , \" USER2 \" , \" test1 \" , \" user3 \" , \" Rendszergazda1 \" , \" 1 \" , \" 123 \" , \" a \" , \" actuser, a, admin2,, \" test2, \" ASPNET, \" \" test3 \" , \" ASPNET \" , \" Backup \" , \" Console \" , \" \" \" Guest \" , \" John \" , Owner, \" \" \" root \" , \" Server \" , \" SQL \" , \" support \" support_388945a0, \" \" , \" sys \" , \" user4 \" , \" user5 \" \" \" \" \" ,</span><span class="sxs-lookup"><span data-stu-id="65032-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="65032-121">**Minimális hosszúságú (Linux):** 1 karakter</span><span class="sxs-lookup"><span data-stu-id="65032-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="65032-122">**Max-length (Linux):** 64 karakterek</span><span class="sxs-lookup"><span data-stu-id="65032-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="65032-123">**Max-length (Windows):** 20 karakter</span><span class="sxs-lookup"><span data-stu-id="65032-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="65032-124">A Linux VM eléréséhez a [root-jogosultságok használata az Azure-alapú virtuális gépeken](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)című témakörben tájékozódhat.</span><span class="sxs-lookup"><span data-stu-id="65032-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="65032-125">A Linuxban nem használható beépített rendszerfelhasználók listáját a következő témakörben találhatja meg: a [felhasználónevek kiválasztása a Linux rendszerhez az Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)rendszerében.</span><span class="sxs-lookup"><span data-stu-id="65032-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="65032-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="65032-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="65032-127">A VMSS a virtuálisgép-példányok számítógép nevének előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="65032-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="65032-128">A számítógépek nevének 1 – 15 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="65032-128">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="65032-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="65032-129">-CustomData</span></span>
<span data-ttu-id="65032-130">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="65032-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="65032-131">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="65032-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="65032-132">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="65032-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="65032-133">Ha a VM rendszerhez a Cloud-init-ot szeretné használni, akkor olvassa el a következő témakört: a [Felhőbeli init használata a Linux VM testreszabására](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="65032-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="65032-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65032-134">-DefaultProfile</span></span>
<span data-ttu-id="65032-135">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65032-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65032-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="65032-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="65032-137">Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="65032-137">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="65032-138">-Listener</span><span class="sxs-lookup"><span data-stu-id="65032-138">-Listener</span></span>
<span data-ttu-id="65032-139">A Windows Remote Management (WinRM) figyelőit adja meg.</span><span class="sxs-lookup"><span data-stu-id="65032-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="65032-140">Ez engedélyezi a távoli Windows PowerShellt.</span><span class="sxs-lookup"><span data-stu-id="65032-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="65032-141">A figyelő létrehozásához használhatja a Add-AzVmssWinRMListener parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="65032-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="65032-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="65032-142">-PublicKey</span></span>
<span data-ttu-id="65032-143">A biztonságos rendszerhéj (SSH) nyilvánoskulcs-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="65032-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="65032-144">Az objektum létrehozásához az Add-AzVMSshPublicKey parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="65032-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="65032-145">-Secret</span><span class="sxs-lookup"><span data-stu-id="65032-145">-Secret</span></span>
<span data-ttu-id="65032-146">Megadja a titok objektumot, amely a virtuális gépen elhelyezni kívánt tanúsítványra mutató hivatkozásokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="65032-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="65032-147">A Secrets objektumot a Add-AzVmssSecret parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="65032-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="65032-148">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="65032-148">-TimeZone</span></span>
<span data-ttu-id="65032-149">A virtuális gép időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="65032-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="65032-150">például \" Pacific standard Time \" .</span><span class="sxs-lookup"><span data-stu-id="65032-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="65032-151">A lehetséges értékek a [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)által eredményül adott időzónákban is [TimeZoneInfo.id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) .</span><span class="sxs-lookup"><span data-stu-id="65032-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="65032-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="65032-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="65032-153">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="65032-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="65032-154">Az objektum létrehozásához az New-AzVmssConfig parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="65032-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="65032-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="65032-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="65032-156">Azt jelzi, hogy a VMSS lévő virtuális gépek engedélyezve vannak-e az automatikus frissítésekhez.</span><span class="sxs-lookup"><span data-stu-id="65032-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="65032-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="65032-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="65032-158">Azt jelzi, hogy a virtuális gép ügynököt kell-e kiépíteni a VMSS lévő virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="65032-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="65032-159">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="65032-159">-Confirm</span></span>
<span data-ttu-id="65032-160">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="65032-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65032-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65032-161">-WhatIf</span></span>
<span data-ttu-id="65032-162">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="65032-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65032-163">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="65032-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65032-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65032-164">CommonParameters</span></span>
<span data-ttu-id="65032-165">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65032-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65032-166">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="65032-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65032-167">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65032-167">INPUTS</span></span>

### <span data-ttu-id="65032-168">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="65032-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="65032-169">System. String</span><span class="sxs-lookup"><span data-stu-id="65032-169">System.String</span></span>

### <span data-ttu-id="65032-170">System. null ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = semleges, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="65032-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="65032-171">Microsoft. Azure. Management. számítás. models. AdditionalUnattendContent []</span><span class="sxs-lookup"><span data-stu-id="65032-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="65032-172">Microsoft. Azure. Management. számítás. models. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="65032-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="65032-173">Microsoft. Azure. Management. számítás. models. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="65032-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="65032-174">Microsoft. Azure. Management. számítás. models. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="65032-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="65032-175">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65032-175">OUTPUTS</span></span>

### <span data-ttu-id="65032-176">Microsoft. Azure. commands. számítási. Automation. models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="65032-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="65032-177">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65032-177">NOTES</span></span>

## <span data-ttu-id="65032-178">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65032-178">RELATED LINKS</span></span>

[<span data-ttu-id="65032-179">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="65032-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="65032-180">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="65032-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="65032-181">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="65032-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="65032-182">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="65032-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="65032-183">Új – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="65032-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


