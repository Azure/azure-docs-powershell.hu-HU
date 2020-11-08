---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015828"
---
# <span data-ttu-id="635ec-101">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="635ec-101">Set-AzureOSDisk</span></span>

## <span data-ttu-id="635ec-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="635ec-102">SYNOPSIS</span></span>
<span data-ttu-id="635ec-103">Egy Azure Virtual Machine állomás-gyorsítótári üzemmódjának módosítása.</span><span class="sxs-lookup"><span data-stu-id="635ec-103">Modifies the host cache mode of an Azure virtual machine.</span></span>

## <span data-ttu-id="635ec-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="635ec-104">SYNTAX</span></span>

### <span data-ttu-id="635ec-105">Átméretezés</span><span class="sxs-lookup"><span data-stu-id="635ec-105">NoResize</span></span>
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="635ec-106">Átméretezése</span><span class="sxs-lookup"><span data-stu-id="635ec-106">Resize</span></span>
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="635ec-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="635ec-107">DESCRIPTION</span></span>
<span data-ttu-id="635ec-108">A **set-AzureOSDisk** parancsmag az Azure Virtual Machine operációs rendszer lemezének állomás-gyorsítótári üzemmódját módosítja.</span><span class="sxs-lookup"><span data-stu-id="635ec-108">The **Set-AzureOSDisk** cmdlet modifies the host cache mode of the operating system disk of an Azure virtual machine.</span></span>
<span data-ttu-id="635ec-109">A támogatott állomás-gyorsítótári üzemmódok ReadOnly és ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="635ec-109">The supported host cache modes are ReadOnly and ReadWrite.</span></span>
<span data-ttu-id="635ec-110">Ha futtatja ezt a parancsmagot egy futó virtuális gépen, a virtuális gép újraindul.</span><span class="sxs-lookup"><span data-stu-id="635ec-110">If you run this cmdlet on a virtual machine that is running, that virtual machine restarts.</span></span>

## <span data-ttu-id="635ec-111">Példák</span><span class="sxs-lookup"><span data-stu-id="635ec-111">EXAMPLES</span></span>

### <span data-ttu-id="635ec-112">1. példa: az állomás-gyorsítótári mód beállítása ReadOnly értékre a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="635ec-112">Example 1: Set the host cache mode to ReadOnly by using the pipeline</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

<span data-ttu-id="635ec-113">Ez a parancs a **Get-AzureVM** parancsmag használatával kapja meg a VirtualMachine02 nevű virtuális gépet a ContosoService nevű szolgáltatásban.</span><span class="sxs-lookup"><span data-stu-id="635ec-113">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="635ec-114">A parancs a virtuális gépet az aktuális parancsmagba továbbítja a csővezeték-kezelő segítségével.</span><span class="sxs-lookup"><span data-stu-id="635ec-114">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="635ec-115">Az aktuális parancsmag a virtuális gép operációsrendszer-lemezének állomás-gyorsítótári üzemmódját a ReadOnly értékre állítja.</span><span class="sxs-lookup"><span data-stu-id="635ec-115">The current cmdlet sets the host cache mode of the operating system disk of that virtual machine to be ReadOnly.</span></span>

### <span data-ttu-id="635ec-116">2. példa: az állomás gyorsítótári módjának beállítása ReadWrite</span><span class="sxs-lookup"><span data-stu-id="635ec-116">Example 2: Set the host cache mode to ReadWrite</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

<span data-ttu-id="635ec-117">Az első parancs megkapja a VirtualMachine02 nevű virtuális gépet a ContosoService nevű szolgáltatásban, majd a változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="635ec-117">The first command gets the virtual machine named VirtualMachine02 in the service named ContosoService, and then stores it in the variable.</span></span>

<span data-ttu-id="635ec-118">A második parancs beállítja a ReadWrite a virtuális gép operációs rendszer lemezének állomás-gyorsítótári módját.</span><span class="sxs-lookup"><span data-stu-id="635ec-118">The second command sets the host cache mode of the operating system disk of that virtual machine to be ReadWrite.</span></span>

