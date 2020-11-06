---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: 6c24c01ebff1d0a74835b968640caea6b5d2b308
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492355"
---
# <span data-ttu-id="3747a-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3747a-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="3747a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3747a-102">SYNOPSIS</span></span>
<span data-ttu-id="3747a-103">A VMAccess bővítmény felvétele egy virtuális gépre.</span><span class="sxs-lookup"><span data-stu-id="3747a-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3747a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3747a-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-UserName <String>] [-Password <String>] [-ResourceGroupName] <String>
 [-VMName] <String> [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3747a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3747a-105">DESCRIPTION</span></span>
<span data-ttu-id="3747a-106">A **set-AzureRmVMAccessExtension** parancsmag hozzáadja a Virtual Machine Access (VMAccess) Virtual Machine VMAccess bővítményt egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="3747a-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="3747a-107">Az VMAccess-kiterjesztéssel ideiglenes jelszót állíthat be, ezért ezt azonnal módosítania kell a gépbe való bejelentkezés után.</span><span class="sxs-lookup"><span data-stu-id="3747a-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="3747a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="3747a-108">EXAMPLES</span></span>

### <span data-ttu-id="3747a-109">Példa 1: VMAccess bővítmény felvétele</span><span class="sxs-lookup"><span data-stu-id="3747a-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="3747a-110">Ez a parancs összead egy VMAccess-kiterjesztést a VirtualMachine07 nevű virtuális gépnek a ResrouceGroup11-ban.</span><span class="sxs-lookup"><span data-stu-id="3747a-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="3747a-111">A parancs a VMAccess név és típus kezelőjének verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3747a-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="3747a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3747a-112">PARAMETERS</span></span>

### <span data-ttu-id="3747a-113">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3747a-113">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="3747a-114">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="3747a-114">-ForceRerun</span></span>
<span data-ttu-id="3747a-115">Azt jelzi, hogy ez a parancsmag a virtuális gép ugyanezt a bővítményét futtatja újra a bővítmény eltávolítása és újratelepítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="3747a-115">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="3747a-116">Az érték tetszőleges karakterlánc lehet, amely az aktuális értéktől eltérő lehet.</span><span class="sxs-lookup"><span data-stu-id="3747a-116">The value can be any string different from the current value.</span></span>

<span data-ttu-id="3747a-117">Ha a forceUpdateTag nem változik, a kezelő továbbra is alkalmazza a nyilvános vagy a védett beállításokra vonatkozó frissítéseket.</span><span class="sxs-lookup"><span data-stu-id="3747a-117">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="3747a-118">-Hely</span><span class="sxs-lookup"><span data-stu-id="3747a-118">-Location</span></span>
<span data-ttu-id="3747a-119">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3747a-119">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="3747a-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3747a-120">-Name</span></span>
<span data-ttu-id="3747a-121">Itt adhatja meg annak a bővítménynek a nevét, amelyet a parancsmag ad.</span><span class="sxs-lookup"><span data-stu-id="3747a-121">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="3747a-122">-Jelszó</span><span class="sxs-lookup"><span data-stu-id="3747a-122">-Password</span></span>
<span data-ttu-id="3747a-123">A virtuális gép új jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="3747a-123">Specifies the new password of the virtual machine.</span></span>

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

### <span data-ttu-id="3747a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3747a-124">-ResourceGroupName</span></span>
<span data-ttu-id="3747a-125">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3747a-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3747a-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3747a-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="3747a-127">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="3747a-127">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="3747a-128">A verzió beolvasásához futtassa a Get-AzureRmVMExtensionImage-parancsmagot a Microsoft. számítás értékével, és adja meg a *PublisherName* paramétert és a VMAccessAgent a *Type* paraméterhez.</span><span class="sxs-lookup"><span data-stu-id="3747a-128">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="3747a-129">-Felhasználónév</span><span class="sxs-lookup"><span data-stu-id="3747a-129">-UserName</span></span>
<span data-ttu-id="3747a-130">A virtuális gép új felhasználónevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3747a-130">Specifies the new user name for the virtual machine.</span></span>

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

### <span data-ttu-id="3747a-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="3747a-131">-VMName</span></span>
<span data-ttu-id="3747a-132">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3747a-132">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="3747a-133">Ez a parancsmag hozzáadja a VMAccess a virtuális géphez, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="3747a-133">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="3747a-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3747a-134">-Confirm</span></span>
<span data-ttu-id="3747a-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3747a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3747a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3747a-136">-WhatIf</span></span>
<span data-ttu-id="3747a-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3747a-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3747a-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3747a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3747a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3747a-139">CommonParameters</span></span>
<span data-ttu-id="3747a-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3747a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3747a-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3747a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3747a-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3747a-142">INPUTS</span></span>

### <span data-ttu-id="3747a-143">Nincs</span><span class="sxs-lookup"><span data-stu-id="3747a-143">None</span></span>
<span data-ttu-id="3747a-144">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3747a-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3747a-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3747a-145">OUTPUTS</span></span>

## <span data-ttu-id="3747a-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3747a-146">NOTES</span></span>

## <span data-ttu-id="3747a-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3747a-147">RELATED LINKS</span></span>

[<span data-ttu-id="3747a-148">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3747a-148">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3747a-149">Remove-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="3747a-149">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="3747a-150">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="3747a-150">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="3747a-151">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="3747a-151">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


