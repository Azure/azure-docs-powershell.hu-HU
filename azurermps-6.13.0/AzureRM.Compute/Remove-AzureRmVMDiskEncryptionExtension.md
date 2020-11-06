---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: a1a077ff6abec8dc2b0b77ef7f3b9c17ca2f1b46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502203"
---
# <span data-ttu-id="ad1b3-101">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="ad1b3-101">Remove-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="ad1b3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ad1b3-103">Eltávolítja a titkosítási bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-103">Removes the disk encryption extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad1b3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad1b3-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad1b3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad1b3-105">DESCRIPTION</span></span>
<span data-ttu-id="ad1b3-106">A **Remove-AzureRmVMDiskEncryptionExtension** parancsmag eltávolítja a titkosítási bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-106">The **Remove-AzureRmVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="ad1b3-107">Ha nincs megadva a bővítmény neve, ez a parancsmag eltávolítja a Windows operációs rendszert futtató virtuális gépekhez használt alapértelmezett név AzureDiskEncryption, illetve a AzureDiskEncryptionForLinux a Linux-alapú virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="ad1b3-108">Ez a parancsmag nem tiltja le a titkosítást a virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="ad1b3-109">Eltávolítja a virtuális gépről a kiterjesztést és a hozzá tartozó bővítmény-konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="ad1b3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="ad1b3-110">EXAMPLES</span></span>

### <span data-ttu-id="ad1b3-111">1. példa: a lemez titkosítási bővítményének eltávolítása virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="ad1b3-112">Ez a parancs eltávolítja a bővítményt az alapértelmezett név AzureDiskEncryption, amely a Windows operációs rendszert futtató virtuális gép vagy a AzureDiskEncryptionForLinux a MyTestVM nevű virtuális gépre épül.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="ad1b3-113">2. példa: az adott titkosítási bővítmény eltávolítása egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="ad1b3-114">Ez a parancs eltávolítja a MyDiskEncryptionExtension nevű titkosítási bővítményt a MyTestVM nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="ad1b3-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad1b3-115">PARAMETERS</span></span>

### <span data-ttu-id="ad1b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad1b3-116">-DefaultProfile</span></span>
<span data-ttu-id="ad1b3-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad1b3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ad1b3-118">-Force</span></span>
<span data-ttu-id="ad1b3-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad1b3-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ad1b3-120">-Name</span></span>
<span data-ttu-id="ad1b3-121">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="ad1b3-122">A Set-AzureRmVMDiskEncryptionExtension parancsmag ezt a nevet a AzureDiskEncryption-ra állítja be a Windows operációs rendszert futtató virtuális gépekhez és a AzureDiskEncryptionForLinux for Linux virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-122">The Set-AzureRmVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="ad1b3-123">Csak akkor adja meg ezt a paramétert, ha módosította az alapértelmezett nevet a **set-AzureRmVMDiskEncryptionExtension** parancsmagban, vagy másik erőforrás nevét használta egy erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-123">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad1b3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad1b3-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad1b3-125">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-125">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="ad1b3-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="ad1b3-126">-VMName</span></span>
<span data-ttu-id="ad1b3-127">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-127">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="ad1b3-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ad1b3-128">-Confirm</span></span>
<span data-ttu-id="ad1b3-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad1b3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad1b3-130">-WhatIf</span></span>
<span data-ttu-id="ad1b3-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad1b3-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ad1b3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad1b3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad1b3-133">CommonParameters</span></span>
<span data-ttu-id="ad1b3-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad1b3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad1b3-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad1b3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad1b3-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad1b3-136">INPUTS</span></span>

### <span data-ttu-id="ad1b3-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ad1b3-137">System.String</span></span>

## <span data-ttu-id="ad1b3-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad1b3-138">OUTPUTS</span></span>

### <span data-ttu-id="ad1b3-139">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ad1b3-139">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ad1b3-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad1b3-140">NOTES</span></span>

## <span data-ttu-id="ad1b3-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad1b3-141">RELATED LINKS</span></span>

[<span data-ttu-id="ad1b3-142">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="ad1b3-142">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="ad1b3-143">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="ad1b3-143">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)