## <span data-ttu-id="635ec-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="635ec-119">PARAMETERS</span></span>

### <span data-ttu-id="635ec-120">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="635ec-120">-HostCaching</span></span>
<span data-ttu-id="635ec-121">Az operációs rendszer merevlemezének az állomás-gyorsítótár attribútumát adja meg.</span><span class="sxs-lookup"><span data-stu-id="635ec-121">Specifies the host cache attribute for the operating system disk.</span></span>
<span data-ttu-id="635ec-122">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="635ec-122">Valid values are:</span></span> 

- <span data-ttu-id="635ec-123">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="635ec-123">ReadOnly</span></span> 
- <span data-ttu-id="635ec-124">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="635ec-124">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635ec-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="635ec-125">-InformationAction</span></span>
<span data-ttu-id="635ec-126">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="635ec-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="635ec-127">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="635ec-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="635ec-128">Folytassa</span><span class="sxs-lookup"><span data-stu-id="635ec-128">Continue</span></span>
- <span data-ttu-id="635ec-129">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="635ec-129">Ignore</span></span>
- <span data-ttu-id="635ec-130">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="635ec-130">Inquire</span></span>
- <span data-ttu-id="635ec-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="635ec-131">SilentlyContinue</span></span>
- <span data-ttu-id="635ec-132">állj</span><span class="sxs-lookup"><span data-stu-id="635ec-132">Stop</span></span>
- <span data-ttu-id="635ec-133">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="635ec-133">Suspend</span></span>

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

### <span data-ttu-id="635ec-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="635ec-134">-InformationVariable</span></span>
<span data-ttu-id="635ec-135">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="635ec-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="635ec-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="635ec-136">-Profile</span></span>
<span data-ttu-id="635ec-137">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="635ec-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="635ec-138">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="635ec-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="635ec-139">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="635ec-139">-ResizedSizeInGB</span></span>
<span data-ttu-id="635ec-140">Új méretet ad meg az operációs rendszer merevlemezének gigabájtjában.</span><span class="sxs-lookup"><span data-stu-id="635ec-140">Specifies a new size, in gigabytes, for the operating system disk.</span></span>
<span data-ttu-id="635ec-141">A méretnek az aktuális méretnél nagyobbnak kell lennie.</span><span class="sxs-lookup"><span data-stu-id="635ec-141">The size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="635ec-142">-VM</span><span class="sxs-lookup"><span data-stu-id="635ec-142">-VM</span></span>
<span data-ttu-id="635ec-143">Azt a virtuális gépet adja meg, amelyre a parancsmag az operációs rendszer lemezét módosítja.</span><span class="sxs-lookup"><span data-stu-id="635ec-143">Specifies the virtual machine for which this cmdlet modifies the operating system disk.</span></span>
<span data-ttu-id="635ec-144">Virtuális gép objektum beszerzéséhez használja a **Get-AzureVM** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="635ec-144">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="635ec-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="635ec-145">CommonParameters</span></span>
<span data-ttu-id="635ec-146">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="635ec-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="635ec-147">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="635ec-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="635ec-148">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="635ec-148">INPUTS</span></span>

## <span data-ttu-id="635ec-149">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="635ec-149">OUTPUTS</span></span>

## <span data-ttu-id="635ec-150">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="635ec-150">NOTES</span></span>

## <span data-ttu-id="635ec-151">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="635ec-151">RELATED LINKS</span></span>

[<span data-ttu-id="635ec-152">Add-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="635ec-152">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="635ec-153">Get-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="635ec-153">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)

[<span data-ttu-id="635ec-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="635ec-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="635ec-155">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="635ec-155">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="635ec-156">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="635ec-156">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="635ec-157">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="635ec-157">Update-AzureVM</span></span>](./Update-AzureVM.md)


