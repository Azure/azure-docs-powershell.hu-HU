---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 9c9f7dca5bd698a0eda76637618fe946b723a576
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495426"
---
# <span data-ttu-id="31aae-101">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="31aae-101">Remove-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="31aae-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="31aae-102">SYNOPSIS</span></span>
<span data-ttu-id="31aae-103">Eltávolítja a titkosítási bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="31aae-103">Removes the disk encryption extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31aae-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="31aae-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31aae-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="31aae-105">DESCRIPTION</span></span>
<span data-ttu-id="31aae-106">A **Remove-AzureRmVMDiskEncryptionExtension** parancsmag eltávolítja a titkosítási bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="31aae-106">The **Remove-AzureRmVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="31aae-107">Ha nincs megadva a bővítmény neve, ez a parancsmag eltávolítja a Windows operációs rendszert futtató virtuális gépekhez használt alapértelmezett név AzureDiskEncryption, illetve a AzureDiskEncryptionForLinux a Linux-alapú virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="31aae-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="31aae-108">Ez a parancsmag nem tiltja le a titkosítást a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="31aae-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="31aae-109">Eltávolítja a virtuális gépről a kiterjesztést és a hozzá tartozó bővítmény-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="31aae-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="31aae-110">Példák</span><span class="sxs-lookup"><span data-stu-id="31aae-110">EXAMPLES</span></span>

### <span data-ttu-id="31aae-111">1. példa: a lemez titkosítási bővítményének eltávolítása virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="31aae-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="31aae-112">Ez a parancs eltávolítja a bővítményt az alapértelmezett név AzureDiskEncryption, amely a Windows operációs rendszert futtató virtuális gép vagy a AzureDiskEncryptionForLinux a MyTestVM nevű virtuális gépre épül.</span><span class="sxs-lookup"><span data-stu-id="31aae-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="31aae-113">2. példa: az adott titkosítási bővítmény eltávolítása egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="31aae-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="31aae-114">Ez a parancs eltávolítja a MyDiskEncryptionExtension nevű titkosítási bővítményt a MyTestVM nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="31aae-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="31aae-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="31aae-115">PARAMETERS</span></span>

### <span data-ttu-id="31aae-116">-Force</span><span class="sxs-lookup"><span data-stu-id="31aae-116">-Force</span></span>
<span data-ttu-id="31aae-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="31aae-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="31aae-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="31aae-118">-Name</span></span>
<span data-ttu-id="31aae-119">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31aae-119">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="31aae-120">A Set-AzureRmVMDiskEncryptionExtension parancsmag ezt a nevet a AzureDiskEncryption-ra állítja be a Windows operációs rendszert futtató virtuális gépekhez és a AzureDiskEncryptionForLinux for Linux virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="31aae-120">The Set-AzureRmVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="31aae-121">Csak akkor adja meg ezt a paramétert, ha módosította az alapértelmezett nevet a **set-AzureRmVMDiskEncryptionExtension** parancsmagban, vagy másik erőforrás nevét használta egy erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="31aae-121">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31aae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31aae-122">-ResourceGroupName</span></span>
<span data-ttu-id="31aae-123">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31aae-123">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="31aae-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="31aae-124">-VMName</span></span>
<span data-ttu-id="31aae-125">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="31aae-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="31aae-126">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="31aae-126">-Confirm</span></span>
<span data-ttu-id="31aae-127">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="31aae-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31aae-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31aae-128">-WhatIf</span></span>
<span data-ttu-id="31aae-129">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="31aae-129">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="31aae-130">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="31aae-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31aae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31aae-131">CommonParameters</span></span>
<span data-ttu-id="31aae-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="31aae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31aae-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31aae-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31aae-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="31aae-134">INPUTS</span></span>

### <span data-ttu-id="31aae-135">Nincs</span><span class="sxs-lookup"><span data-stu-id="31aae-135">None</span></span>
<span data-ttu-id="31aae-136">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="31aae-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31aae-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="31aae-137">OUTPUTS</span></span>

## <span data-ttu-id="31aae-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="31aae-138">NOTES</span></span>

## <span data-ttu-id="31aae-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="31aae-139">RELATED LINKS</span></span>

[<span data-ttu-id="31aae-140">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="31aae-140">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="31aae-141">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="31aae-141">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


