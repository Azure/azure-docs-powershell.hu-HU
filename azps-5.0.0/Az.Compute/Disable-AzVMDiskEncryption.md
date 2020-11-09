---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 1aad073ebd1f1a5e14abfd728ba6e6266a2d6fb8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301556"
---
# <span data-ttu-id="59daf-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="59daf-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="59daf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="59daf-102">SYNOPSIS</span></span>
<span data-ttu-id="59daf-103">Letiltja a titkosítást egy IaaS virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="59daf-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="59daf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="59daf-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59daf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="59daf-105">DESCRIPTION</span></span>
<span data-ttu-id="59daf-106">A **disable-AzVMDiskEncryption** parancsmag letiltja a titkosítást egy infrastruktúrában Service (IaaS) virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="59daf-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="59daf-107">Ez a parancsmag csak a Windows virtuális gépeken támogatott, a Linux virtuális gépeken nem.</span><span class="sxs-lookup"><span data-stu-id="59daf-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="59daf-108">Ez a parancsmag a virtuális gép kiterjesztését telepíti a titkosítás letiltásához.</span><span class="sxs-lookup"><span data-stu-id="59daf-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="59daf-109">Ha a *Name* paraméter nincs megadva, létrejön egy, a "AzureDiskEncryption for Windows VMS" nevű alapértelmezett név nevű kiterjesztés.</span><span class="sxs-lookup"><span data-stu-id="59daf-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="59daf-110">Figyelmeztetés: Ez a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="59daf-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="59daf-111">Példák</span><span class="sxs-lookup"><span data-stu-id="59daf-111">EXAMPLES</span></span>

### <span data-ttu-id="59daf-112">1. példa: a Windows Virtual Machine minden kötete titkosításának letiltása</span><span class="sxs-lookup"><span data-stu-id="59daf-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="59daf-113">Ez a parancs letiltja a titkosítást az összes típusa az Group001 nevű erőforráscsoport VM002 nevű virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="59daf-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="59daf-114">Mivel a *VolumeType* paraméter nincs megadva, a parancsmag az összes értéket állítja be.</span><span class="sxs-lookup"><span data-stu-id="59daf-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="59daf-115">2. példa: Az adatkötetek titkosításának letiltása Windows virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="59daf-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

<span data-ttu-id="59daf-116">Ez a parancs letiltja a VM004 nevű virtuális gép adattípusának titkosítását, amely a Group002 nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="59daf-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="59daf-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="59daf-117">PARAMETERS</span></span>

### <span data-ttu-id="59daf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59daf-118">-DefaultProfile</span></span>
<span data-ttu-id="59daf-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="59daf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59daf-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="59daf-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="59daf-121">Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziójának automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="59daf-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="59daf-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="59daf-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="59daf-123">A bővítmény közzétevője név.</span><span class="sxs-lookup"><span data-stu-id="59daf-123">The extension publisher name.</span></span> <span data-ttu-id="59daf-124">Csak akkor adja meg ezt a paramétert, ha a "Microsoft. Azure. Security" alapértelmezett értékét szeretné felülbírálni.</span><span class="sxs-lookup"><span data-stu-id="59daf-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="59daf-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="59daf-125">-ExtensionType</span></span>
<span data-ttu-id="59daf-126">A bővítmény típusa.</span><span class="sxs-lookup"><span data-stu-id="59daf-126">The extension type.</span></span> <span data-ttu-id="59daf-127">Adja meg ezt a paramétert, ha a Windows VMs "AzureDiskEncryption" alapértelmezett értékét szeretné felülbírálni, és a Linux VMs esetében a "AzureDiskEncryptionForLinux".</span><span class="sxs-lookup"><span data-stu-id="59daf-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="59daf-128">-Force</span><span class="sxs-lookup"><span data-stu-id="59daf-128">-Force</span></span>
<span data-ttu-id="59daf-129">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="59daf-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="59daf-130">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="59daf-130">-Name</span></span>
<span data-ttu-id="59daf-131">A kiterjesztést jelképező Azure Resource Manager (ARM) erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59daf-131">Specifies the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="59daf-132">Ha ez a paraméter nincs megadva, ez a parancsmag alapértelmezés szerint "AzureDiskEncryption Windows VMs-re".</span><span class="sxs-lookup"><span data-stu-id="59daf-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="59daf-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59daf-133">-ResourceGroupName</span></span>
<span data-ttu-id="59daf-134">A virtuális gép erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="59daf-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="59daf-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="59daf-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="59daf-136">A titkosítási bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59daf-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="59daf-137">Ha nem ad meg értéket ehhez a paraméterhez, a program a bővítmény legújabb verzióját használja.</span><span class="sxs-lookup"><span data-stu-id="59daf-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="59daf-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="59daf-138">-VMName</span></span>
<span data-ttu-id="59daf-139">Annak a virtuális gépnek a nevét adja meg, amelyre a parancsmag letiltja a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="59daf-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="59daf-140">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="59daf-140">-VolumeType</span></span>
<span data-ttu-id="59daf-141">A titkosítási művelet végrehajtásához használt virtuálisgép-kötetek típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="59daf-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="59daf-142">Windows virtuális gépek esetén az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="59daf-142">For Windows virtual machines, valid values are:</span></span> 
- <span data-ttu-id="59daf-143">Minden</span><span class="sxs-lookup"><span data-stu-id="59daf-143">All</span></span>
- <span data-ttu-id="59daf-144">OS</span><span class="sxs-lookup"><span data-stu-id="59daf-144">OS</span></span>
- <span data-ttu-id="59daf-145">Adatok.</span><span class="sxs-lookup"><span data-stu-id="59daf-145">Data.</span></span>
<span data-ttu-id="59daf-146">Ha nem ad meg értéket ehhez a paraméterhez, az alapértelmezett érték az összes.</span><span class="sxs-lookup"><span data-stu-id="59daf-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="59daf-147">A titkosítás letiltása a Linuxban jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="59daf-147">Disable encryption is not currently supported for Linux.</span></span>

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

### <span data-ttu-id="59daf-148">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="59daf-148">-Confirm</span></span>
<span data-ttu-id="59daf-149">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="59daf-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59daf-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59daf-150">-WhatIf</span></span>
<span data-ttu-id="59daf-151">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="59daf-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59daf-152">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="59daf-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59daf-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59daf-153">CommonParameters</span></span>
<span data-ttu-id="59daf-154">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="59daf-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59daf-155">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="59daf-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59daf-156">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="59daf-156">INPUTS</span></span>

### <span data-ttu-id="59daf-157">System. String</span><span class="sxs-lookup"><span data-stu-id="59daf-157">System.String</span></span>

### <span data-ttu-id="59daf-158">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="59daf-158">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="59daf-159">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="59daf-159">OUTPUTS</span></span>

### <span data-ttu-id="59daf-160">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="59daf-160">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="59daf-161">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="59daf-161">NOTES</span></span>

## <span data-ttu-id="59daf-162">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="59daf-162">RELATED LINKS</span></span>

[<span data-ttu-id="59daf-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="59daf-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="59daf-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="59daf-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="59daf-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="59daf-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


