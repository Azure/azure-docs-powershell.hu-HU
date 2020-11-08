---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015563"
---
# <span data-ttu-id="3b82b-101">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="3b82b-101">Get-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="3b82b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3b82b-102">SYNOPSIS</span></span>
<span data-ttu-id="3b82b-103">Mennyiségi tárolókat kap egy eszközön.</span><span class="sxs-lookup"><span data-stu-id="3b82b-103">Gets volume containers on a device.</span></span>

## <span data-ttu-id="3b82b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3b82b-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3b82b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3b82b-105">DESCRIPTION</span></span>
<span data-ttu-id="3b82b-106">A **Get-AzureStorSimpleDeviceVolumeContainer** parancsmag az eszközön lévő mennyiségi tárolók listáját, illetve a megadott nevű kötet-tárolót kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3b82b-106">The **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet gets a list of volume containers on a device, or volume container that has the specified name.</span></span>
<span data-ttu-id="3b82b-107">A visszaadott objektum a következő tulajdonságokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="3b82b-107">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="3b82b-108">**BandwidthRate**</span><span class="sxs-lookup"><span data-stu-id="3b82b-108">**BandwidthRate**</span></span>
- <span data-ttu-id="3b82b-109">**EncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="3b82b-109">**EncryptionKey**</span></span>
- <span data-ttu-id="3b82b-110">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="3b82b-110">**InstanceId**</span></span>
- <span data-ttu-id="3b82b-111">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="3b82b-111">**IsDefault**</span></span>
- <span data-ttu-id="3b82b-112">**IsEncryptionEnabled**</span><span class="sxs-lookup"><span data-stu-id="3b82b-112">**IsEncryptionEnabled**</span></span>
- <span data-ttu-id="3b82b-113">**név**</span><span class="sxs-lookup"><span data-stu-id="3b82b-113">**Name**</span></span>
- <span data-ttu-id="3b82b-114">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="3b82b-114">**OperationInProgress**</span></span>
- <span data-ttu-id="3b82b-115">**Tulajdonú**</span><span class="sxs-lookup"><span data-stu-id="3b82b-115">**Owned**</span></span>
- <span data-ttu-id="3b82b-116">**PrimaryStorageAccountCredential**</span><span class="sxs-lookup"><span data-stu-id="3b82b-116">**PrimaryStorageAccountCredential**</span></span>
- <span data-ttu-id="3b82b-117">**SecretsEncryptionThumbprint**</span><span class="sxs-lookup"><span data-stu-id="3b82b-117">**SecretsEncryptionThumbprint**</span></span>
- <span data-ttu-id="3b82b-118">**VolumeCount**</span><span class="sxs-lookup"><span data-stu-id="3b82b-118">**VolumeCount**</span></span>

## <span data-ttu-id="3b82b-119">Példák</span><span class="sxs-lookup"><span data-stu-id="3b82b-119">EXAMPLES</span></span>

### <span data-ttu-id="3b82b-120">1. példa: eszközön lévő összes tároló lekérése</span><span class="sxs-lookup"><span data-stu-id="3b82b-120">Example 1: Get all the containers on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

<span data-ttu-id="3b82b-121">Ez a parancs a 8600-Bravo 001 nevű eszközön található mennyiségi tárolók listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="3b82b-121">This command gets a list of the volume containers on the device named 8600-Bravo 001.</span></span>

### <span data-ttu-id="3b82b-122">2. példa: tároló beszerzése a neve alapján</span><span class="sxs-lookup"><span data-stu-id="3b82b-122">Example 2: Get a container by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

<span data-ttu-id="3b82b-123">Ez a parancs a Container08 nevű kötet tárolót kapja a Contoso63-AppVm nevű eszközön.</span><span class="sxs-lookup"><span data-stu-id="3b82b-123">This command gets the volume container named Container08 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="3b82b-124">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3b82b-124">PARAMETERS</span></span>

### <span data-ttu-id="3b82b-125">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3b82b-125">-DeviceName</span></span>
<span data-ttu-id="3b82b-126">Egy StorSimple-eszköz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b82b-126">Specifies the name of a StorSimple device.</span></span>
<span data-ttu-id="3b82b-127">Ez a parancsmag a mennyiségi tárolókat az eszközről kapja, amelyet a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="3b82b-127">This cmdlet gets volume containers from the device that this parameter specifies.</span></span>

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

### <span data-ttu-id="3b82b-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="3b82b-128">-Profile</span></span>
<span data-ttu-id="3b82b-129">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="3b82b-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="3b82b-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="3b82b-130">-VolumeContainerName</span></span>
<span data-ttu-id="3b82b-131">A beolvasott kötet tárolójának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b82b-131">Specifies the name of the volume container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b82b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b82b-132">CommonParameters</span></span>
<span data-ttu-id="3b82b-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3b82b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b82b-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b82b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b82b-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b82b-135">INPUTS</span></span>

### <span data-ttu-id="3b82b-136">Nincs</span><span class="sxs-lookup"><span data-stu-id="3b82b-136">None</span></span>

## <span data-ttu-id="3b82b-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3b82b-137">OUTPUTS</span></span>

### <span data-ttu-id="3b82b-138">DataContainer, IList\<DataContainer\></span><span class="sxs-lookup"><span data-stu-id="3b82b-138">DataContainer, IList\<DataContainer\></span></span>
<span data-ttu-id="3b82b-139">Ez a parancsmag **DataContainer** -objektumot ad eredményül, ha a *VolumeContainerName* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="3b82b-139">This cmdlet returns a **DataContainer** object, if you specify the *VolumeContainerName* parameter.</span></span>
<span data-ttu-id="3b82b-140">Ha nem adja meg ezt a paramétert, ez a parancsmag **egy \<DataContainer\> IList** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="3b82b-140">If you do not specify that parameter, this cmdlet returns an **IList\<DataContainer\>** object.</span></span>

## <span data-ttu-id="3b82b-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3b82b-141">NOTES</span></span>

## <span data-ttu-id="3b82b-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3b82b-142">RELATED LINKS</span></span>

[<span data-ttu-id="3b82b-143">Új – AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="3b82b-143">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="3b82b-144">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="3b82b-144">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


