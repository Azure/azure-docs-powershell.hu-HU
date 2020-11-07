---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
ms.openlocfilehash: ee9649d7a2a88dd3a91f428201ddc66d1a6562da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680177"
---
# <span data-ttu-id="e4299-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="e4299-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="e4299-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e4299-102">SYNOPSIS</span></span>
<span data-ttu-id="e4299-103">Beállítja a VMSS operációs rendszer profiljának tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="e4299-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4299-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e4299-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4299-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e4299-105">DESCRIPTION</span></span>
<span data-ttu-id="e4299-106">A **set-AzureRmVmssOsProfile** parancsmag a virtuális gép méretarányának beállítása operációs rendszer profiljának tulajdonságait adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4299-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="e4299-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e4299-107">EXAMPLES</span></span>

### <span data-ttu-id="e4299-108">Példa 1: az operációs rendszer profiljának tulajdonságainak beállítása VMSS</span><span class="sxs-lookup"><span data-stu-id="e4299-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="e4299-109">Ez a parancs beállítja az operációs rendszer profiljának tulajdonságait a ContosoVMSS nevű VMSS tartozó virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="e4299-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="e4299-110">A parancs a VMSS a virtuálisgép-példányok számítógép nevének előtagját állítja be a rendszergazda felhasználónevének és jelszavának teszteléséhez és ellátásához.</span><span class="sxs-lookup"><span data-stu-id="e4299-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="e4299-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e4299-111">PARAMETERS</span></span>

### <span data-ttu-id="e4299-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="e4299-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="e4299-113">Egy felügyelet nélküli tartalom-objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="e4299-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="e4299-114">Az objektum létrehozásához használhatja a Add-AzureRmVMAdditionalUnattendContent.</span><span class="sxs-lookup"><span data-stu-id="e4299-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="e4299-115">-AdminPassword</span></span>
<span data-ttu-id="e4299-116">A VMSS lévő összes virtuálisgép-példányhoz használt rendszergazdai jelszót adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4299-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="e4299-117">-AdminUsername</span></span>
<span data-ttu-id="e4299-118">Annak a rendszergazdai fióknak a nevét adja meg, amelyet a VMSS minden virtuális gép példányához használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="e4299-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="e4299-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="e4299-120">A VMSS a virtuálisgép-példányok számítógép nevének előtagját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4299-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="e4299-121">A számítógépek nevének 1 – 15 karakter hosszúnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="e4299-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="e4299-122">-CustomData</span></span>
<span data-ttu-id="e4299-123">Az alap-64 kódolt karakterláncát adja meg az egyéni adatokhoz.</span><span class="sxs-lookup"><span data-stu-id="e4299-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="e4299-124">Ez a cikk a virtuális gépen fájlként mentett bináris tömböt dekódolja.</span><span class="sxs-lookup"><span data-stu-id="e4299-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="e4299-125">A bináris tömb maximális hossza 65535 bájt.</span><span class="sxs-lookup"><span data-stu-id="e4299-125">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-126">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="e4299-126">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="e4299-127">Azt jelzi, hogy ez a parancsmag letiltja a jelszó-hitelesítést.</span><span class="sxs-lookup"><span data-stu-id="e4299-127">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-128">-Listener</span><span class="sxs-lookup"><span data-stu-id="e4299-128">-Listener</span></span>
<span data-ttu-id="e4299-129">A Windows Remote Management (WinRM) figyelőit adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4299-129">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="e4299-130">Ez engedélyezi a távoli Windows PowerShellt.</span><span class="sxs-lookup"><span data-stu-id="e4299-130">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="e4299-131">A figyelő létrehozásához használhatja a Add-AzureRmVmssWinRMListener parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="e4299-131">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: WinRMListener[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-132">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="e4299-132">-PublicKey</span></span>
<span data-ttu-id="e4299-133">A biztonságos rendszerhéj (SSH) nyilvánoskulcs-objektumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4299-133">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="e4299-134">Az objektum létrehozásához az Add-AzureRmVMSshPublicKey parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="e4299-134">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: SshPublicKey[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-135">-Secret</span><span class="sxs-lookup"><span data-stu-id="e4299-135">-Secret</span></span>
<span data-ttu-id="e4299-136">Megadja a titok objektumot, amely a virtuális gépen elhelyezni kívánt tanúsítványra mutató hivatkozásokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="e4299-136">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="e4299-137">A Secrets objektumot a Add-AzureRmVmssSecret parancsmaggal hozhatja létre.</span><span class="sxs-lookup"><span data-stu-id="e4299-137">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: VaultSecretGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-138">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="e4299-138">-TimeZone</span></span>
<span data-ttu-id="e4299-139">A virtuális gép időzónáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4299-139">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-140">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e4299-140">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e4299-141">A VMSS objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="e4299-141">Specifies the VMSS object.</span></span>
<span data-ttu-id="e4299-142">Az objektum létrehozásához az New-AzureRmVmssConfig parancsmagot használhatja.</span><span class="sxs-lookup"><span data-stu-id="e4299-142">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-143">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="e4299-143">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="e4299-144">Azt jelzi, hogy a VMSS lévő virtuális gépek engedélyezve vannak-e az automatikus frissítésekhez.</span><span class="sxs-lookup"><span data-stu-id="e4299-144">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-145">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="e4299-145">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="e4299-146">Azt jelzi, hogy a virtuális gép ügynököt kell-e kiépíteni a VMSS lévő virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="e4299-146">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-147">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e4299-147">-Confirm</span></span>
<span data-ttu-id="e4299-148">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e4299-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4299-149">-WhatIf</span></span>
<span data-ttu-id="e4299-150">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e4299-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e4299-151">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e4299-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4299-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4299-152">CommonParameters</span></span>
<span data-ttu-id="e4299-153">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e4299-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4299-154">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4299-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4299-155">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4299-155">INPUTS</span></span>

### <span data-ttu-id="e4299-156">Nincs</span><span class="sxs-lookup"><span data-stu-id="e4299-156">None</span></span>
<span data-ttu-id="e4299-157">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e4299-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4299-158">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e4299-158">OUTPUTS</span></span>

### <span data-ttu-id="e4299-159">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="e4299-159">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e4299-160">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e4299-160">NOTES</span></span>

## <span data-ttu-id="e4299-161">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e4299-161">RELATED LINKS</span></span>

[<span data-ttu-id="e4299-162">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="e4299-162">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="e4299-163">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="e4299-163">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="e4299-164">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e4299-164">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="e4299-165">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="e4299-165">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="e4299-166">Új – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e4299-166">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


