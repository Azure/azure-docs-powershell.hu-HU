---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015566"
---
# <span data-ttu-id="20cac-101">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="20cac-101">Get-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="20cac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20cac-102">SYNOPSIS</span></span>
<span data-ttu-id="20cac-103">Kötetet kap egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="20cac-103">Gets volumes on a device.</span></span>

## <span data-ttu-id="20cac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20cac-104">SYNTAX</span></span>

### <span data-ttu-id="20cac-105">IdentifyByParentObject</span><span class="sxs-lookup"><span data-stu-id="20cac-105">IdentifyByParentObject</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="20cac-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="20cac-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="20cac-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="20cac-107">DESCRIPTION</span></span>
<span data-ttu-id="20cac-108">A **Get-AzureStorSimpleDeviceVolume** parancsmag egy adott mennyiségi tároló vagy a megadott nevű kötet köteteinek listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="20cac-108">The **Get-AzureStorSimpleDeviceVolume** cmdlet gets a list of volumes for a specified volume container, or volume that has the specified name.</span></span>
<span data-ttu-id="20cac-109">A visszaadott objektum a következő tulajdonságokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="20cac-109">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="20cac-110">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="20cac-110">**AccessType**</span></span>
- <span data-ttu-id="20cac-111">**AcrList**</span><span class="sxs-lookup"><span data-stu-id="20cac-111">**AcrList**</span></span>
- <span data-ttu-id="20cac-112">**AppType**</span><span class="sxs-lookup"><span data-stu-id="20cac-112">**AppType**</span></span>
- <span data-ttu-id="20cac-113">**DataContainer**</span><span class="sxs-lookup"><span data-stu-id="20cac-113">**DataContainer**</span></span>
- <span data-ttu-id="20cac-114">**DataContainerId**</span><span class="sxs-lookup"><span data-stu-id="20cac-114">**DataContainerId**</span></span>
- <span data-ttu-id="20cac-115">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="20cac-115">**InstanceId**</span></span>
- <span data-ttu-id="20cac-116">**IsBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="20cac-116">**IsBackupEnabled**</span></span>
- <span data-ttu-id="20cac-117">**IsDefaultBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="20cac-117">**IsDefaultBackupEnabled**</span></span>
- <span data-ttu-id="20cac-118">**IsMonitoringEnabled**</span><span class="sxs-lookup"><span data-stu-id="20cac-118">**IsMonitoringEnabled**</span></span>
- <span data-ttu-id="20cac-119">**név**</span><span class="sxs-lookup"><span data-stu-id="20cac-119">**Name**</span></span>
- <span data-ttu-id="20cac-120">**Online**</span><span class="sxs-lookup"><span data-stu-id="20cac-120">**Online**</span></span>
- <span data-ttu-id="20cac-121">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="20cac-121">**OperationInProgress**</span></span>
- <span data-ttu-id="20cac-122">**SizeInBytes**</span><span class="sxs-lookup"><span data-stu-id="20cac-122">**SizeInBytes**</span></span>
- <span data-ttu-id="20cac-123">**VSN**</span><span class="sxs-lookup"><span data-stu-id="20cac-123">**VSN**</span></span>

## <span data-ttu-id="20cac-124">Példák</span><span class="sxs-lookup"><span data-stu-id="20cac-124">EXAMPLES</span></span>

### <span data-ttu-id="20cac-125">Példa 1: a megadott tárolóban lévő kötetek beolvasása</span><span class="sxs-lookup"><span data-stu-id="20cac-125">Example 1: Get volumes in a specified container</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

<span data-ttu-id="20cac-126">Ez a parancs a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmag segítségével a Container03 nevű kötet tárolóját kapja a Contoso63-AppVm nevű eszközön.</span><span class="sxs-lookup"><span data-stu-id="20cac-126">This command gets the volume container named Container03 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="20cac-127">A parancs a pipeline operátor segítségével átadja az adott tárolót az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="20cac-127">The command uses the pipeline operator to pass that container to the current cmdlet.</span></span>
<span data-ttu-id="20cac-128">A parancsmag a Contoso63-AppVm nevű eszközhöz a tárolóban található összes kötetet megkapja.</span><span class="sxs-lookup"><span data-stu-id="20cac-128">That cmdlet gets all the volumes in that container for the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="20cac-129">2. példa: kötet beszerzése a neve alapján</span><span class="sxs-lookup"><span data-stu-id="20cac-129">Example 2: Get a volume by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

