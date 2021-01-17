---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364179"
---
# <span data-ttu-id="a70e9-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="a70e9-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="a70e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a70e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a70e9-103">Letiltja a titkosítást az IaaS virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="a70e9-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="a70e9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a70e9-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a70e9-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a70e9-105">DESCRIPTION</span></span>
<span data-ttu-id="a70e9-106">A **Disable-AzVMDiskEncryption** parancsmag letiltja a titkosítást az infrastruktúra szolgáltatásként (IaaS) virtuális gépén.</span><span class="sxs-lookup"><span data-stu-id="a70e9-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="a70e9-107">Ez a parancsmag csak Windows-virtuális gépeken támogatott, Linux virtuális gépeken nem.</span><span class="sxs-lookup"><span data-stu-id="a70e9-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="a70e9-108">Ez a parancsmag egy bővítményt telepít a virtuális gépre a titkosítás letiltásához.</span><span class="sxs-lookup"><span data-stu-id="a70e9-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="a70e9-109">Ha a *Name paraméter* nincs megadva, létrejön egy "AzureDiskEncryption for Windows VMs" nevű bővítmény.</span><span class="sxs-lookup"><span data-stu-id="a70e9-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="a70e9-110">Figyelem: Ez a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="a70e9-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="a70e9-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a70e9-111">EXAMPLES</span></span>

### <span data-ttu-id="a70e9-112">1. példa: A windowsos virtuális gép összes kötetének titkosításának letiltása</span><span class="sxs-lookup"><span data-stu-id="a70e9-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="a70e9-113">Ez a parancs letiltja a titkosítást az összes típusú, VM002 nevű virtuális gépre, amely a Group0001 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="a70e9-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="a70e9-114">Mivel a *VolumeType* paraméter nincs megadva, a parancsmag az Összes értékre állítja az értéket.</span><span class="sxs-lookup"><span data-stu-id="a70e9-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="a70e9-115">2. példa: Adatkötetek titkosításának letiltása Windows virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="a70e9-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="a70e9-116">Ez a parancs letiltja a titkosítást a VM004 nevű virtuális gép típusadatokat mennyisége számára, amely a Group002 nevű erőforráscsoporthoz tartozik.</span><span class="sxs-lookup"><span data-stu-id="a70e9-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="a70e9-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a70e9-117">PARAMETERS</span></span>

### <span data-ttu-id="a70e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a70e9-118">-DefaultProfile</span></span>
<span data-ttu-id="a70e9-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a70e9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a70e9-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a70e9-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a70e9-121">Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziója automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="a70e9-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="a70e9-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="a70e9-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="a70e9-123">A bővítmény közzétevőjának neve.</span><span class="sxs-lookup"><span data-stu-id="a70e9-123">The extension publisher name.</span></span> <span data-ttu-id="a70e9-124">Ezt a paramétert csak a "Microsoft.Azure.Security" alapértelmezett értékének felülbírálása érdekében adja meg.</span><span class="sxs-lookup"><span data-stu-id="a70e9-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="a70e9-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="a70e9-125">-ExtensionType</span></span>
<span data-ttu-id="a70e9-126">A bővítmény típusa.</span><span class="sxs-lookup"><span data-stu-id="a70e9-126">The extension type.</span></span> <span data-ttu-id="a70e9-127">Ezt a paramétert megadva felülbírálhatja a Windows-VMs -hez használt "AzureDiskEncryption" és a Linux-alapú "AzureDiskEncryptionForLinux" alapértelmezett értékét.</span><span class="sxs-lookup"><span data-stu-id="a70e9-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="a70e9-128">-Force</span><span class="sxs-lookup"><span data-stu-id="a70e9-128">-Force</span></span>
<span data-ttu-id="a70e9-129">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="a70e9-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a70e9-130">-Name</span><span class="sxs-lookup"><span data-stu-id="a70e9-130">-Name</span></span>
<span data-ttu-id="a70e9-131">A bővítményt képviselő Azure Resource Manager (ARM) nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a70e9-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="a70e9-132">Ha nincs megadva ez a paraméter, ez a parancsmag alapértelmezés szerint "AzureDiskEncryption windowsos VMs esetén" lesz.</span><span class="sxs-lookup"><span data-stu-id="a70e9-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70e9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a70e9-133">-ResourceGroupName</span></span>
<span data-ttu-id="a70e9-134">A virtuális gép erőforráscsoportnevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a70e9-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="a70e9-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a70e9-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="a70e9-136">A titkosítási bővítmény verzióját határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a70e9-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="a70e9-137">Ha nem ad meg értéket ehhez a paraméterhez, a bővítmény legújabb verzióját használja a program.</span><span class="sxs-lookup"><span data-stu-id="a70e9-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70e9-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="a70e9-138">-VMName</span></span>
<span data-ttu-id="a70e9-139">Annak a virtuális gépnek a nevét adja meg, amelyn ez a parancsmag letiltja a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="a70e9-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70e9-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="a70e9-140">-VolumeType</span></span>
<span data-ttu-id="a70e9-141">A titkosítási művelet végrehajtásához szükséges virtuális gépkötet típusát határozza meg.</span><span class="sxs-lookup"><span data-stu-id="a70e9-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="a70e9-142">Windows-virtuális gépek esetén érvényes értékek:</span><span class="sxs-lookup"><span data-stu-id="a70e9-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="a70e9-143">Mind</span><span class="sxs-lookup"><span data-stu-id="a70e9-143">All</span></span>
- <span data-ttu-id="a70e9-144">Operációs rendszer</span><span class="sxs-lookup"><span data-stu-id="a70e9-144">OS</span></span>
- <span data-ttu-id="a70e9-145">Adatok.</span><span class="sxs-lookup"><span data-stu-id="a70e9-145">Data.</span></span>
<span data-ttu-id="a70e9-146">Ha nem ad meg értéket ehhez a paraméterhez, az alapértelmezett érték a Mind érték.</span><span class="sxs-lookup"><span data-stu-id="a70e9-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="a70e9-147">Linux esetén jelenleg nem támogatott a titkosítás letiltása.</span><span class="sxs-lookup"><span data-stu-id="a70e9-147">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a70e9-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a70e9-148">-Confirm</span></span>
<span data-ttu-id="a70e9-149">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="a70e9-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70e9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a70e9-150">-WhatIf</span></span>
<span data-ttu-id="a70e9-151">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="a70e9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a70e9-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a70e9-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a70e9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a70e9-153">CommonParameters</span></span>
<span data-ttu-id="a70e9-154">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a70e9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a70e9-155">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a70e9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a70e9-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a70e9-156">INPUTS</span></span>

### <span data-ttu-id="a70e9-157">System.String</span><span class="sxs-lookup"><span data-stu-id="a70e9-157">System.String</span></span>

### <span data-ttu-id="a70e9-158">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a70e9-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a70e9-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a70e9-159">OUTPUTS</span></span>

### <span data-ttu-id="a70e9-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a70e9-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a70e9-161">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a70e9-161">NOTES</span></span>

## <span data-ttu-id="a70e9-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a70e9-162">RELATED LINKS</span></span>

[<span data-ttu-id="a70e9-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="a70e9-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="a70e9-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="a70e9-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="a70e9-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="a70e9-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


