---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016166"
---
# <span data-ttu-id="af235-101">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="af235-101">Remove-AzureDataDisk</span></span>

## <span data-ttu-id="af235-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af235-102">SYNOPSIS</span></span>
<span data-ttu-id="af235-103">Egy Azure virtuális gépről származó adatlemez eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="af235-103">Removes a data disk from an Azure virtual machine.</span></span>

## <span data-ttu-id="af235-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af235-104">SYNTAX</span></span>

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="af235-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="af235-105">DESCRIPTION</span></span>
<span data-ttu-id="af235-106">A **Remove-AzureDataDisk** parancsmag eltávolítja az adatlemezt egy Azure Virtual Machine-webhelyről.</span><span class="sxs-lookup"><span data-stu-id="af235-106">The **Remove-AzureDataDisk** cmdlet removes a data disk from an Azure virtual machine.</span></span>
<span data-ttu-id="af235-107">Ez a parancsmag alapértelmezés szerint nem távolítja el az adatlemez blobját a tároló fiókból.</span><span class="sxs-lookup"><span data-stu-id="af235-107">By default, this cmdlet does not remove the data disk blob from the storage account.</span></span>

## <span data-ttu-id="af235-108">Példák</span><span class="sxs-lookup"><span data-stu-id="af235-108">EXAMPLES</span></span>

### <span data-ttu-id="af235-109">1. példa: adatlemez eltávolítása</span><span class="sxs-lookup"><span data-stu-id="af235-109">Example 1: Remove a data disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

<span data-ttu-id="af235-110">Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="af235-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="af235-111">A parancs a virtuális gépet az aktuális parancsmagba továbbítja a csővezeték-kezelő segítségével.</span><span class="sxs-lookup"><span data-stu-id="af235-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="af235-112">Az aktuális parancsmag eltávolítja azt az adatlemezt, amelynek a logikai egysége 0.</span><span class="sxs-lookup"><span data-stu-id="af235-112">The current cmdlet removes the data disk that has the LUN 0.</span></span>

### <span data-ttu-id="af235-113">2. példa: adatlemez és a virtuális merevlemez-fájl eltávolítása</span><span class="sxs-lookup"><span data-stu-id="af235-113">Example 2: Remove a data disk and the virtual hard disk file</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

<span data-ttu-id="af235-114">Ez a parancs a VirtualMachine07 nevű virtuális gépet a ContosoService nevű szolgáltatásban kapja meg.</span><span class="sxs-lookup"><span data-stu-id="af235-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="af235-115">A parancs átadja a virtuális gépet az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="af235-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="af235-116">Az aktuális parancsmag eltávolítja azt az adatlemezt, amelynek a logikai egysége 0.</span><span class="sxs-lookup"><span data-stu-id="af235-116">The current cmdlet removes the data disk that has the LUN 0.</span></span>
<span data-ttu-id="af235-117">A parancs a *DeleteVHD* paramétert tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="af235-117">The command includes the *DeleteVHD* parameter.</span></span>
<span data-ttu-id="af235-118">Emiatt a mögöttes virtuális merevlemez is törlődik.</span><span class="sxs-lookup"><span data-stu-id="af235-118">Therefore, it also deletes the underlying virtual hard disk.</span></span>
<span data-ttu-id="af235-119">A parancs frissíti a virtuális gépet a módosítások tükrözéséhez a **Update-AzureVM** parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="af235-119">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="af235-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af235-120">PARAMETERS</span></span>

### <span data-ttu-id="af235-121">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="af235-121">-DeleteVHD</span></span>
<span data-ttu-id="af235-122">Jelzi, hogy ez a parancsmag eltávolítja az adatlemezt és a virtuális merevlemezt (VHD) a blob-tárolóból.</span><span class="sxs-lookup"><span data-stu-id="af235-122">Indicates that this cmdlet removes the data disk and the virtual hard disk (VHD) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af235-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="af235-123">-InformationAction</span></span>
<span data-ttu-id="af235-124">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="af235-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="af235-125">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="af235-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="af235-126">Folytassa</span><span class="sxs-lookup"><span data-stu-id="af235-126">Continue</span></span>
- <span data-ttu-id="af235-127">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="af235-127">Ignore</span></span>
- <span data-ttu-id="af235-128">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="af235-128">Inquire</span></span>
- <span data-ttu-id="af235-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="af235-129">SilentlyContinue</span></span>
- <span data-ttu-id="af235-130">állj</span><span class="sxs-lookup"><span data-stu-id="af235-130">Stop</span></span>
- <span data-ttu-id="af235-131">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="af235-131">Suspend</span></span>

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

### <span data-ttu-id="af235-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="af235-132">-InformationVariable</span></span>
<span data-ttu-id="af235-133">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="af235-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="af235-134">-LUN</span><span class="sxs-lookup"><span data-stu-id="af235-134">-LUN</span></span>
<span data-ttu-id="af235-135">Annak a logikai egységnek a logikai egység számát adja meg, amely a virtuális gép adatmeghajtójának logikai egysége.</span><span class="sxs-lookup"><span data-stu-id="af235-135">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="af235-136">Az érvényes értékek a következők: 0 – 15.</span><span class="sxs-lookup"><span data-stu-id="af235-136">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af235-137">-Profil</span><span class="sxs-lookup"><span data-stu-id="af235-137">-Profile</span></span>
<span data-ttu-id="af235-138">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="af235-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="af235-139">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="af235-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="af235-140">-VM</span><span class="sxs-lookup"><span data-stu-id="af235-140">-VM</span></span>
<span data-ttu-id="af235-141">Az adatlemezhez kapcsolt virtuálisgép-objektumot adja meg.</span><span class="sxs-lookup"><span data-stu-id="af235-141">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="af235-142">Virtuális gép objektum beszerzéséhez használja a **Get-AzureVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="af235-142">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af235-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af235-143">CommonParameters</span></span>
<span data-ttu-id="af235-144">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af235-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af235-145">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af235-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af235-146">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af235-146">INPUTS</span></span>

## <span data-ttu-id="af235-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af235-147">OUTPUTS</span></span>

## <span data-ttu-id="af235-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af235-148">NOTES</span></span>

## <span data-ttu-id="af235-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af235-149">RELATED LINKS</span></span>

[<span data-ttu-id="af235-150">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="af235-150">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="af235-151">Get-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="af235-151">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="af235-152">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="af235-152">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="af235-153">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="af235-153">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="af235-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="af235-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


