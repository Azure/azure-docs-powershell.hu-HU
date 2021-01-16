---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358621"
---
# <span data-ttu-id="ffa93-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="ffa93-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="ffa93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffa93-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa93-103">Lehetővé teszi a lemeztitkosítást egy VM-méretkészleten.</span><span class="sxs-lookup"><span data-stu-id="ffa93-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="ffa93-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ffa93-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ffa93-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ffa93-105">DESCRIPTION</span></span>
<span data-ttu-id="ffa93-106">A **Set-AzVmssDiskEncryptionExtension parancsmag** lehetővé teszi a titkosítást egy VM-méretkészleten.</span><span class="sxs-lookup"><span data-stu-id="ffa93-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="ffa93-107">Ez a parancsmag lehetővé teszi a titkosítást úgy, hogy telepíti a lemeztitkosítási bővítményt a VM méretkészletére.</span><span class="sxs-lookup"><span data-stu-id="ffa93-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="ffa93-108">Linuxos virtuális gépek esetén a *VolumeType* paraméternek jelen kell lennie, és az "Adatok" értéknek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="ffa93-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="ffa93-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ffa93-109">EXAMPLES</span></span>

### <span data-ttu-id="ffa93-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="ffa93-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="ffa93-111">Ez a parancs lehetővé teszi a titkosítást az összes Windows-virtuális gép összes lemezén egy VM-méretkészletben.</span><span class="sxs-lookup"><span data-stu-id="ffa93-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="ffa93-112">2. példa</span><span class="sxs-lookup"><span data-stu-id="ffa93-112">Example 2</span></span>
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

<span data-ttu-id="ffa93-113">Ez a parancs lehetővé teszi a titkosítást az összes Linux-virtuális gép adatlemezén egy VM-méretkészletben.</span><span class="sxs-lookup"><span data-stu-id="ffa93-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="ffa93-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffa93-114">PARAMETERS</span></span>

### <span data-ttu-id="ffa93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa93-115">-DefaultProfile</span></span>
<span data-ttu-id="ffa93-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ffa93-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffa93-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="ffa93-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="ffa93-118">Az alverzió automatikus frissítésének letiltása</span><span class="sxs-lookup"><span data-stu-id="ffa93-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="ffa93-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ffa93-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="ffa93-120">ResourceID of the KeyVault where generated encryption key will be placed to</span><span class="sxs-lookup"><span data-stu-id="ffa93-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="ffa93-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="ffa93-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="ffa93-122">Annak a KeyVaultnak az URL-címe, ahová a létrehozott titkosítási kulcs kerül</span><span class="sxs-lookup"><span data-stu-id="ffa93-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="ffa93-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="ffa93-123">-ExtensionName</span></span>
<span data-ttu-id="ffa93-124">A bővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="ffa93-124">The extension name.</span></span>
<span data-ttu-id="ffa93-125">Ha nincs megadva ez a paraméter, az alapértelmezett értékek a Windows VMs azureDiskEncryption és a Linux-alapú AzureDiskEncryptionForLinux esetén</span><span class="sxs-lookup"><span data-stu-id="ffa93-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="ffa93-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ffa93-126">-Force</span></span>
<span data-ttu-id="ffa93-127">A titkosítás kényszerítenie kell a virtuális gép méretaránykészletének engedélyezését.</span><span class="sxs-lookup"><span data-stu-id="ffa93-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ffa93-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="ffa93-128">-ForceUpdate</span></span>
<span data-ttu-id="ffa93-129">Címke létrehozása kényszerítő frissítéshez.</span><span class="sxs-lookup"><span data-stu-id="ffa93-129">Generate a tag for force update.</span></span>  <span data-ttu-id="ffa93-130">Ezt meg kell adni, hogy ismétlődő titkosítási műveleteket hajtson végre ugyanazon a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="ffa93-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="ffa93-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ffa93-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="ffa93-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span><span class="sxs-lookup"><span data-stu-id="ffa93-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="ffa93-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="ffa93-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="ffa93-134">A billentyűzettitkosítási kulcs titkosításához használt KeyEncryptionKey verziójú KeyVault URL-címe</span><span class="sxs-lookup"><span data-stu-id="ffa93-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="ffa93-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ffa93-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="ffa93-136">A lemeztitkosítási kulcs titkosításához használt KeyVault-kulcs Erőforrásazonosítója</span><span class="sxs-lookup"><span data-stu-id="ffa93-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="ffa93-137">-Passphrase</span><span class="sxs-lookup"><span data-stu-id="ffa93-137">-Passphrase</span></span>
<span data-ttu-id="ffa93-138">A paraméterekben megadott jelszó.</span><span class="sxs-lookup"><span data-stu-id="ffa93-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="ffa93-139">Ez a paraméter csak Linux VM esetén működik.</span><span class="sxs-lookup"><span data-stu-id="ffa93-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="ffa93-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffa93-140">-ResourceGroupName</span></span>
<span data-ttu-id="ffa93-141">Az erőforráscsoport neve, amelyhez a VM-méretkészlet tartozik</span><span class="sxs-lookup"><span data-stu-id="ffa93-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="ffa93-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="ffa93-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="ffa93-143">A típuskezelő verziója.</span><span class="sxs-lookup"><span data-stu-id="ffa93-143">The type handler version.</span></span>

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

### <span data-ttu-id="ffa93-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ffa93-144">-VMScaleSetName</span></span>
<span data-ttu-id="ffa93-145">A virtuális gép méretaránykészletének neve</span><span class="sxs-lookup"><span data-stu-id="ffa93-145">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="ffa93-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="ffa93-146">-VolumeType</span></span>
<span data-ttu-id="ffa93-147">Megadja, hogy milyen típusú virtuális gépköteten végezze el a titkosítási műveletet: OPERÁCIÓS rendszer, Adatok vagy Mind.</span><span class="sxs-lookup"><span data-stu-id="ffa93-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="ffa93-148">Linux: A **VolumeType paraméternek** jelen kell lennie, és adatokra kell állítania.</span><span class="sxs-lookup"><span data-stu-id="ffa93-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="ffa93-149">Windows: A **VolumeType paramétert** (ha van ilyen) vagy Az összes, vagy az operációs rendszer paramétert kell beállítani.</span><span class="sxs-lookup"><span data-stu-id="ffa93-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="ffa93-150">Ha a **VolumeType paramétert** nem ad meg, az alapértelmezés szerint az "Összes" értéket használja.</span><span class="sxs-lookup"><span data-stu-id="ffa93-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


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

### <span data-ttu-id="ffa93-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffa93-151">-Confirm</span></span>
<span data-ttu-id="ffa93-152">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ffa93-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa93-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa93-153">-WhatIf</span></span>
<span data-ttu-id="ffa93-154">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ffa93-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa93-155">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ffa93-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa93-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa93-156">CommonParameters</span></span>
<span data-ttu-id="ffa93-157">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa93-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa93-158">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ffa93-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa93-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffa93-159">INPUTS</span></span>

### <span data-ttu-id="ffa93-160">System.String</span><span class="sxs-lookup"><span data-stu-id="ffa93-160">System.String</span></span>

### <span data-ttu-id="ffa93-161">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ffa93-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ffa93-162">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ffa93-162">OUTPUTS</span></span>

### <span data-ttu-id="ffa93-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="ffa93-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="ffa93-164">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ffa93-164">NOTES</span></span>

## <span data-ttu-id="ffa93-165">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ffa93-165">RELATED LINKS</span></span>
