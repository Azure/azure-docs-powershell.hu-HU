---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C5A2A8D2-A840-4712-A8BD-F49C6063D193
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1156b4887e7b97d4e783ec738a939d320fe397a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016292"
---
# <span data-ttu-id="d25c0-101">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="d25c0-101">Get-AzureStorSimpleDevice</span></span>

## <span data-ttu-id="d25c0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d25c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d25c0-103">Az erőforráshoz kapcsolt eszközök beolvasása</span><span class="sxs-lookup"><span data-stu-id="d25c0-103">Gets devices attached to the resource.</span></span>

## <span data-ttu-id="d25c0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d25c0-104">SYNTAX</span></span>

### <span data-ttu-id="d25c0-105">Üres (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d25c0-105">Empty (Default)</span></span>
```
Get-AzureStorSimpleDevice [-Type <String>] [-ModelID <String>] [-Detailed] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d25c0-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="d25c0-106">IdentifyById</span></span>
```
Get-AzureStorSimpleDevice [-DeviceId <String>] [-Type <String>] [-ModelID <String>] [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d25c0-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="d25c0-107">IdentifyByName</span></span>
```
Get-AzureStorSimpleDevice [-DeviceName <String>] [-Type <String>] [-ModelID <String>] [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d25c0-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="d25c0-108">DESCRIPTION</span></span>
<span data-ttu-id="d25c0-109">A **Get-AzureStorSimpleDevice** parancsmag az erőforráshoz kapcsolt StorSimple-eszközök listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="d25c0-109">The **Get-AzureStorSimpleDevice** cmdlet gets a list of StorSimple devices attached to the resource.</span></span>
<span data-ttu-id="d25c0-110">Megadhatja az eszköz AZONOSÍTÓját, nevét, modell-AZONOSÍTÓját és típusát.</span><span class="sxs-lookup"><span data-stu-id="d25c0-110">You can specify device ID, name, model ID, and type.</span></span>
<span data-ttu-id="d25c0-111">Használja az ezzel a parancsmaggal kapott **DeviceID** tulajdonságot az egyéb StorSimple-parancsmagok eszközeinek megadásához.</span><span class="sxs-lookup"><span data-stu-id="d25c0-111">Use the **DeviceID** property obtained by using this cmdlet to specify devices for other StorSimple cmdlets.</span></span>

## <span data-ttu-id="d25c0-112">Példák</span><span class="sxs-lookup"><span data-stu-id="d25c0-112">EXAMPLES</span></span>

### <span data-ttu-id="d25c0-113">Példa 1: elérhető eszközök beszerzése egy erőforráson</span><span class="sxs-lookup"><span data-stu-id="d25c0-113">Example 1: Get available devices on a resource</span></span>
```
PS C:\>Get-AzureStorSimpleDevice
DeviceId                  : 6f9ab151-39c7-4ded-b7d0-f5b0968f2766
DeviceName                : 8600-: SHX0881018G88
SerialNumber              : SHX0881018G88
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Offline
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx0991018g00e4-target
TimeZone                  : Pacific Standard Time
ActivationTime            : 2015-04-07T16:32:30.2960842Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 12693995520

DeviceId                  : eb30ea31-c856-4cf2-9a02-aee611d6a3b9
DeviceName                : 8100-Delta 001
SerialNumber              : SHX90391XXXXXXX
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8100
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8100-shx90193xxxxxxx-target
TimeZone                  : Eastern Standard Time
ActivationTime            : 2015-03-26T14:53:14.4219391Z
AvailableStorageInBytes   : 205509890146304
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 219902325555200
UsingStorageInBytes       : 23904321536

DeviceId                  : edcb0b9b-1ed5-4102-9c5d-c589f7632994
DeviceName                : 8600-Bravo 001
SerialNumber              : SHX0900915G44SY
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx0900915g44sy-target
TimeZone                  : Eastern Standard Time
ActivationTime            : 2015-03-26T15:36:26.0870525Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 978893799424
```

<span data-ttu-id="d25c0-114">Ez a parancs minden elérhető eszközt beolvas egy erőforrásra.</span><span class="sxs-lookup"><span data-stu-id="d25c0-114">This command gets all available devices on a resource.</span></span>
<span data-ttu-id="d25c0-115">Ebben a példában csak egy eszköz áll rendelkezésre.</span><span class="sxs-lookup"><span data-stu-id="d25c0-115">In this example, only one device is available.</span></span>

### <span data-ttu-id="d25c0-116">2. példa: meghatározott elérhető eszközök beszerzése egy erőforrásra</span><span class="sxs-lookup"><span data-stu-id="d25c0-116">Example 2: Get specific available devices on a resource</span></span>
```
PS C:\>Get-AzureStorSimpleDevice -DeviceName "8600-SHX90193XXXXXXX" -Type Appliance -ModelId "8600"
DeviceId                  : f9db31da-8a6c-4718-8f5b-5ce89e600f28
DeviceName                : 8600-SHX90193XXXXXXX
SerialNumber              : SHX90193XXXXXXX
DeviceSoftwareVersion     : 6.3.9600.17430
Location                  : 
ModelDescription          : 8600
Status                    : Online
Type                      : Appliance
TargetIQN                 : iqn.1991-05.com.microsoft:storsimple8600-shx90193xxxxxxx-target
TimeZone                  : Pacific Standard Time
ActivationTime            : 2015-04-07T18:10:46.4524766Z
AvailableStorageInBytes   : 535363378479104
ProvisionedStorageInBytes : 14392435408896
TotalStorageInBytes       : 549755813888000
UsingStorageInBytes       : 14445182976
```

<span data-ttu-id="d25c0-117">Ez a parancs a megadott név, típus és modell AZONOSÍTÓval rendelkező erőforrás minden elérhető eszközét bekapja.</span><span class="sxs-lookup"><span data-stu-id="d25c0-117">This command gets all available devices on a resource that have the specified name, type, and model ID.</span></span>

### <span data-ttu-id="d25c0-118">3. példa: az eszközök részleteinek beszerzése</span><span class="sxs-lookup"><span data-stu-id="d25c0-118">Example 3: Get details for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDevice -Name "8600-SHX90193XXXXXXX" -Type Appliance -Detailed
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : f9db31da-8a6c-4718-8f5b-5ce89e600f28
Name                           : 
NetInterfaceList               : {Data0, Data1, Data2, Data3...} 
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings

RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : Appliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings
```

<span data-ttu-id="d25c0-119">Ez a parancs a megadott névvel rendelkező erőforrás minden elérhető eszközét bekapja.</span><span class="sxs-lookup"><span data-stu-id="d25c0-119">This command gets all available devices on a resource that have the specified name and type.</span></span>
<span data-ttu-id="d25c0-120">Ez a parancs a *részletes* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="d25c0-120">This command specifies the *Detailed* parameter.</span></span>
<span data-ttu-id="d25c0-121">A parancs további részleteket tartalmaz az eredményül adott eszközökről.</span><span class="sxs-lookup"><span data-stu-id="d25c0-121">The command provides additional details about the devices it returns.</span></span>

## <span data-ttu-id="d25c0-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d25c0-122">PARAMETERS</span></span>

### <span data-ttu-id="d25c0-123">– Részletes</span><span class="sxs-lookup"><span data-stu-id="d25c0-123">-Detailed</span></span>
<span data-ttu-id="d25c0-124">Azt jelzi, hogy ez a parancsmag a kapott eszközökhöz tartozó eszközök adatait adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="d25c0-124">Indicates that this cmdlet returns device details for the devices that it gets.</span></span>

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

### <span data-ttu-id="d25c0-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d25c0-125">-DeviceId</span></span>
<span data-ttu-id="d25c0-126">A beszerzéshez használt eszköz példány-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d25c0-126">Specifies the instance ID of the device to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25c0-127">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d25c0-127">-DeviceName</span></span>
<span data-ttu-id="d25c0-128">A beszerzéshez használt StorSimple-eszköz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d25c0-128">Specifies the name of the StorSimple device to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25c0-129">-ModelID</span><span class="sxs-lookup"><span data-stu-id="d25c0-129">-ModelID</span></span>
<span data-ttu-id="d25c0-130">A beolvasott StorSimple-eszközök modelljének AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d25c0-130">Specifies the ID of the model of StorSimple devices to get.</span></span>

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

### <span data-ttu-id="d25c0-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="d25c0-131">-Profile</span></span>
<span data-ttu-id="d25c0-132">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="d25c0-132">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="d25c0-133">-Type (típus)</span><span class="sxs-lookup"><span data-stu-id="d25c0-133">-Type</span></span>
<span data-ttu-id="d25c0-134">Egy StorSimple-eszköz típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d25c0-134">Specifies the type of a StorSimple device.</span></span>
<span data-ttu-id="d25c0-135">Érvényes értékek: készülék-és VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="d25c0-135">Valid values are: Appliance and VirtualAppliance.</span></span>

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

### <span data-ttu-id="d25c0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25c0-136">CommonParameters</span></span>
<span data-ttu-id="d25c0-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d25c0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25c0-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d25c0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25c0-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d25c0-139">INPUTS</span></span>

### <span data-ttu-id="d25c0-140">Nincs</span><span class="sxs-lookup"><span data-stu-id="d25c0-140">None</span></span>

## <span data-ttu-id="d25c0-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d25c0-141">OUTPUTS</span></span>

### <span data-ttu-id="d25c0-142">Lista \<DeviceDetails\> , IEnumerable\<DeviceInfo\></span><span class="sxs-lookup"><span data-stu-id="d25c0-142">List\<DeviceDetails\>, IEnumerable\<DeviceInfo\></span></span>
<span data-ttu-id="d25c0-143">Ez a parancsmag a **lista \<DeviceDetails\>** objektumát adja eredményül, ha a *részletes* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="d25c0-143">This cmdlet returns a **List\<DeviceDetails\>** object, if you specify the *Detailed* parameter.</span></span>
<span data-ttu-id="d25c0-144">Ha nem adja meg ezt a paramétert, az eredmény **egy \<DeviceInfo\> IEnumerable** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d25c0-144">If you do not specify that parameter, it returns an **IEnumerable\<DeviceInfo\>** object.</span></span>

## <span data-ttu-id="d25c0-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d25c0-145">NOTES</span></span>

## <span data-ttu-id="d25c0-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d25c0-146">RELATED LINKS</span></span>

[<span data-ttu-id="d25c0-147">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="d25c0-147">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="d25c0-148">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="d25c0-148">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)


