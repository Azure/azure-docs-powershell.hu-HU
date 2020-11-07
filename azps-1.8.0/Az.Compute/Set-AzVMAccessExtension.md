---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0b91e2892f087da6eb510d087980e6f31dd67ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671238"
---
# <span data-ttu-id="406de-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="406de-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="406de-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="406de-102">SYNOPSIS</span></span>
<span data-ttu-id="406de-103">A VMAccess bővítmény felvétele egy virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="406de-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="406de-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="406de-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="406de-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="406de-105">DESCRIPTION</span></span>
<span data-ttu-id="406de-106">A **set-AzVMAccessExtension** parancsmag hozzáadja a Virtual Machine Access (VMAccess) Virtual Machine VMAccess bővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="406de-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="406de-107">Az VMAccess-kiterjesztéssel ideiglenes jelszót állíthat be, ezért ezt azonnal módosítania kell a gépbe való bejelentkezés után.</span><span class="sxs-lookup"><span data-stu-id="406de-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="406de-108">Windows-tartományvezérlőkön ez a funkció nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="406de-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="406de-109">Példák</span><span class="sxs-lookup"><span data-stu-id="406de-109">EXAMPLES</span></span>

### <span data-ttu-id="406de-110">Példa 1: VMAccess bővítmény felvétele</span><span class="sxs-lookup"><span data-stu-id="406de-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="406de-111">Ez a parancs összead egy VMAccess-kiterjesztést a VirtualMachine07 nevű virtuális gépnek a ResrouceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="406de-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="406de-112">A parancs a VMAccess név és típus kezelőjének verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="406de-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="406de-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="406de-113">PARAMETERS</span></span>

### <span data-ttu-id="406de-114">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="406de-114">-Credential</span></span>
<span data-ttu-id="406de-115">A virtuális gép **PSCredential** -objektumként használt felhasználónevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="406de-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="406de-116">Ha a VM-ben a jelenlegi helyi rendszergazdai fióktól eltérő nevet ad meg, a VMAccess bővítmény egy helyi rendszergazdai fiókot ad hozzá az adott névhez, és hozzárendeli a megadott jelszót az adott fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="406de-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="406de-117">Ha a VM helyi rendszergazdai fiókja létezik, a rendszer alaphelyzetbe állítja a jelszót, és ha a fiók le van tiltva, az VMAccess bővítmény engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="406de-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="406de-118">Hitelesítő adatok beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="406de-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="406de-119">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="406de-119">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="406de-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="406de-120">-DefaultProfile</span></span>
<span data-ttu-id="406de-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="406de-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="406de-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="406de-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="406de-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="406de-123">-ForceRerun</span></span>
<span data-ttu-id="406de-124">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="406de-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="406de-125">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="406de-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="406de-126">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="406de-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="406de-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="406de-127">-Location</span></span>
<span data-ttu-id="406de-128">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="406de-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="406de-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="406de-129">-Name</span></span>
<span data-ttu-id="406de-130">Itt adhatja meg annak a bővítménynek a nevét, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="406de-130">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="406de-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="406de-131">-ResourceGroupName</span></span>
<span data-ttu-id="406de-132">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="406de-132">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="406de-133">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="406de-133">-TypeHandlerVersion</span></span>
<span data-ttu-id="406de-134">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="406de-134">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="406de-135">A verzió beolvasásához futtassa a Get-AzVMExtensionImage-parancsmagot a Microsoft. számítás értékével, és adja meg a *PublisherName* paramétert és a VMAccessAgent a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="406de-135">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="406de-136">A typeHandlerVersion 2,0 vagy nagyobbnak kell lennie, mivel az 1-es verzió elavult.</span><span class="sxs-lookup"><span data-stu-id="406de-136">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="406de-137">-VMName</span><span class="sxs-lookup"><span data-stu-id="406de-137">-VMName</span></span>
<span data-ttu-id="406de-138">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="406de-138">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="406de-139">Ez a parancsmag hozzáadja a VMAccess a virtuális géphez, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="406de-139">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="406de-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="406de-140">-Confirm</span></span>
<span data-ttu-id="406de-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="406de-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="406de-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="406de-142">-WhatIf</span></span>
<span data-ttu-id="406de-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="406de-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="406de-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="406de-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="406de-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="406de-145">CommonParameters</span></span>
<span data-ttu-id="406de-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="406de-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="406de-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="406de-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="406de-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="406de-148">INPUTS</span></span>

### <span data-ttu-id="406de-149">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="406de-149">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="406de-150">System. String</span><span class="sxs-lookup"><span data-stu-id="406de-150">System.String</span></span>

### <span data-ttu-id="406de-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="406de-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="406de-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="406de-152">OUTPUTS</span></span>

### <span data-ttu-id="406de-153">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="406de-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="406de-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="406de-154">NOTES</span></span>

## <span data-ttu-id="406de-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="406de-155">RELATED LINKS</span></span>

[<span data-ttu-id="406de-156">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="406de-156">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="406de-157">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="406de-157">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="406de-158">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="406de-158">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="406de-159">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="406de-159">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


