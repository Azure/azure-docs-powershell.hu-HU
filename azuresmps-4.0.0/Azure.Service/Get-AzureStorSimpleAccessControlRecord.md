---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016552"
---
# <span data-ttu-id="e7c3b-101">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="e7c3b-101">Get-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="e7c3b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e7c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c3b-103">A szolgáltatás-konfigurációban hozzáférés-vezérlési rekordokat kap.</span><span class="sxs-lookup"><span data-stu-id="e7c3b-103">Gets access control records in a service configuration.</span></span>

## <span data-ttu-id="e7c3b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e7c3b-104">SYNTAX</span></span>

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e7c3b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e7c3b-105">DESCRIPTION</span></span>
<span data-ttu-id="e7c3b-106">A **Get-AzureStorSimpleAccessControlRecord** parancsmag hozzáférés-vezérlési rekordokat kap a StorSimple-kezelő szolgáltatás konfigurációjában.</span><span class="sxs-lookup"><span data-stu-id="e7c3b-106">The **Get-AzureStorSimpleAccessControlRecord** cmdlet gets access control records in the StorSimple Manager service configuration.</span></span>
<span data-ttu-id="e7c3b-107">Ez a parancsmag minden rekordot vagy névvel ellátott rekordot kap.</span><span class="sxs-lookup"><span data-stu-id="e7c3b-107">This cmdlet gets all records or a named record.</span></span>

<span data-ttu-id="e7c3b-108">A hozzáférés-vezérlési rekordok az iSCSI-kezdeményező paramétereinek tárolói.</span><span class="sxs-lookup"><span data-stu-id="e7c3b-108">Access control records are containers of iSCSI initiator parameters.</span></span>
<span data-ttu-id="e7c3b-109">Ezek a paraméterek azt adják meg, hogy mely kezdeményezők érhetik el a kötetet.</span><span class="sxs-lookup"><span data-stu-id="e7c3b-109">These parameters specify which initiators can access a volume.</span></span>
<span data-ttu-id="e7c3b-110">Ha egy iSCSI-kezdeményező megkísérel kapcsolódni egy kötethez, a készülék ellenőrzi a kötethez rendelt hozzáférés-vezérlési rekordokat.</span><span class="sxs-lookup"><span data-stu-id="e7c3b-110">When an iSCSI initiator attempts to connect to a volume, your appliance checks the access control records assigned to that volume.</span></span>
<span data-ttu-id="e7c3b-111">Ha az iSCSI-kezdeményező paraméterei megegyeznek az adott kötethez rendelt Access-vezérlők rekordjainak egyikével, az iSCSI-kezdeményező csatlakozni tud.</span><span class="sxs-lookup"><span data-stu-id="e7c3b-111">If the iSCSI initiator parameters match one of the entries in an access control record mapped to that volume, the iSCSI initiator can connect.</span></span>

## <span data-ttu-id="e7c3b-112">Példák</span><span class="sxs-lookup"><span data-stu-id="e7c3b-112">EXAMPLES</span></span>

### <span data-ttu-id="e7c3b-113">Példa 1: a hozzáférés-vezérlési rekordok beszerzése</span><span class="sxs-lookup"><span data-stu-id="e7c3b-113">Example 1: Get all access control records</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

<span data-ttu-id="e7c3b-114">Ez a parancs a hozzáférés-vezérlési rekordokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e7c3b-114">This command gets all access control records.</span></span>

### <span data-ttu-id="e7c3b-115">2. példa: speciális hozzáférés-szabályozási rekord beszerzése</span><span class="sxs-lookup"><span data-stu-id="e7c3b-115">Example 2: Get a specific access control record</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

<span data-ttu-id="e7c3b-116">Ez a parancs a Acr11 nevű hozzáférés-vezérlési rekordot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e7c3b-116">This command gets the access control record named Acr11.</span></span>

## <span data-ttu-id="e7c3b-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e7c3b-117">PARAMETERS</span></span>

### <span data-ttu-id="e7c3b-118">-ACRName</span><span class="sxs-lookup"><span data-stu-id="e7c3b-118">-ACRName</span></span>
<span data-ttu-id="e7c3b-119">A beolvasott hozzáférés-vezérlési rekord nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e7c3b-119">Specifies the name of an access control record to get.</span></span>

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

### <span data-ttu-id="e7c3b-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="e7c3b-120">-Profile</span></span>
<span data-ttu-id="e7c3b-121">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="e7c3b-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="e7c3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c3b-122">CommonParameters</span></span>
<span data-ttu-id="e7c3b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e7c3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c3b-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7c3b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c3b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7c3b-125">INPUTS</span></span>

### <span data-ttu-id="e7c3b-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="e7c3b-126">None</span></span>

## <span data-ttu-id="e7c3b-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e7c3b-127">OUTPUTS</span></span>

### <span data-ttu-id="e7c3b-128">AccessControlRecord, IList\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="e7c3b-128">AccessControlRecord, IList\<AccessControlRecord\></span></span>
<span data-ttu-id="e7c3b-129">Ez a parancsmag egy **AccessControlRecord** -objektumot vagy **egy \<AccessControlRecord\> IList** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="e7c3b-129">This cmdlet returns an **AccessControlRecord** object or an **IList\<AccessControlRecord\>** object.</span></span>
<span data-ttu-id="e7c3b-130">A **AccessControlRecord** -objektumok az alábbi mezőket tartalmazzák:</span><span class="sxs-lookup"><span data-stu-id="e7c3b-130">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="e7c3b-131">**GlobalId** ( **karakterlánc** )</span><span class="sxs-lookup"><span data-stu-id="e7c3b-131">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="e7c3b-132">**InitiatorName** ( **karakterlánc** )</span><span class="sxs-lookup"><span data-stu-id="e7c3b-132">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="e7c3b-133">**InstanceId** ( **karakterlánc** )</span><span class="sxs-lookup"><span data-stu-id="e7c3b-133">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="e7c3b-134">**Name** ( **karakterlánc** )</span><span class="sxs-lookup"><span data-stu-id="e7c3b-134">**Name** ( **String** )</span></span> 
- <span data-ttu-id="e7c3b-135">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="e7c3b-135">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="e7c3b-136">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="e7c3b-136">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="e7c3b-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e7c3b-137">NOTES</span></span>

## <span data-ttu-id="e7c3b-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e7c3b-138">RELATED LINKS</span></span>

[<span data-ttu-id="e7c3b-139">Új – AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="e7c3b-139">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="e7c3b-140">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="e7c3b-140">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="e7c3b-141">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="e7c3b-141">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)


