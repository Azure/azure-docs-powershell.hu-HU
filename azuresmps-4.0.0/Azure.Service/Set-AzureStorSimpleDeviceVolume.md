---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 39E9BB88-6AD8-4B05-9498-35393E22BA30
online version: ''
schema: 2.0.0
ms.openlocfilehash: 234b1f7fa2719cc1b34e6bcd0b8e8fd340acc4af
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016418"
---
# <span data-ttu-id="5f730-101">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="5f730-101">Set-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="5f730-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5f730-102">SYNOPSIS</span></span>
<span data-ttu-id="5f730-103">Frissíti a meglévő kötetek tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="5f730-103">Updates the properties of an existing volume.</span></span>

## <span data-ttu-id="5f730-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5f730-104">SYNTAX</span></span>

### <span data-ttu-id="5f730-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="5f730-105">IdentifyByName</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5f730-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="5f730-106">IdentifyByObject</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5f730-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5f730-107">DESCRIPTION</span></span>
<span data-ttu-id="5f730-108">A **set-AzureStorSimpleDeviceVolume** parancsmag frissíti egy meglévő kötet tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="5f730-108">The **Set-AzureStorSimpleDeviceVolume** cmdlet updates the properties of an existing volume.</span></span>
<span data-ttu-id="5f730-109">Ez a parancsmag egy vagy több hozzáférés-vezérlési rekorddal rendelkező kötetet társít.</span><span class="sxs-lookup"><span data-stu-id="5f730-109">This cmdlet associates a volume with one or more access control records.</span></span>
<span data-ttu-id="5f730-110">Ha **AccessControlRecord** -objektumokat szeretne beolvasni, használja a **Get-AzureStorSimpleAccessControlRecord** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5f730-110">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="5f730-111">A kötet méretének vagy típusának frissítése</span><span class="sxs-lookup"><span data-stu-id="5f730-111">Update the size or type for the volume.</span></span>
<span data-ttu-id="5f730-112">Azt is megadhatja, hogy a kötetet online szeretné-e létrehozni.</span><span class="sxs-lookup"><span data-stu-id="5f730-112">Also, update whether to create the volume online.</span></span>

## <span data-ttu-id="5f730-113">Példák</span><span class="sxs-lookup"><span data-stu-id="5f730-113">EXAMPLES</span></span>

### <span data-ttu-id="5f730-114">Példa 1: a kötet online értékének frissítése</span><span class="sxs-lookup"><span data-stu-id="5f730-114">Example 1: Update online value for a volume</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $False
VERBOSE: ClientRequestId: f2869570-ea47-4be7-801e-9c0f22f2600d_PS
VERBOSE: ClientRequestId: c70bb86a-51d3-4390-be17-4d0847641dc3_PS
VERBOSE: ClientRequestId: d20cb5b2-6b3c-4e06-af99-cada28c5e50a_PS
VERBOSE: ClientRequestId: ab6d533e-b55b-4cfb-9c58-9153295e0547_PS
de7000f1-29c7-4102-a375-b52432f9e67e
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
de7000f1-29c7-4102-a375-b52432f9e67e for tracking the task's status
```

<span data-ttu-id="5f730-115">Ez a parancs frissíti a Volume18 nevű kötetet, és a $False online értékét tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="5f730-115">This command updates the volume named Volume18 to have an online value of $False.</span></span>
<span data-ttu-id="5f730-116">Ez a parancs elindítja a feladatot, majd egy **TaskResponse** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="5f730-116">This command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="5f730-117">A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5f730-117">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="5f730-118">2. példa: az online érték módosítása és beírása</span><span class="sxs-lookup"><span data-stu-id="5f730-118">Example 2: Modify online value and type</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $True -VolumeAppType ArchiveVolume 
VERBOSE: ClientRequestId: af42b02a-645e-4801-a2d7-4197511c68cf_PS
VERBOSE: ClientRequestId: 7cb4f3b4-548e-42dc-a38c-0df0911c5206_PS
VERBOSE: ClientRequestId: 7cc706ad-a58f-4939-8e78-cabae8379a51_PS
VERBOSE: ClientRequestId: 6bed21d5-12fc-4a12-a89c-120bdb5636b1_PS
aa977225-af78-4c93-b754-72704afc928f
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
aa977225-af78-4c93-b754-72704afc928f for tracking the task's status
```

<span data-ttu-id="5f730-119">Ez a parancs frissíti a Volume18 nevű kötetet.</span><span class="sxs-lookup"><span data-stu-id="5f730-119">This command updates the volume named Volume18.</span></span>
<span data-ttu-id="5f730-120">Módosította a típust, és módosítja az *online* paraméter értékét $Truera.</span><span class="sxs-lookup"><span data-stu-id="5f730-120">It modifies the type and changes the value of the *Online* parameter to $True.</span></span>

## <span data-ttu-id="5f730-121">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5f730-121">PARAMETERS</span></span>

