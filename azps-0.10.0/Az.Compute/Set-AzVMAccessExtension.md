---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0335a063e810a94e6d557986e682ec4c777e5c1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844250"
---
# <span data-ttu-id="5b908-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5b908-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="5b908-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b908-102">SYNOPSIS</span></span>
<span data-ttu-id="5b908-103">A VMAccess bővítmény felvétele egy virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="5b908-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="5b908-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b908-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b908-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b908-105">DESCRIPTION</span></span>
<span data-ttu-id="5b908-106">A **set-AzVMAccessExtension** parancsmag hozzáadja a Virtual Machine Access (VMAccess) Virtual Machine VMAccess bővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="5b908-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="5b908-107">Az VMAccess-kiterjesztéssel ideiglenes jelszót állíthat be, ezért ezt azonnal módosítania kell a gépbe való bejelentkezés után.</span><span class="sxs-lookup"><span data-stu-id="5b908-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="5b908-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5b908-108">EXAMPLES</span></span>

### <span data-ttu-id="5b908-109">Példa 1: VMAccess bővítmény felvétele</span><span class="sxs-lookup"><span data-stu-id="5b908-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="5b908-110">Ez a parancs összead egy VMAccess-kiterjesztést a VirtualMachine07 nevű virtuális gépnek a ResrouceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="5b908-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="5b908-111">A parancs a VMAccess név és típus kezelőjének verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b908-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="5b908-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b908-112">PARAMETERS</span></span>

### <span data-ttu-id="5b908-113">-Hitelesítő adatok</span><span class="sxs-lookup"><span data-stu-id="5b908-113">-Credential</span></span>
<span data-ttu-id="5b908-114">A virtuális gép **PSCredential** -objektumként használt felhasználónevét és jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b908-114">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="5b908-115">Hitelesítő adatok beolvasásához használja az Get-Credential parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5b908-115">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="5b908-116">További információért írja be a következőt: `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="5b908-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b908-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b908-117">-DefaultProfile</span></span>
<span data-ttu-id="5b908-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5b908-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b908-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5b908-119">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b908-120">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="5b908-120">-ForceRerun</span></span>
<span data-ttu-id="5b908-121">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="5b908-121">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="5b908-122">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="5b908-122">The value can be any string different from the current value.</span></span>

<span data-ttu-id="5b908-123">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="5b908-123">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b908-124">-Hely</span><span class="sxs-lookup"><span data-stu-id="5b908-124">-Location</span></span>
<span data-ttu-id="5b908-125">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b908-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b908-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5b908-126">-Name</span></span>
<span data-ttu-id="5b908-127">Itt adhatja meg annak a bővítménynek a nevét, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="5b908-127">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b908-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b908-128">-ResourceGroupName</span></span>
<span data-ttu-id="5b908-129">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b908-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5b908-130">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5b908-130">-TypeHandlerVersion</span></span>
<span data-ttu-id="5b908-131">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="5b908-131">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="5b908-132">A verzió beolvasásához futtassa a Get-AzVMExtensionImage-parancsmagot a Microsoft. számítás értékével, és adja meg a *PublisherName* paramétert és a VMAccessAgent a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="5b908-132">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b908-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="5b908-133">-VMName</span></span>
<span data-ttu-id="5b908-134">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b908-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5b908-135">Ez a parancsmag hozzáadja a VMAccess a virtuális géphez, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="5b908-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b908-136">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5b908-136">-Confirm</span></span>
<span data-ttu-id="5b908-137">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5b908-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b908-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b908-138">-WhatIf</span></span>
<span data-ttu-id="5b908-139">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5b908-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5b908-140">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5b908-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b908-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b908-141">CommonParameters</span></span>
<span data-ttu-id="5b908-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b908-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b908-143">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b908-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b908-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b908-144">INPUTS</span></span>

### <span data-ttu-id="5b908-145">Nincs</span><span class="sxs-lookup"><span data-stu-id="5b908-145">None</span></span>
<span data-ttu-id="5b908-146">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="5b908-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b908-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b908-147">OUTPUTS</span></span>

### <span data-ttu-id="5b908-148">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5b908-148">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5b908-149">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b908-149">NOTES</span></span>

## <span data-ttu-id="5b908-150">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b908-150">RELATED LINKS</span></span>

[<span data-ttu-id="5b908-151">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5b908-151">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="5b908-152">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="5b908-152">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="5b908-153">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="5b908-153">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="5b908-154">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="5b908-154">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


