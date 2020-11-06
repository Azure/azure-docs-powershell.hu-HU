---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 087ae12961d6bd9faf844221772b92c79362d13d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496644"
---
# <span data-ttu-id="6062e-101">Disable-AzureRmVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="6062e-101">Disable-AzureRmVMDiskEncryption</span></span>

## <span data-ttu-id="6062e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6062e-102">SYNOPSIS</span></span>
<span data-ttu-id="6062e-103">Letiltja a titkosítást egy IaaS virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="6062e-103">Disables encryption on an IaaS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6062e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6062e-104">SYNTAX</span></span>

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6062e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6062e-105">DESCRIPTION</span></span>
<span data-ttu-id="6062e-106">A **disable-AzureRmVMDiskEncryption** parancsmag letiltja a titkosítást egy infrastruktúrában Service (IaaS) virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="6062e-106">The **Disable-AzureRmVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="6062e-107">Ez a parancsmag csak a Windows virtuális gépeken támogatott, a Linux virtuális gépeken nem.</span><span class="sxs-lookup"><span data-stu-id="6062e-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="6062e-108">Ez a parancsmag a virtuális gép kiterjesztését telepíti a titkosítás letiltásához.</span><span class="sxs-lookup"><span data-stu-id="6062e-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="6062e-109">Ha a *Name* paraméter nincs megadva, létrejön egy, a "AzureDiskEncryption for Windows VMS" nevű alapértelmezett név nevű kiterjesztés.</span><span class="sxs-lookup"><span data-stu-id="6062e-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="6062e-110">Figyelmeztetés: Ez a parancsmag újraindítja a virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="6062e-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="6062e-111">Példák</span><span class="sxs-lookup"><span data-stu-id="6062e-111">EXAMPLES</span></span>

### <span data-ttu-id="6062e-112">1. példa: a Windows Virtual Machine minden kötete titkosításának letiltása</span><span class="sxs-lookup"><span data-stu-id="6062e-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="6062e-113">Ez a parancs letiltja a titkosítást az összes típusa az Group001 nevű erőforráscsoport VM002 nevű virtuális gépnek.</span><span class="sxs-lookup"><span data-stu-id="6062e-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="6062e-114">Mivel a *VolumeType* paraméter nincs megadva, a parancsmag az összes értéket állítja be.</span><span class="sxs-lookup"><span data-stu-id="6062e-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="6062e-115">2. példa: Az adatkötetek titkosításának letiltása Windows virtuális gépen</span><span class="sxs-lookup"><span data-stu-id="6062e-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="6062e-116">Ez a parancs letiltja a VM004 nevű virtuális gép adattípusának titkosítását, amely a Group002 nevű erőforráscsoport nevéhez tartozik.</span><span class="sxs-lookup"><span data-stu-id="6062e-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="6062e-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6062e-117">PARAMETERS</span></span>

### <span data-ttu-id="6062e-118">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6062e-118">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6062e-119">Azt jelzi, hogy ez a parancsmag letiltja a bővítmény alverziójának automatikus frissítését.</span><span class="sxs-lookup"><span data-stu-id="6062e-119">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="6062e-120">-Force</span></span>
<span data-ttu-id="6062e-121">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6062e-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6062e-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6062e-122">-Name</span></span>
<span data-ttu-id="6062e-123">A Specifes a bővítményt jelképező Azure Resource Manager (ARM) erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6062e-123">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="6062e-124">Ha ez a paraméter nincs megadva, ez a parancsmag alapértelmezés szerint "AzureDiskEncryption Windows VMs-re".</span><span class="sxs-lookup"><span data-stu-id="6062e-124">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6062e-125">-ResourceGroupName</span></span>
<span data-ttu-id="6062e-126">A virtuális gép erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6062e-126">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="6062e-127">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6062e-127">-TypeHandlerVersion</span></span>
<span data-ttu-id="6062e-128">A titkosítási bővítmény verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6062e-128">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="6062e-129">Ha nem ad meg értéket ehhez a paraméterhez, a program a bővítmény legújabb verzióját használja.</span><span class="sxs-lookup"><span data-stu-id="6062e-129">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="6062e-130">-VMName</span></span>
<span data-ttu-id="6062e-131">Annak a virtuális gépnek a nevét adja meg, amelyre a parancsmag letiltja a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="6062e-131">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-132">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="6062e-132">-VolumeType</span></span>
<span data-ttu-id="6062e-133">A titkosítási művelet végrehajtásához használt virtuálisgép-kötetek típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="6062e-133">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="6062e-134">Windows virtuális gépek esetén az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="6062e-134">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="6062e-135">Minden</span><span class="sxs-lookup"><span data-stu-id="6062e-135">All</span></span>
- <span data-ttu-id="6062e-136">OS</span><span class="sxs-lookup"><span data-stu-id="6062e-136">OS</span></span>
- <span data-ttu-id="6062e-137">Adatok.</span><span class="sxs-lookup"><span data-stu-id="6062e-137">Data.</span></span>
<span data-ttu-id="6062e-138">Ha nem ad meg értéket ehhez a paraméterhez, az alapértelmezett érték az összes.</span><span class="sxs-lookup"><span data-stu-id="6062e-138">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="6062e-139">A titkosítás letiltása a Linuxban jelenleg nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="6062e-139">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6062e-140">-Confirm</span></span>
<span data-ttu-id="6062e-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6062e-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6062e-142">-WhatIf</span></span>
<span data-ttu-id="6062e-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6062e-143">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6062e-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6062e-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6062e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6062e-145">CommonParameters</span></span>
<span data-ttu-id="6062e-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6062e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6062e-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6062e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6062e-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6062e-148">INPUTS</span></span>

### <span data-ttu-id="6062e-149">Nincs</span><span class="sxs-lookup"><span data-stu-id="6062e-149">None</span></span>
<span data-ttu-id="6062e-150">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6062e-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6062e-151">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6062e-151">OUTPUTS</span></span>

### <span data-ttu-id="6062e-152">Ez a parancsmag semmilyen kimenetet nem hoz létre.</span><span class="sxs-lookup"><span data-stu-id="6062e-152">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6062e-153">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6062e-153">NOTES</span></span>

## <span data-ttu-id="6062e-154">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6062e-154">RELATED LINKS</span></span>

[<span data-ttu-id="6062e-155">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="6062e-155">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="6062e-156">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="6062e-156">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="6062e-157">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="6062e-157">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


