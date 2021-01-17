---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480759"
---
# <span data-ttu-id="61e8c-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="61e8c-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="61e8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="61e8c-103">Eltávolítja a lemeztitkosítási bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="61e8c-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="61e8c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="61e8c-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61e8c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="61e8c-105">DESCRIPTION</span></span>
<span data-ttu-id="61e8c-106">A **Remove-AzVMDiskEncryptionExtension** parancsmag eltávolítja a lemeztitkosítási bővítményt és a hozzá tartozó bővítménykonfigurációt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="61e8c-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="61e8c-107">Ha nincs megadva bővítménynév, ez a parancsmag eltávolítja az alapértelmezett AzureDiskEncryption nevű bővítményt a Windows operációs rendszert vagy a Linux-alapú AzureDiskEncryptionForLinux virtuális gépeket futtató virtuális gépek esetén.</span><span class="sxs-lookup"><span data-stu-id="61e8c-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="61e8c-108">Ez a parancsmag nem fog működni, ha a virtuális gépen a titkosítást először nem tiltották le.</span><span class="sxs-lookup"><span data-stu-id="61e8c-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="61e8c-109">Virtuális gép titkosításának letiltásához használja a [Disable-AzVMDiskEncryption eszközt.](./Disable-AzVMDiskEncryption.md)</span><span class="sxs-lookup"><span data-stu-id="61e8c-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="61e8c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="61e8c-110">EXAMPLES</span></span>

### <span data-ttu-id="61e8c-111">1. példa: Távolítsa el a lemeztitkosítási bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="61e8c-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="61e8c-112">Ez a parancs eltávolítja a bővítmény alapértelmezett AzureDiskEncryption nevű bővítményét egy Olyan virtuális gép esetén, amely a Windows operációs rendszert vagy a Linux AzureDiskEncryptionForLinux virtuális gépét futtatja MyTestVM néven.</span><span class="sxs-lookup"><span data-stu-id="61e8c-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="61e8c-113">2. példa: Eltávolíthat egy adott lemeztitkosítási bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="61e8c-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="61e8c-114">Ez a parancs eltávolítja a MyDiskEncryptionExtension nevű titkosítási bővítményt a MyTestVM nevű virtuális gépből.</span><span class="sxs-lookup"><span data-stu-id="61e8c-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="61e8c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61e8c-115">PARAMETERS</span></span>

### <span data-ttu-id="61e8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e8c-116">-DefaultProfile</span></span>
<span data-ttu-id="61e8c-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61e8c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61e8c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="61e8c-118">-Force</span></span>
<span data-ttu-id="61e8c-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="61e8c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="61e8c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="61e8c-120">-Name</span></span>
<span data-ttu-id="61e8c-121">A bővítményt képviselő Azure Resource Manager-erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="61e8c-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="61e8c-122">A Set-AzVMDiskEncryptionExtension parancsmag az AzureDiskEncryption nevet állítja be a Windows operációs rendszert és a Linux azurediskencryptionForLinux virtuális gépeket futtató virtuális gépeken.</span><span class="sxs-lookup"><span data-stu-id="61e8c-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="61e8c-123">Ezt a paramétert csak akkor adja meg, ha módosította az alapértelmezett nevet a **Set-AzVMDiskEncryptionExtension** parancsmagban, vagy másik erőforrásnevet használt egy Erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="61e8c-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="61e8c-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="61e8c-124">-NoWait</span></span>
<span data-ttu-id="61e8c-125">Elindítja a műveletet, és azonnal, a művelet befejezése előtt visszatér.</span><span class="sxs-lookup"><span data-stu-id="61e8c-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="61e8c-126">Ha meg szeretné állapítani, hogy a művelet sikeresen befejeződött-e, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="61e8c-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="61e8c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61e8c-127">-ResourceGroupName</span></span>
<span data-ttu-id="61e8c-128">A virtuális gép erőforráscsoportját adja meg.</span><span class="sxs-lookup"><span data-stu-id="61e8c-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="61e8c-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="61e8c-129">-VMName</span></span>
<span data-ttu-id="61e8c-130">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="61e8c-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="61e8c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61e8c-131">-Confirm</span></span>
<span data-ttu-id="61e8c-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="61e8c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61e8c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e8c-133">-WhatIf</span></span>
<span data-ttu-id="61e8c-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="61e8c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61e8c-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="61e8c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61e8c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e8c-136">CommonParameters</span></span>
<span data-ttu-id="61e8c-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61e8c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e8c-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61e8c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e8c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61e8c-139">INPUTS</span></span>

### <span data-ttu-id="61e8c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="61e8c-140">System.String</span></span>

## <span data-ttu-id="61e8c-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61e8c-141">OUTPUTS</span></span>

### <span data-ttu-id="61e8c-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="61e8c-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="61e8c-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="61e8c-143">NOTES</span></span>

## <span data-ttu-id="61e8c-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61e8c-144">RELATED LINKS</span></span>

[<span data-ttu-id="61e8c-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="61e8c-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="61e8c-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="61e8c-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


