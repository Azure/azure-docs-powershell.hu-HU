---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8DC10708-09CE-449C-BE20-1E9E49CCE08A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 55d9879d6e6768bf3ad409c84a4fc1052d58d8b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016013"
---
# <span data-ttu-id="418a4-101">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="418a4-101">Update-AzureVM</span></span>

## <span data-ttu-id="418a4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="418a4-102">SYNOPSIS</span></span>
<span data-ttu-id="418a4-103">Egy Azure virtuális gép konfigurációjának módosítása.</span><span class="sxs-lookup"><span data-stu-id="418a4-103">Modifies the configuration of an Azure virtual machine.</span></span>

## <span data-ttu-id="418a4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="418a4-104">SYNTAX</span></span>

```
Update-AzureVM [-Name] <String> -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="418a4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="418a4-105">DESCRIPTION</span></span>
<span data-ttu-id="418a4-106">Az **Update-AzureVM** parancsmag a megadott virtuális géphez tartozó frissítési információkat fogadja el, és elindítja a frissítést.</span><span class="sxs-lookup"><span data-stu-id="418a4-106">The **Update-AzureVM** cmdlet accepts update information for the specified virtual machine and initiates the update.</span></span>
<span data-ttu-id="418a4-107">Hozzáadhat vagy eltávolíthat adatlemezeket, módosíthatja az adatok vagy az operációs rendszer lemezek gyorsítótárát, módosíthatja a hálózati végpontokat, illetve módosíthatja a virtuális gép méretét.</span><span class="sxs-lookup"><span data-stu-id="418a4-107">You can add or remove data disks, modify the cache mode of data or operating system disks, change the network endpoints, or change the size of the virtual machine.</span></span>

## <span data-ttu-id="418a4-108">Példák</span><span class="sxs-lookup"><span data-stu-id="418a4-108">EXAMPLES</span></span>

### <span data-ttu-id="418a4-109">Példa 1: virtuális gép méretének frissítése</span><span class="sxs-lookup"><span data-stu-id="418a4-109">Example 1: Update the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" | Set-AzureVMSize -InstanceSize "Medium" | Update-AzureVM
```

<span data-ttu-id="418a4-110">Ez a parancs megváltoztatja a VirtualMachine04 nevű virtuális gép méretét, amely a ContosoService03 nevű szolgáltatásban fut, a közepes értékkel.</span><span class="sxs-lookup"><span data-stu-id="418a4-110">This command changes the size of the virtual machine named VirtualMachine04, running in the service named ContosoService03, to Medium.</span></span>

### <span data-ttu-id="418a4-111">2. példa: adatlemez hozzáadása virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="418a4-111">Example 2: Add a data disk to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine05" | Add-AzureDataDisk -CreateNew -MediaLocation "https://ContosoStore1.blob.core.azure.com/vhds/Disk22.vhd" -DiskSizeInGB 128 -DiskLabel "Data-128" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="418a4-112">Ez a parancs új adatlemezt ad a VirtualMachine05 nevű virtuális géphez, amelyen a ContosoService03 nevű szolgáltatás fut.</span><span class="sxs-lookup"><span data-stu-id="418a4-112">This command adds a new data disk to the virtual machine named VirtualMachine05, running in the service named ContosoService03.</span></span>

## <span data-ttu-id="418a4-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="418a4-113">PARAMETERS</span></span>

### <span data-ttu-id="418a4-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="418a4-114">-InformationAction</span></span>
<span data-ttu-id="418a4-115">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="418a4-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="418a4-116">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="418a4-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="418a4-117">Folytassa</span><span class="sxs-lookup"><span data-stu-id="418a4-117">Continue</span></span>
- <span data-ttu-id="418a4-118">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="418a4-118">Ignore</span></span>
- <span data-ttu-id="418a4-119">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="418a4-119">Inquire</span></span>
- <span data-ttu-id="418a4-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="418a4-120">SilentlyContinue</span></span>
- <span data-ttu-id="418a4-121">állj</span><span class="sxs-lookup"><span data-stu-id="418a4-121">Stop</span></span>
- <span data-ttu-id="418a4-122">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="418a4-122">Suspend</span></span>

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

### <span data-ttu-id="418a4-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="418a4-123">-InformationVariable</span></span>
<span data-ttu-id="418a4-124">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="418a4-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="418a4-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="418a4-125">-Name</span></span>
<span data-ttu-id="418a4-126">A frissítendő virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="418a4-126">Specifies the name of the virtual machine to update.</span></span>

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

### <span data-ttu-id="418a4-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="418a4-127">-Profile</span></span>
<span data-ttu-id="418a4-128">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="418a4-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="418a4-129">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="418a4-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="418a4-130">-Szolgáltatásnév</span><span class="sxs-lookup"><span data-stu-id="418a4-130">-ServiceName</span></span>
<span data-ttu-id="418a4-131">Az Azure-szolgáltatás nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="418a4-131">Specifies the name of the Azure service.</span></span>

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

### <span data-ttu-id="418a4-132">-VM</span><span class="sxs-lookup"><span data-stu-id="418a4-132">-VM</span></span>
<span data-ttu-id="418a4-133">Azt a virtuálisgép-objektumot adja meg, amely a frissített beállításokat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="418a4-133">Specifies the virtual machine object that includes updated settings.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="418a4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418a4-134">CommonParameters</span></span>
<span data-ttu-id="418a4-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="418a4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418a4-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="418a4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418a4-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="418a4-137">INPUTS</span></span>

## <span data-ttu-id="418a4-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="418a4-138">OUTPUTS</span></span>

## <span data-ttu-id="418a4-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="418a4-139">NOTES</span></span>

## <span data-ttu-id="418a4-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="418a4-140">RELATED LINKS</span></span>

[<span data-ttu-id="418a4-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="418a4-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="418a4-142">Új – AzureVM</span><span class="sxs-lookup"><span data-stu-id="418a4-142">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="418a4-143">Új – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="418a4-143">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="418a4-144">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="418a4-144">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="418a4-145">Újraindítás – AzureVM</span><span class="sxs-lookup"><span data-stu-id="418a4-145">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="418a4-146">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="418a4-146">Set-AzureVMSize</span></span>](./Set-AzureVMSize.md)

[<span data-ttu-id="418a4-147">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="418a4-147">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="418a4-148">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="418a4-148">Stop-AzureVM</span></span>](./Stop-AzureVM.md)


