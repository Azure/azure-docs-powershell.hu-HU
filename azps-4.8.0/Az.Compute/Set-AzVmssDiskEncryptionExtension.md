---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181164"
---
# <span data-ttu-id="cda99-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="cda99-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="cda99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cda99-102">SYNOPSIS</span></span>
<span data-ttu-id="cda99-103">Lehetővé teszi a lemezek titkosítását a VM-léptékű készleteken.</span><span class="sxs-lookup"><span data-stu-id="cda99-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="cda99-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cda99-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cda99-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cda99-105">DESCRIPTION</span></span>
<span data-ttu-id="cda99-106">A **set-AzVmssDiskEncryptionExtension** parancsmag engedélyezi a titkosítást egy VM-léptékű készleten.</span><span class="sxs-lookup"><span data-stu-id="cda99-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="cda99-107">Ez a parancsmag lehetővé teszi a titkosítást, ha telepíti a titkosítási bővítményt a VM-méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="cda99-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="cda99-108">A Linux virtuális gépek esetében a *VolumeType* paraméternek jelen kell lennie, és "Data" értékre kell állítania.</span><span class="sxs-lookup"><span data-stu-id="cda99-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="cda99-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cda99-109">EXAMPLES</span></span>

### <span data-ttu-id="cda99-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cda99-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="cda99-111">Ez a parancs engedélyezi a Windows VMs minden lemezén a VM méretarányos készletben való titkosítást.</span><span class="sxs-lookup"><span data-stu-id="cda99-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="cda99-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="cda99-112">Example 2</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "Data"

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
 -VolumeType $volumeType
```

<span data-ttu-id="cda99-113">Ez a parancs engedélyezi az összes Linux VM adatlemezén a VM-méretarányos készletben való titkosítást.</span><span class="sxs-lookup"><span data-stu-id="cda99-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="cda99-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cda99-114">PARAMETERS</span></span>

### <span data-ttu-id="cda99-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda99-115">-DefaultProfile</span></span>
<span data-ttu-id="cda99-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cda99-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cda99-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="cda99-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="cda99-118">Az alverzió automatikus frissítésének letiltása</span><span class="sxs-lookup"><span data-stu-id="cda99-118">Disable auto-upgrade of minor version</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda99-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="cda99-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="cda99-120">A ResourceID, amelybe a generált titkosítási kulcs kerül</span><span class="sxs-lookup"><span data-stu-id="cda99-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda99-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="cda99-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="cda99-122">A kulcsfájl URL-címe, amelybe a generált titkosítási kulcs kerül</span><span class="sxs-lookup"><span data-stu-id="cda99-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="cda99-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="cda99-123">-ExtensionName</span></span>
<span data-ttu-id="cda99-124">A kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="cda99-124">The extension name.</span></span>
<span data-ttu-id="cda99-125">Ha ez a paraméter nincs megadva, az alapértelmezett értékek a Windows VMs-AzureDiskEncryption és a AzureDiskEncryptionForLinux for Linux VMs esetén használhatók.</span><span class="sxs-lookup"><span data-stu-id="cda99-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="cda99-126">-Force</span><span class="sxs-lookup"><span data-stu-id="cda99-126">-Force</span></span>
<span data-ttu-id="cda99-127">A titkosítás engedélyezésének kényszerítése a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="cda99-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="cda99-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="cda99-128">-ForceUpdate</span></span>
<span data-ttu-id="cda99-129">Címke létrehozása a haderő frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="cda99-129">Generate a tag for force update.</span></span>  <span data-ttu-id="cda99-130">Ezt meg kell adni az ismétlődő titkosítási műveletek elvégzésének ugyanazon a VM-eszközön.</span><span class="sxs-lookup"><span data-stu-id="cda99-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda99-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="cda99-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="cda99-132">A hangerő-titkosítási kulcs titkosítására használt kulcskezelő algoritmus</span><span class="sxs-lookup"><span data-stu-id="cda99-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda99-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="cda99-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="cda99-134">A KeyEncryptionKey titkosítási kulcs titkosítására használt verziójának verziószámmal bejelentkező URL-címe</span><span class="sxs-lookup"><span data-stu-id="cda99-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="cda99-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="cda99-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="cda99-136">A titkosító kulcs titkosításához használt KeyEncryptionKey tartalmazó ResourceID</span><span class="sxs-lookup"><span data-stu-id="cda99-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="cda99-137">-Jelmondat</span><span class="sxs-lookup"><span data-stu-id="cda99-137">-Passphrase</span></span>
<span data-ttu-id="cda99-138">A paraméterekben megadott jelmondat.</span><span class="sxs-lookup"><span data-stu-id="cda99-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="cda99-139">Ez a paraméter csak Linux VM esetén működik.</span><span class="sxs-lookup"><span data-stu-id="cda99-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="cda99-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda99-140">-ResourceGroupName</span></span>
<span data-ttu-id="cda99-141">Az erőforráscsoport neve, amelyhez a VM Méretarányi készlete tartozik</span><span class="sxs-lookup"><span data-stu-id="cda99-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="cda99-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="cda99-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="cda99-143">A Type Handler verziója.</span><span class="sxs-lookup"><span data-stu-id="cda99-143">The type handler version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda99-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cda99-144">-VMScaleSetName</span></span>
<span data-ttu-id="cda99-145">A virtuális gép méretarányának neve</span><span class="sxs-lookup"><span data-stu-id="cda99-145">Name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda99-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="cda99-146">-VolumeType</span></span>
<span data-ttu-id="cda99-147">Annak a virtuálisgép-köteteknek a típusát adja meg, amelyeken titkosítási műveletet kell végrehajtani: operációs rendszer, adat vagy mind.</span><span class="sxs-lookup"><span data-stu-id="cda99-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="cda99-148">Linux: a **VolumeType** paraméternek jelen kell lennie, és az adatértéknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="cda99-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="cda99-149">Windows: a **VolumeType** paramétert (ha van) az All vagy az os értékre kell állítani.</span><span class="sxs-lookup"><span data-stu-id="cda99-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="cda99-150">Ha a **VolumeType** paraméter nincs kihagyva az "összes" értékkel.</span><span class="sxs-lookup"><span data-stu-id="cda99-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cda99-151">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cda99-151">-Confirm</span></span>
<span data-ttu-id="cda99-152">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cda99-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cda99-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cda99-153">-WhatIf</span></span>
<span data-ttu-id="cda99-154">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cda99-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cda99-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cda99-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cda99-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda99-156">CommonParameters</span></span>
<span data-ttu-id="cda99-157">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cda99-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda99-158">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cda99-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda99-159">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cda99-159">INPUTS</span></span>

### <span data-ttu-id="cda99-160">System. String</span><span class="sxs-lookup"><span data-stu-id="cda99-160">System.String</span></span>

### <span data-ttu-id="cda99-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cda99-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cda99-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cda99-162">OUTPUTS</span></span>

### <span data-ttu-id="cda99-163">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="cda99-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="cda99-164">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cda99-164">NOTES</span></span>

## <span data-ttu-id="cda99-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cda99-165">RELATED LINKS</span></span>