### <span data-ttu-id="5f730-122">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="5f730-122">-AccessControlRecords</span></span>
<span data-ttu-id="5f730-123">A kötethez társítani kívánt hozzáférés-vezérlési rekordok listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f730-123">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f730-124">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5f730-124">-DeviceName</span></span>
<span data-ttu-id="5f730-125">Annak a StorSimple-eszköznek a nevét adja meg, amelyen a kötetet frissíteni szeretné.</span><span class="sxs-lookup"><span data-stu-id="5f730-125">Specifies the name of the StorSimple device on which to update the volume exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f730-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5f730-126">-InformationAction</span></span>
<span data-ttu-id="5f730-127">Itt adhatja meg, hogy a parancsmag hogyan válaszoljon egy információs eseményre.</span><span class="sxs-lookup"><span data-stu-id="5f730-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5f730-128">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="5f730-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f730-129">Folytassa</span><span class="sxs-lookup"><span data-stu-id="5f730-129">Continue</span></span>
- <span data-ttu-id="5f730-130">Mellőzése</span><span class="sxs-lookup"><span data-stu-id="5f730-130">Ignore</span></span>
- <span data-ttu-id="5f730-131">Érdeklődni</span><span class="sxs-lookup"><span data-stu-id="5f730-131">Inquire</span></span>
- <span data-ttu-id="5f730-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5f730-132">SilentlyContinue</span></span>
- <span data-ttu-id="5f730-133">állj</span><span class="sxs-lookup"><span data-stu-id="5f730-133">Stop</span></span>
- <span data-ttu-id="5f730-134">Felfüggesztheti</span><span class="sxs-lookup"><span data-stu-id="5f730-134">Suspend</span></span>

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

### <span data-ttu-id="5f730-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5f730-135">-InformationVariable</span></span>
<span data-ttu-id="5f730-136">Egy információs változót ad meg.</span><span class="sxs-lookup"><span data-stu-id="5f730-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5f730-137">-NewName</span><span class="sxs-lookup"><span data-stu-id="5f730-137">-NewName</span></span>
<span data-ttu-id="5f730-138">A StorSimple-eszköz új nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f730-138">Specifies a new name for the StorSimple device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f730-139">-Online</span><span class="sxs-lookup"><span data-stu-id="5f730-139">-Online</span></span>
<span data-ttu-id="5f730-140">Megadja, hogy a kötet online legyen-e.</span><span class="sxs-lookup"><span data-stu-id="5f730-140">Specifies whether the volume is online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f730-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="5f730-141">-Profile</span></span>
<span data-ttu-id="5f730-142">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="5f730-142">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="5f730-143">-Volume</span><span class="sxs-lookup"><span data-stu-id="5f730-143">-Volume</span></span>
<span data-ttu-id="5f730-144">A frissítendő kötet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f730-144">Specifies the name of the volume to update.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f730-145">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="5f730-145">-VolumeAppType</span></span>
<span data-ttu-id="5f730-146">Azt adja meg, hogy a kötetet elsődleges vagy archív kötetként szeretné-e frissíteni.</span><span class="sxs-lookup"><span data-stu-id="5f730-146">Specifies whether to update the volume to be a primary or archive volume.</span></span>
<span data-ttu-id="5f730-147">Az érvényes értékek a következők: PrimaryVolume és ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="5f730-147">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f730-148">-Kötetnév</span><span class="sxs-lookup"><span data-stu-id="5f730-148">-VolumeName</span></span>
<span data-ttu-id="5f730-149">A frissítendő kötet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f730-149">Specifies the name of the volume to update.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f730-150">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="5f730-150">-VolumeSizeInBytes</span></span>
<span data-ttu-id="5f730-151">A kötetben a frissített méretet adja meg bájtban.</span><span class="sxs-lookup"><span data-stu-id="5f730-151">Specifies the updated size, in bytes, for the volume.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f730-152">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="5f730-152">-WaitForComplete</span></span>
<span data-ttu-id="5f730-153">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="5f730-153">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f730-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f730-154">CommonParameters</span></span>
<span data-ttu-id="5f730-155">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5f730-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f730-156">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f730-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f730-157">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f730-157">INPUTS</span></span>

### <span data-ttu-id="5f730-158">Lista\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="5f730-158">List\<AccessControlRecord\></span></span>
<span data-ttu-id="5f730-159">Ez a parancsmag elfogadja a kötethez társítani kívánt **AccessControlRecord** -objektumok listáját.</span><span class="sxs-lookup"><span data-stu-id="5f730-159">This cmdlet accepts a list of **AccessControlRecord** objects to associate to a volume.</span></span>

## <span data-ttu-id="5f730-160">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5f730-160">OUTPUTS</span></span>

### <span data-ttu-id="5f730-161">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="5f730-161">TaskStatusInfo</span></span>
<span data-ttu-id="5f730-162">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="5f730-162">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="5f730-163">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5f730-163">NOTES</span></span>

## <span data-ttu-id="5f730-164">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5f730-164">RELATED LINKS</span></span>

[<span data-ttu-id="5f730-165">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="5f730-165">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="5f730-166">Új – AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="5f730-166">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="5f730-167">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="5f730-167">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="5f730-168">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="5f730-168">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="5f730-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="5f730-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