<span data-ttu-id="20cac-130">Ez a parancs a Volume18 nevű kötetet a Contoso63-AppVm nevű eszközön kapja.</span><span class="sxs-lookup"><span data-stu-id="20cac-130">This command gets the volume named Volume18 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="20cac-131">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20cac-131">PARAMETERS</span></span>

### <span data-ttu-id="20cac-132">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="20cac-132">-DeviceName</span></span>
<span data-ttu-id="20cac-133">Annak a StorSimple-eszköznek a nevét adja meg, amelyből a köteteket be szeretné szerezni.</span><span class="sxs-lookup"><span data-stu-id="20cac-133">Specifies the name of the StorSimple device from which to get volumes.</span></span>

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

### <span data-ttu-id="20cac-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="20cac-134">-Profile</span></span>
<span data-ttu-id="20cac-135">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="20cac-135">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="20cac-136">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="20cac-136">-VolumeContainer</span></span>
<span data-ttu-id="20cac-137">Itt adhatja meg a **DataContainer** -objektumhoz tartozó kötet tárolóját, amely tartalmazza a beolvasott mennyiségeket.</span><span class="sxs-lookup"><span data-stu-id="20cac-137">Specifies the volume container, as a **DataContainer** object, that includes the volumes to get.</span></span>
<span data-ttu-id="20cac-138">**DataContainer** beszerzéséhez használja a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="20cac-138">To obtain a **DataContainer** , use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20cac-139">-Kötetnév</span><span class="sxs-lookup"><span data-stu-id="20cac-139">-VolumeName</span></span>
<span data-ttu-id="20cac-140">A beolvasott kötet nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="20cac-140">Specifies the name of the volume to get.</span></span>

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

### <span data-ttu-id="20cac-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20cac-141">CommonParameters</span></span>
<span data-ttu-id="20cac-142">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20cac-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20cac-143">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20cac-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20cac-144">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20cac-144">INPUTS</span></span>

### <span data-ttu-id="20cac-145">DataContainer</span><span class="sxs-lookup"><span data-stu-id="20cac-145">DataContainer</span></span>
<span data-ttu-id="20cac-146">Ez a parancsmag a beolvasott kötetet tartalmazó **DataContainer** -objektumot fogadja el.</span><span class="sxs-lookup"><span data-stu-id="20cac-146">This cmdlet accepts a **DataContainer** object that contains the volume to get.</span></span>

## <span data-ttu-id="20cac-147">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20cac-147">OUTPUTS</span></span>

### <span data-ttu-id="20cac-148">VirtualDisk, IList\<VirtualDisk\></span><span class="sxs-lookup"><span data-stu-id="20cac-148">VirtualDisk, IList\<VirtualDisk\></span></span>
<span data-ttu-id="20cac-149">Ez a parancsmag **VirtualDisk** -objektumot ad eredményül, ha a *kötetnév* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="20cac-149">This cmdlet returns a **VirtualDisk** object if you specify the *VolumeName* parameter.</span></span>
<span data-ttu-id="20cac-150">Ha megadja a *VolumeContainer* , ez a parancsmag egy **IList \<VirtualDisk\>** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="20cac-150">If you specify the *VolumeContainer* , this cmdlet returns an **IList\<VirtualDisk\>** object.</span></span>

## <span data-ttu-id="20cac-151">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20cac-151">NOTES</span></span>

## <span data-ttu-id="20cac-152">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20cac-152">RELATED LINKS</span></span>

[<span data-ttu-id="20cac-153">Új – AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="20cac-153">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="20cac-154">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="20cac-154">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="20cac-155">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="20cac-155">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="20cac-156">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="20cac-156">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


