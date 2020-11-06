---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: 0a2d3ce354a5039db21fdd336f6f2d64efdb56fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504452"
---
# <span data-ttu-id="1d36d-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1d36d-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="1d36d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d36d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d36d-103">A VMAccess bővítmény felvétele egy virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="1d36d-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d36d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d36d-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d36d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d36d-105">DESCRIPTION</span></span>
<span data-ttu-id="1d36d-106">A **set-AzureRmVMAccessExtension** parancsmag hozzáadja a Virtual Machine Access (VMAccess) Virtual Machine VMAccess bővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="1d36d-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="1d36d-107">Az VMAccess-kiterjesztéssel ideiglenes jelszót állíthat be, ezért ezt azonnal módosítania kell a gépbe való bejelentkezés után.</span><span class="sxs-lookup"><span data-stu-id="1d36d-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="1d36d-108">Windows-tartományvezérlőkön ez a funkció nem támogatott.</span><span class="sxs-lookup"><span data-stu-id="1d36d-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="1d36d-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1d36d-109">EXAMPLES</span></span>

### <span data-ttu-id="1d36d-110">Példa 1: VMAccess bővítmény felvétele</span><span class="sxs-lookup"><span data-stu-id="1d36d-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="1d36d-111">Ez a parancs összead egy VMAccess-kiterjesztést a VirtualMachine07 nevű virtuális gépnek a ResrouceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="1d36d-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="1d36d-112">A parancs a VMAccess név és típus kezelőjének verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d36d-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="1d36d-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d36d-113">PARAMETERS</span></span>

### <span data-ttu-id="1d36d-114">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="1d36d-114">-Credential</span></span>
<span data-ttu-id="1d36d-115">A virtuális gép **PSCredential** -objektumként használt felhasználónevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d36d-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="1d36d-116">Ha a VM-ben a jelenlegi helyi rendszergazdai fióktól eltérő nevet ad meg, a VMAccess bővítmény egy helyi rendszergazdai fiókot ad hozzá az adott névhez, és hozzárendeli a megadott jelszót az adott fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="1d36d-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="1d36d-117">Ha a VM helyi rendszergazdai fiókja létezik, a rendszer alaphelyzetbe állítja a jelszót, és ha a fiók le van tiltva, az VMAccess bővítmény engedélyezi.</span><span class="sxs-lookup"><span data-stu-id="1d36d-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="1d36d-118">Hitelesítő adatok beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1d36d-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="1d36d-119">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1d36d-119">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="1d36d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d36d-120">-DefaultProfile</span></span>
<span data-ttu-id="1d36d-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d36d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d36d-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1d36d-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="1d36d-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1d36d-123">-ForceRerun</span></span>
<span data-ttu-id="1d36d-124">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="1d36d-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="1d36d-125">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="1d36d-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="1d36d-126">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="1d36d-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="1d36d-127">-Hely</span><span class="sxs-lookup"><span data-stu-id="1d36d-127">-Location</span></span>
<span data-ttu-id="1d36d-128">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d36d-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="1d36d-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d36d-129">-Name</span></span>
<span data-ttu-id="1d36d-130">Itt adhatja meg annak a bővítménynek a nevét, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="1d36d-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="1d36d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d36d-131">-ResourceGroupName</span></span>
<span data-ttu-id="1d36d-132">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d36d-132">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1d36d-133">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1d36d-133">-TypeHandlerVersion</span></span>
<span data-ttu-id="1d36d-134">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="1d36d-134">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="1d36d-135">A verzió beolvasásához futtassa a Get-AzureRmVMExtensionImage-parancsmagot a Microsoft. számítás értékével, és adja meg a *PublisherName* paramétert és a VMAccessAgent a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="1d36d-135">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="1d36d-136">A typeHandlerVersion 2,0 vagy nagyobbnak kell lennie, mivel az 1-es verzió elavult.</span><span class="sxs-lookup"><span data-stu-id="1d36d-136">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="1d36d-137">-VMName</span><span class="sxs-lookup"><span data-stu-id="1d36d-137">-VMName</span></span>
<span data-ttu-id="1d36d-138">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d36d-138">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1d36d-139">Ez a parancsmag hozzáadja a VMAccess a virtuális géphez, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="1d36d-139">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1d36d-140">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1d36d-140">-Confirm</span></span>
<span data-ttu-id="1d36d-141">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1d36d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d36d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d36d-142">-WhatIf</span></span>
<span data-ttu-id="1d36d-143">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1d36d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d36d-144">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1d36d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d36d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d36d-145">CommonParameters</span></span>
<span data-ttu-id="1d36d-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d36d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d36d-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d36d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d36d-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d36d-148">INPUTS</span></span>

### <span data-ttu-id="1d36d-149">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="1d36d-149">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="1d36d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="1d36d-150">System.String</span></span>

### <span data-ttu-id="1d36d-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1d36d-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1d36d-152">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d36d-152">OUTPUTS</span></span>

### <span data-ttu-id="1d36d-153">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1d36d-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1d36d-154">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d36d-154">NOTES</span></span>

## <span data-ttu-id="1d36d-155">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d36d-155">RELATED LINKS</span></span>

[<span data-ttu-id="1d36d-156">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1d36d-156">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="1d36d-157">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1d36d-157">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="1d36d-158">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="1d36d-158">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="1d36d-159">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="1d36d-159">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


