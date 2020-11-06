---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssDiskEncryptionExtension.md
ms.openlocfilehash: aeac00806ef77d756dc8060b06f7baa995568fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503016"
---
# <span data-ttu-id="fcfb9-101">Set-AzureRmVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="fcfb9-101">Set-AzureRmVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="fcfb9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fcfb9-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfb9-103">Lehetővé teszi a lemezek titkosítását a VM-léptékű készleteken.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-103">Enables disk encryption on a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcfb9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fcfb9-104">SYNTAX</span></span>

```
Set-AzureRmVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcfb9-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fcfb9-105">DESCRIPTION</span></span>
<span data-ttu-id="fcfb9-106">A **set-AzureRmVmssDiskEncryptionExtension** parancsmag engedélyezi a titkosítást egy VM-léptékű készleten.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-106">The **Set-AzureRmVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="fcfb9-107">Ez a parancsmag lehetővé teszi a titkosítást, ha telepíti a titkosítási bővítményt a VM-méretarány beállítással.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="fcfb9-108">Ha nincs megadva *név* paraméter, akkor a program a Windows operációs rendszert futtató virtuális gépekhez használt alapértelmezett név AzureDiskEncryption, illetve a AzureDiskEncryptionForLinux virtuális gépekhez telepített virtuális gépekhez bővítményt tartalmaz.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="fcfb9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="fcfb9-109">EXAMPLES</span></span>

### <span data-ttu-id="fcfb9-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fcfb9-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzureRmKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzureRmVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="fcfb9-111">Ez a parancs engedélyezi az összes VMs-meghajtó titkosítását a VM méretarányos készletében.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="fcfb9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fcfb9-112">PARAMETERS</span></span>

### <span data-ttu-id="fcfb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcfb9-113">-DefaultProfile</span></span>
<span data-ttu-id="fcfb9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcfb9-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fcfb9-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="fcfb9-116">Az alverzió automatikus frissítésének letiltása</span><span class="sxs-lookup"><span data-stu-id="fcfb9-116">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="fcfb9-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="fcfb9-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="fcfb9-118">A ResourceID, amelybe a generált titkosítási kulcs kerül</span><span class="sxs-lookup"><span data-stu-id="fcfb9-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="fcfb9-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="fcfb9-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="fcfb9-120">A kulcsfájl URL-címe, amelybe a generált titkosítási kulcs kerül</span><span class="sxs-lookup"><span data-stu-id="fcfb9-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="fcfb9-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="fcfb9-121">-ExtensionName</span></span>
<span data-ttu-id="fcfb9-122">A kiterjesztés neve.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-122">The extension name.</span></span>
<span data-ttu-id="fcfb9-123">Ha ez a paraméter nincs megadva, az alapértelmezett értékek a Windows VMs-AzureDiskEncryption és a AzureDiskEncryptionForLinux for Linux VMs esetén használhatók.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="fcfb9-124">-Force</span><span class="sxs-lookup"><span data-stu-id="fcfb9-124">-Force</span></span>
<span data-ttu-id="fcfb9-125">A titkosítás engedélyezésének kényszerítése a virtuálisgép-méretarány beállításakor.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-125">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="fcfb9-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="fcfb9-126">-ForceUpdate</span></span>
<span data-ttu-id="fcfb9-127">Címke létrehozása a haderő frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-127">Generate a tag for force update.</span></span>  <span data-ttu-id="fcfb9-128">Ezt meg kell adni az ismétlődő titkosítási műveletek elvégzésének ugyanazon a VM-eszközön.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="fcfb9-129">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="fcfb9-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="fcfb9-130">A hangerő-titkosítási kulcs titkosítására használt kulcskezelő algoritmus</span><span class="sxs-lookup"><span data-stu-id="fcfb9-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="fcfb9-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="fcfb9-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="fcfb9-132">A KeyEncryptionKey titkosítási kulcs titkosítására használt verziójának verziószámmal bejelentkező URL-címe</span><span class="sxs-lookup"><span data-stu-id="fcfb9-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="fcfb9-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="fcfb9-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="fcfb9-134">A titkosító kulcs titkosításához használt KeyEncryptionKey tartalmazó ResourceID</span><span class="sxs-lookup"><span data-stu-id="fcfb9-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="fcfb9-135">-Jelmondat</span><span class="sxs-lookup"><span data-stu-id="fcfb9-135">-Passphrase</span></span>
<span data-ttu-id="fcfb9-136">A paraméterekben megadott jelmondat.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="fcfb9-137">Ez a paraméter csak Linux VM esetén működik.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-137">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="fcfb9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcfb9-138">-ResourceGroupName</span></span>
<span data-ttu-id="fcfb9-139">Az erőforráscsoport neve, amelyhez a VM Méretarányi készlete tartozik</span><span class="sxs-lookup"><span data-stu-id="fcfb9-139">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="fcfb9-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fcfb9-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="fcfb9-141">A Type Handler verziója.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-141">The type handler version.</span></span>

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

### <span data-ttu-id="fcfb9-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fcfb9-142">-VMScaleSetName</span></span>
<span data-ttu-id="fcfb9-143">A virtuális gép méretarányának neve</span><span class="sxs-lookup"><span data-stu-id="fcfb9-143">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="fcfb9-144">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="fcfb9-144">-VolumeType</span></span>
<span data-ttu-id="fcfb9-145">A titkosítási művelet elvégzéséhez használt hangerő (operációs rendszer vagy adat) típusa</span><span class="sxs-lookup"><span data-stu-id="fcfb9-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="fcfb9-146">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fcfb9-146">-Confirm</span></span>
<span data-ttu-id="fcfb9-147">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcfb9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcfb9-148">-WhatIf</span></span>
<span data-ttu-id="fcfb9-149">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcfb9-150">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fcfb9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcfb9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfb9-151">CommonParameters</span></span>
<span data-ttu-id="fcfb9-152">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fcfb9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfb9-153">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcfb9-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfb9-154">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcfb9-154">INPUTS</span></span>

### <span data-ttu-id="fcfb9-155">System. String</span><span class="sxs-lookup"><span data-stu-id="fcfb9-155">System.String</span></span>

### <span data-ttu-id="fcfb9-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fcfb9-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fcfb9-157">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fcfb9-157">OUTPUTS</span></span>

### <span data-ttu-id="fcfb9-158">Microsoft. Azure. commands. kiszámítás. models. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="fcfb9-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="fcfb9-159">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fcfb9-159">NOTES</span></span>

## <span data-ttu-id="fcfb9-160">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fcfb9-160">RELATED LINKS</span></span>