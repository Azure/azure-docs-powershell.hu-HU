---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016291"
---
# <span data-ttu-id="fade9-101">Get-AzureStorSimpleDeviceConnectedInitiator</span><span class="sxs-lookup"><span data-stu-id="fade9-101">Get-AzureStorSimpleDeviceConnectedInitiator</span></span>

## <span data-ttu-id="fade9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fade9-102">SYNOPSIS</span></span>
<span data-ttu-id="fade9-103">Elérhetővé válik az iSCSI-kapcsolatok StorSimple-eszközön.</span><span class="sxs-lookup"><span data-stu-id="fade9-103">Gets the iSCSI connections available for a StorSimple device.</span></span>

## <span data-ttu-id="fade9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fade9-104">SYNTAX</span></span>

### <span data-ttu-id="fade9-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="fade9-105">IdentifyById</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fade9-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="fade9-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="fade9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="fade9-107">DESCRIPTION</span></span>
<span data-ttu-id="fade9-108">A **Get-AzureStorSimpleDeviceConnectedInitiator** parancsmag a StorSimple-eszközökhöz elérhető iSCSI-kapcsolatok listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="fade9-108">The **Get-AzureStorSimpleDeviceConnectedInitiator** cmdlet gets a list of the iSCSI connections available for a StorSimple device.</span></span>
<span data-ttu-id="fade9-109">A parancsmag által visszaadott iSCSI-kapcsolati objektumok a következő tulajdonságokat tartalmazzák:</span><span class="sxs-lookup"><span data-stu-id="fade9-109">The iSCSI connection objects that this cmdlet returns contain the following properties:</span></span>

- <span data-ttu-id="fade9-110">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="fade9-110">**AcrInstanceId**</span></span>
- <span data-ttu-id="fade9-111">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="fade9-111">**AcrName**</span></span>
- <span data-ttu-id="fade9-112">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="fade9-112">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="fade9-113">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="fade9-113">**InitiatorAddress**</span></span>
- <span data-ttu-id="fade9-114">**Felületek**</span><span class="sxs-lookup"><span data-stu-id="fade9-114">**Interfaces**</span></span>
- <span data-ttu-id="fade9-115">**IQN**</span><span class="sxs-lookup"><span data-stu-id="fade9-115">**Iqn**</span></span>
- <span data-ttu-id="fade9-116">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="fade9-116">**IscsiConnectionId**</span></span>

<span data-ttu-id="fade9-117">Ez a parancsmag csak akkor kapja meg a kapcsolat objektumot, ha az eszközön be van kapcsolva az iSCSI-kapcsolatok.</span><span class="sxs-lookup"><span data-stu-id="fade9-117">This cmdlet gets connection object only if iSCSI connections are turned on for the device.</span></span>
<span data-ttu-id="fade9-118">A kapcsolatok alapértelmezés szerint ki vannak kapcsolva.</span><span class="sxs-lookup"><span data-stu-id="fade9-118">By default, connections are turned off.</span></span>

## <span data-ttu-id="fade9-119">Példák</span><span class="sxs-lookup"><span data-stu-id="fade9-119">EXAMPLES</span></span>

### <span data-ttu-id="fade9-120">Példa 1: egy eszköz minden kapcsolatának lekérése</span><span class="sxs-lookup"><span data-stu-id="fade9-120">Example 1: Get all connections for a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

<span data-ttu-id="fade9-121">Ez a parancs a Contoso63-AppVm nevű eszköz minden iSCSI-kapcsolatát bekapja.</span><span class="sxs-lookup"><span data-stu-id="fade9-121">This command gets all iSCSI connections for the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="fade9-122">Ez a parancs csak akkor ad visszaadott kapcsolatokat, ha a kapcsolat be van kapcsolva az eszközön.</span><span class="sxs-lookup"><span data-stu-id="fade9-122">This command returns connections only if connections are turned on for the device.</span></span>

## <span data-ttu-id="fade9-123">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fade9-123">PARAMETERS</span></span>

### <span data-ttu-id="fade9-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fade9-124">-DeviceId</span></span>
<span data-ttu-id="fade9-125">Annak az StorSimple-eszköznek a példány-AZONOSÍTÓját adja meg, amelyből az iSCSI-kezdeményezőket be szeretné szerezni.</span><span class="sxs-lookup"><span data-stu-id="fade9-125">Specifies the instance ID of the StorSimple device from which to get iSCSI initiators.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fade9-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fade9-126">-DeviceName</span></span>
<span data-ttu-id="fade9-127">Annak a StorSimple-eszköznek a neve, amelyből az iSCSI-kezdeményezőket be kell szerezni.</span><span class="sxs-lookup"><span data-stu-id="fade9-127">Specifies the name of the StorSimple device from which to get iSCSI initiators.</span></span>

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

### <span data-ttu-id="fade9-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="fade9-128">-Profile</span></span>
<span data-ttu-id="fade9-129">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="fade9-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="fade9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fade9-130">CommonParameters</span></span>
<span data-ttu-id="fade9-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fade9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fade9-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fade9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fade9-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fade9-133">INPUTS</span></span>

### <span data-ttu-id="fade9-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="fade9-134">None</span></span>

## <span data-ttu-id="fade9-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fade9-135">OUTPUTS</span></span>

### <span data-ttu-id="fade9-136">Lista\<IscsiConnection\></span><span class="sxs-lookup"><span data-stu-id="fade9-136">List\<IscsiConnection\></span></span>
<span data-ttu-id="fade9-137">Ez a parancsmag egy olyan iSCSI-kapcsolati objektumot ad eredményül, amely a következő tulajdonságokat tartalmazza:</span><span class="sxs-lookup"><span data-stu-id="fade9-137">This cmdlet returns an iSCSI connection object that contains the following properties:</span></span> 

- <span data-ttu-id="fade9-138">**AcrInstanceId**</span><span class="sxs-lookup"><span data-stu-id="fade9-138">**AcrInstanceId**</span></span>
- <span data-ttu-id="fade9-139">**AcrName**</span><span class="sxs-lookup"><span data-stu-id="fade9-139">**AcrName**</span></span>
- <span data-ttu-id="fade9-140">**AllowedVolumeNames**</span><span class="sxs-lookup"><span data-stu-id="fade9-140">**AllowedVolumeNames**</span></span>
- <span data-ttu-id="fade9-141">**InitiatorAddress**</span><span class="sxs-lookup"><span data-stu-id="fade9-141">**InitiatorAddress**</span></span>
- <span data-ttu-id="fade9-142">**Felületek**</span><span class="sxs-lookup"><span data-stu-id="fade9-142">**Interfaces**</span></span>
- <span data-ttu-id="fade9-143">**IQN**</span><span class="sxs-lookup"><span data-stu-id="fade9-143">**Iqn**</span></span>
- <span data-ttu-id="fade9-144">**IscsiConnectionId**</span><span class="sxs-lookup"><span data-stu-id="fade9-144">**IscsiConnectionId**</span></span>

## <span data-ttu-id="fade9-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fade9-145">NOTES</span></span>

## <span data-ttu-id="fade9-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fade9-146">RELATED LINKS</span></span>

[<span data-ttu-id="fade9-147">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="fade9-147">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)


