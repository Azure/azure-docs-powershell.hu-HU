---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 455DB2C0-08A0-4D62-B8EE-7C3DB9AD8A8C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85040f07914aef02355f69baab093c75ce7e4afd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015516"
---
# <span data-ttu-id="06e8a-101">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="06e8a-101">Remove-AzureVM</span></span>

## <span data-ttu-id="06e8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="06e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="06e8a-103">Azure Virtual Machine eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="06e8a-103">Removes an Azure virtual machine.</span></span>

## <span data-ttu-id="06e8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="06e8a-104">SYNTAX</span></span>

```
Remove-AzureVM [-Name] <String> [-DeleteVHD] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06e8a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="06e8a-105">DESCRIPTION</span></span>
<span data-ttu-id="06e8a-106">A **Remove-AzureVM** parancsmag törli az Azure Virtual machinet.</span><span class="sxs-lookup"><span data-stu-id="06e8a-106">The **Remove-AzureVM** cmdlet deletes an Azure virtual machine.</span></span>
<span data-ttu-id="06e8a-107">Ez a folyamat nem törli a virtuális gépre csatlakoztatott lemezek mögöttes. vhd fájljait.</span><span class="sxs-lookup"><span data-stu-id="06e8a-107">This process does not delete the underlying .vhd files of the disks mounted on that virtual machine.</span></span>

## <span data-ttu-id="06e8a-108">Példák</span><span class="sxs-lookup"><span data-stu-id="06e8a-108">EXAMPLES</span></span>

### <span data-ttu-id="06e8a-109">Példa 1: virtuális gép eltávolítása egy szolgáltatásból</span><span class="sxs-lookup"><span data-stu-id="06e8a-109">Example 1: Remove a virtual machine from a service</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine03"
```

<span data-ttu-id="06e8a-110">Ez a parancs eltávolítja a ContosoService03 szolgáltatásban futó VirtualMachine03 nevű virtuális gépet.</span><span class="sxs-lookup"><span data-stu-id="06e8a-110">This command removes the virtual machine named VirtualMachine03 that runs in the ContosoService03 service.</span></span>

### <span data-ttu-id="06e8a-111">2. példa: virtuális gép eltávolítása és a. vhd fájlok törlése</span><span class="sxs-lookup"><span data-stu-id="06e8a-111">Example 2: Remove a virtual machine and delete the .vhd files</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" -DeleteVHD
```

<span data-ttu-id="06e8a-112">Ez a parancs eltávolítja a ContosoService03 szolgáltatásban futó VirtualMachine04 virtuális gépet, és azt adja meg, hogy a. vhd fájlokat a *DeleteVHD* paraméterrel távolítja el.</span><span class="sxs-lookup"><span data-stu-id="06e8a-112">This command removes the VirtualMachine04 virtual machine that runs in the ContosoService03 service, and specifies to remove the .vhd files using the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="06e8a-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="06e8a-113">PARAMETERS</span></span>

### <span data-ttu-id="06e8a-114">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="06e8a-114">-DeleteVHD</span></span>
<span data-ttu-id="06e8a-115">Azt adja meg, hogy a parancsmag eltávolítja-e a virtuális gépet és a mögöttes merevlemez-objektumokat.</span><span class="sxs-lookup"><span data-stu-id="06e8a-115">Specifies whether this cmdlet removes the virtual machine and the underlying disk blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e8a-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="06e8a-116">-InformationAction</span></span>
<span data-ttu-id="06e8a-117">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="06e8a-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="06e8a-118">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="06e8a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06e8a-119">Folytassa</span><span class="sxs-lookup"><span data-stu-id="06e8a-119">Continue</span></span>
- <span data-ttu-id="06e8a-120">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="06e8a-120">Ignore</span></span>
- <span data-ttu-id="06e8a-121">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="06e8a-121">Inquire</span></span>
- <span data-ttu-id="06e8a-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="06e8a-122">SilentlyContinue</span></span>
- <span data-ttu-id="06e8a-123">állj</span><span class="sxs-lookup"><span data-stu-id="06e8a-123">Stop</span></span>
- <span data-ttu-id="06e8a-124">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="06e8a-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e8a-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="06e8a-125">-InformationVariable</span></span>
<span data-ttu-id="06e8a-126">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="06e8a-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e8a-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="06e8a-127">-Name</span></span>
<span data-ttu-id="06e8a-128">Az eltávolítandó virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="06e8a-128">Specifies the name of the virtual machine being removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e8a-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="06e8a-129">-Profile</span></span>
<span data-ttu-id="06e8a-130">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="06e8a-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06e8a-131">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="06e8a-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e8a-132">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="06e8a-132">-ServiceName</span></span>
<span data-ttu-id="06e8a-133">Annak az Azure-szolgáltatásnak a neve, amelyből a virtuális gépet eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="06e8a-133">Specifies the name of the Azure service from which the virtual machine is being removed.</span></span>

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

### <span data-ttu-id="06e8a-134">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="06e8a-134">-Confirm</span></span>
<span data-ttu-id="06e8a-135">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="06e8a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e8a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e8a-136">-WhatIf</span></span>
<span data-ttu-id="06e8a-137">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="06e8a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06e8a-138">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="06e8a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e8a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e8a-139">CommonParameters</span></span>
<span data-ttu-id="06e8a-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="06e8a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e8a-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e8a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e8a-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="06e8a-142">INPUTS</span></span>

## <span data-ttu-id="06e8a-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="06e8a-143">OUTPUTS</span></span>

## <span data-ttu-id="06e8a-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="06e8a-144">NOTES</span></span>

## <span data-ttu-id="06e8a-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="06e8a-145">RELATED LINKS</span></span>

[<span data-ttu-id="06e8a-146">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="06e8a-146">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="06e8a-147">Új – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="06e8a-147">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="06e8a-148">Újraindítás – AzureVM</span><span class="sxs-lookup"><span data-stu-id="06e8a-148">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="06e8a-149">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="06e8a-149">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="06e8a-150">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="06e8a-150">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="06e8a-151">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="06e8a-151">Update-AzureVM</span></span>](./Update-AzureVM.md)


