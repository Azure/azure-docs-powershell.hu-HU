---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 15453163918854dd0efa7440209164007335aced
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844169"
---
# <span data-ttu-id="051db-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="051db-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="051db-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="051db-102">SYNOPSIS</span></span>
<span data-ttu-id="051db-103">Lehetővé teszi a lemezek titkosítását a VM-léptékű készleteken.</span><span class="sxs-lookup"><span data-stu-id="051db-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="051db-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="051db-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="051db-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="051db-105">DESCRIPTION</span></span>
<span data-ttu-id="051db-106">A **set-AzVmssDiskEncryptionExtension** parancsmag engedélyezi a titkosítást egy VM-léptékű készleten.</span><span class="sxs-lookup"><span data-stu-id="051db-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="051db-107">Ez a parancsmag lehetővé teszi a titkosítást, ha telepíti a titkosítási bővítményt a VM-méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="051db-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="051db-108">Ha nincs megadva *név* paraméter, akkor a program a Windows operációs rendszert futtató virtuális gépekhez használt alapértelmezett név AzureDiskEncryption, illetve a AzureDiskEncryptionForLinux virtuális gépekhez telepített virtuális gépekhez bővítményt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="051db-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="051db-109">Példák</span><span class="sxs-lookup"><span data-stu-id="051db-109">EXAMPLES</span></span>

### <span data-ttu-id="051db-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="051db-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="051db-111">Ez a parancs engedélyezi az összes VMs-meghajtó titkosítását a VM méretarányos készletében.</span><span class="sxs-lookup"><span data-stu-id="051db-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="051db-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="051db-112">PARAMETERS</span></span>

### <span data-ttu-id="051db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="051db-113">-DefaultProfile</span></span>
<span data-ttu-id="051db-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="051db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="051db-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="051db-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="051db-116">Az alverzió automatikus frissítésének letiltása</span><span class="sxs-lookup"><span data-stu-id="051db-116">Disable auto-upgrade of minor version</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="051db-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="051db-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="051db-118">A ResourceID, amelybe a generált titkosítási kulcs kerül</span><span class="sxs-lookup"><span data-stu-id="051db-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="051db-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="051db-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="051db-120">A kulcsfájl URL-címe, amelybe a generált titkosítási kulcs kerül</span><span class="sxs-lookup"><span data-stu-id="051db-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="051db-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="051db-121">-ExtensionName</span></span>
<span data-ttu-id="051db-122">A kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="051db-122">The extension name.</span></span>
<span data-ttu-id="051db-123">Ha ez a paraméter nincs megadva, az alapértelmezett értékek a Windows VMs-AzureDiskEncryption és a AzureDiskEncryptionForLinux for Linux VMs esetén használhatók.</span><span class="sxs-lookup"><span data-stu-id="051db-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="051db-124">-Force</span><span class="sxs-lookup"><span data-stu-id="051db-124">-Force</span></span>
<span data-ttu-id="051db-125">A titkosítás engedélyezésének kényszerítése a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="051db-125">To force enabling encryption on the virtual machine scale set.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="051db-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="051db-126">-ForceUpdate</span></span>
<span data-ttu-id="051db-127">Címke létrehozása a haderő frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="051db-127">Generate a tag for force update.</span></span>  <span data-ttu-id="051db-128">Ezt meg kell adni az ismétlődő titkosítási műveletek elvégzésének ugyanazon a VM-eszközön.</span><span class="sxs-lookup"><span data-stu-id="051db-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="051db-129">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="051db-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="051db-130">A hangerő-titkosítási kulcs titkosítására használt kulcskezelő algoritmus</span><span class="sxs-lookup"><span data-stu-id="051db-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="051db-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="051db-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="051db-132">A KeyEncryptionKey titkosítási kulcs titkosítására használt verziójának verziószámmal bejelentkező URL-címe</span><span class="sxs-lookup"><span data-stu-id="051db-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="051db-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="051db-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="051db-134">A titkosító kulcs titkosításához használt KeyEncryptionKey tartalmazó ResourceID</span><span class="sxs-lookup"><span data-stu-id="051db-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="051db-135">-Jelmondat</span><span class="sxs-lookup"><span data-stu-id="051db-135">-Passphrase</span></span>
<span data-ttu-id="051db-136">A paraméterekben megadott jelmondat.</span><span class="sxs-lookup"><span data-stu-id="051db-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="051db-137">Ez a paraméter csak Linux VM esetén működik.</span><span class="sxs-lookup"><span data-stu-id="051db-137">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="051db-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="051db-138">-ResourceGroupName</span></span>
<span data-ttu-id="051db-139">Az erőforráscsoport neve, amelyhez a VM Méretarányi készlete tartozik</span><span class="sxs-lookup"><span data-stu-id="051db-139">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="051db-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="051db-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="051db-141">A Type Handler verziója.</span><span class="sxs-lookup"><span data-stu-id="051db-141">The type handler version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="051db-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="051db-142">-VMScaleSetName</span></span>
<span data-ttu-id="051db-143">A virtuális gép méretarányának neve</span><span class="sxs-lookup"><span data-stu-id="051db-143">Name of the virtual machine scale set</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="051db-144">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="051db-144">-VolumeType</span></span>
<span data-ttu-id="051db-145">A titkosítási művelet elvégzéséhez használt hangerő (operációs rendszer vagy adat) típusa</span><span class="sxs-lookup"><span data-stu-id="051db-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="051db-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="051db-146">-Confirm</span></span>
<span data-ttu-id="051db-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="051db-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="051db-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="051db-148">-WhatIf</span></span>
<span data-ttu-id="051db-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="051db-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="051db-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="051db-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="051db-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="051db-151">CommonParameters</span></span>
<span data-ttu-id="051db-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="051db-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="051db-153">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="051db-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="051db-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="051db-154">INPUTS</span></span>

### <span data-ttu-id="051db-155">System. String</span><span class="sxs-lookup"><span data-stu-id="051db-155">System.String</span></span>
<span data-ttu-id="051db-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="051db-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="051db-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="051db-157">OUTPUTS</span></span>

### <span data-ttu-id="051db-158">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="051db-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="051db-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="051db-159">NOTES</span></span>

## <span data-ttu-id="051db-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="051db-160">RELATED LINKS</span></span>

