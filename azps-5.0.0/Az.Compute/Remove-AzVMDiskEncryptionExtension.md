---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186240"
---
# <span data-ttu-id="87d54-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="87d54-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="87d54-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87d54-102">SYNOPSIS</span></span>
<span data-ttu-id="87d54-103">Eltávolítja a titkosítási bővítményt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="87d54-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="87d54-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87d54-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87d54-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="87d54-105">DESCRIPTION</span></span>
<span data-ttu-id="87d54-106">A **Remove-AzVMDiskEncryptionExtension** parancsmag eltávolítja a lemez titkosítási bővítményét és a hozzá tartozó bővítmény-konfigurációt egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="87d54-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="87d54-107">Ha nincs megadva a bővítmény neve, ez a parancsmag eltávolítja a Windows operációs rendszert futtató virtuális gépekhez használt alapértelmezett név AzureDiskEncryption, illetve a AzureDiskEncryptionForLinux a Linux-alapú virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="87d54-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="87d54-108">Ez a parancsmag akkor lép fel, ha a virtuális gép titkosítását nem sikerült először letiltani.</span><span class="sxs-lookup"><span data-stu-id="87d54-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="87d54-109">Ha le szeretné tiltani a titkosítást egy virtuális gépen, használja a [disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span><span class="sxs-lookup"><span data-stu-id="87d54-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="87d54-110">Példák</span><span class="sxs-lookup"><span data-stu-id="87d54-110">EXAMPLES</span></span>

### <span data-ttu-id="87d54-111">1. példa: a lemez titkosítási bővítményének eltávolítása virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="87d54-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="87d54-112">Ez a parancs eltávolítja a bővítményt az alapértelmezett név AzureDiskEncryption, amely a Windows operációs rendszert futtató virtuális gép vagy a AzureDiskEncryptionForLinux a MyTestVM nevű virtuális gépre épül.</span><span class="sxs-lookup"><span data-stu-id="87d54-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="87d54-113">2. példa: az adott titkosítási bővítmény eltávolítása egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="87d54-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="87d54-114">Ez a parancs eltávolítja a MyDiskEncryptionExtension nevű titkosítási bővítményt a MyTestVM nevű virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="87d54-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="87d54-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87d54-115">PARAMETERS</span></span>

### <span data-ttu-id="87d54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d54-116">-DefaultProfile</span></span>
<span data-ttu-id="87d54-117">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="87d54-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87d54-118">-Force</span><span class="sxs-lookup"><span data-stu-id="87d54-118">-Force</span></span>
<span data-ttu-id="87d54-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="87d54-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="87d54-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="87d54-120">-Name</span></span>
<span data-ttu-id="87d54-121">A bővítményt jelképező Azure Resource Manager-erőforrás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87d54-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="87d54-122">A Set-AzVMDiskEncryptionExtension parancsmag ezt a nevet a AzureDiskEncryption-ra állítja be a Windows operációs rendszert futtató virtuális gépekhez és a AzureDiskEncryptionForLinux for Linux virtuális gépekhez.</span><span class="sxs-lookup"><span data-stu-id="87d54-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="87d54-123">Csak akkor adja meg ezt a paramétert, ha módosította az alapértelmezett nevet a **set-AzVMDiskEncryptionExtension** parancsmagban, vagy másik erőforrás nevét használta egy erőforrás-kezelő sablonban.</span><span class="sxs-lookup"><span data-stu-id="87d54-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="87d54-124">-Várva</span><span class="sxs-lookup"><span data-stu-id="87d54-124">-NoWait</span></span>
<span data-ttu-id="87d54-125">Elindítja a műveletet, és a művelet befejezése előtt azonnal visszaküldi a műveletet.</span><span class="sxs-lookup"><span data-stu-id="87d54-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="87d54-126">Ha meg szeretné állapítani, hogy sikerült-e végrehajtani a műveletet, használjon más mechanizmust.</span><span class="sxs-lookup"><span data-stu-id="87d54-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="87d54-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d54-127">-ResourceGroupName</span></span>
<span data-ttu-id="87d54-128">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87d54-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="87d54-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="87d54-129">-VMName</span></span>
<span data-ttu-id="87d54-130">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87d54-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="87d54-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="87d54-131">-Confirm</span></span>
<span data-ttu-id="87d54-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87d54-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87d54-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87d54-133">-WhatIf</span></span>
<span data-ttu-id="87d54-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="87d54-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87d54-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="87d54-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87d54-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d54-136">CommonParameters</span></span>
<span data-ttu-id="87d54-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87d54-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d54-138">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="87d54-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d54-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87d54-139">INPUTS</span></span>

### <span data-ttu-id="87d54-140">System. String</span><span class="sxs-lookup"><span data-stu-id="87d54-140">System.String</span></span>

## <span data-ttu-id="87d54-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87d54-141">OUTPUTS</span></span>

### <span data-ttu-id="87d54-142">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="87d54-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="87d54-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87d54-143">NOTES</span></span>

## <span data-ttu-id="87d54-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87d54-144">RELATED LINKS</span></span>

[<span data-ttu-id="87d54-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="87d54-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="87d54-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="87d54-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


