---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 8C7551CD-0222-44D1-AA1B-647669B01853
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdb7b8f1b53f7352e3e147c6f203e3a4460e8a05
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016289"
---
# <span data-ttu-id="6967d-101">Get-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="6967d-101">Get-AzureStorSimpleDeviceBackupPolicy</span></span>

## <span data-ttu-id="6967d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6967d-102">SYNOPSIS</span></span>
<span data-ttu-id="6967d-103">Visszakapja a biztonsági házirendeket.</span><span class="sxs-lookup"><span data-stu-id="6967d-103">Gets backup policies.</span></span>

## <span data-ttu-id="6967d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6967d-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> [-BackupPolicyName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6967d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6967d-105">DESCRIPTION</span></span>
<span data-ttu-id="6967d-106">A **Get-AzureStorSimpleDeviceBackupPolicy** parancsmag biztonsági házirendeket kap.</span><span class="sxs-lookup"><span data-stu-id="6967d-106">The **Get-AzureStorSimpleDeviceBackupPolicy** cmdlet gets backup policies.</span></span>
<span data-ttu-id="6967d-107">Ez a parancsmag egy **BackupPolicy** -objektumot vagy egy eszközhöz tartozó összes **BackupPolicy** -objektum listáját ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="6967d-107">This cmdlet returns a **BackupPolicy** object or a list of all the **BackupPolicy** objects that belong to a device.</span></span>
<span data-ttu-id="6967d-108">A biztonsági házirend-objektumok a következő tulajdonságokat tartalmazzák:</span><span class="sxs-lookup"><span data-stu-id="6967d-108">The backup policy objects contain the following properties:</span></span> 

- <span data-ttu-id="6967d-109">**név**</span><span class="sxs-lookup"><span data-stu-id="6967d-109">**Name**</span></span>
- <span data-ttu-id="6967d-110">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="6967d-110">**InstanceId**</span></span>
- <span data-ttu-id="6967d-111">**BackupPolicyCreationType**</span><span class="sxs-lookup"><span data-stu-id="6967d-111">**BackupPolicyCreationType**</span></span>
- <span data-ttu-id="6967d-112">**LastBackup**</span><span class="sxs-lookup"><span data-stu-id="6967d-112">**LastBackup**</span></span>
- <span data-ttu-id="6967d-113">**NextBackup**</span><span class="sxs-lookup"><span data-stu-id="6967d-113">**NextBackup**</span></span>
- <span data-ttu-id="6967d-114">**SchedulesCount**</span><span class="sxs-lookup"><span data-stu-id="6967d-114">**SchedulesCount**</span></span>
- <span data-ttu-id="6967d-115">**SSMHostName**</span><span class="sxs-lookup"><span data-stu-id="6967d-115">**SSMHostName**</span></span>
- <span data-ttu-id="6967d-116">**VolumesCount**</span><span class="sxs-lookup"><span data-stu-id="6967d-116">**VolumesCount**</span></span>

## <span data-ttu-id="6967d-117">Példák</span><span class="sxs-lookup"><span data-stu-id="6967d-117">EXAMPLES</span></span>

### <span data-ttu-id="6967d-118">Példa 1: adatok beszerzése házirendhez</span><span class="sxs-lookup"><span data-stu-id="6967d-118">Example 1: Get details for a policy</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "GeneralBackupPolicy07"
VERBOSE: ClientRequestId: 2a878cd6-8432-4646-8be8-a0cb0750958e_PS
VERBOSE: ClientRequestId: 00ea5a6d-8c27-4e22-b182-5969cdbb8033_PS
VERBOSE: ClientRequestId: 39dac9ff-4455-45ae-ae3d-7de1445b9520_PS


BackupSchedules          : {8658e3a2-8a59-4d43-8725-ab0c95665301}
Volumes                  : {testvolume03, testvolume05}
BackupPolicyCreationType : BySaaS
LastBackup               : 
NextBackup               : 16-12-2014 00:30:00
SchedulesCount           : 1
SSMHostName              : 
VolumesCount             : 2
InstanceId               : 84140a6a-9254-4fff-8d09-ae40e9f1bc7d
Name                     : GeneralBackupPolicy07
OperationInProgress      : None

VERBOSE: BackupPolicy with id 84140a6a-9254-4fff-8d09-ae40e9f1bc7d found!
```

<span data-ttu-id="6967d-119">Ez a parancs a Contoso63-AppVm nevű eszközön a GeneralBackupPolicy07 nevű **BackupPolicyDetails** -objektumot kapja.</span><span class="sxs-lookup"><span data-stu-id="6967d-119">This command gets a **BackupPolicyDetails** object named GeneralBackupPolicy07 on the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="6967d-120">2. példa: biztonsági mentési házirendek listájának beszerzése</span><span class="sxs-lookup"><span data-stu-id="6967d-120">Example 2: Get a list of backup policies</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               SchedulesCount VolumesCount                       BackupPolicyCreationType          LastBackup                        NextBackup                        SSMHostName                      
----------                           ----                               -------------- ------------                       ------------------------          ----------                        ----------                        -----------                      
13db29a4-bba9-4871-b872-db1fa0506b16 VG Clones                          1              2                                  BySaaS                            4/15/2015 8:30:02 AM              4/15/2015 8:30:00 PM                                               
2dcd3002-13c4-4bdb-a1ef-b35ce0a29416 vg-all                             1              4                                  BySaaS                            3/27/2015 9:12:15 PM              1/1/2010 5:30:00 AM                                                
54828d08-8309-4bd4-828f-21904863fb4c Cloud_Snapshot_Vol3_clone VG       1              1                                  BySaaS                            4/15/2015 9:00:03 AM              4/17/2015 9:00:30 AM                                               
6a51f39e-0ec9-4c57-8ec9-14a9255efa95 Test Group                         0              2                                  BySaaS                            3/27/2015 1:47:00 AM              1/1/2010 5:30:00 AM                                                
81c2db43-38f7-45fc-b2f2-476d1f6039a7 Cloud_Snapshot_Vol1_clone VG       1              1                                  BySaaS                            4/15/2015 7:30:02 AM              4/17/2015 7:30:00 AM                                               
82c4a5be-7473-431f-86e7-9db31ee9a9f8 Cloud_Snapshot_vg-all              1              4                                  BySaaS                            4/15/2015 11:30:02 AM             4/15/2015 3:30:00 PM                                               
cda96e83-3b38-4345-a56d-c8a96a0e57b3 Snapshot_vg-all                    1              4                                  BySaaS                            4/15/2015 1:30:02 PM              4/15/2015 3:30:00 PM
```

<span data-ttu-id="6967d-121">Ez a parancs felsorolja a **BackupPolicy** -objektumokat az eszközön, a Contoso63-AppVm nevű eszközön.</span><span class="sxs-lookup"><span data-stu-id="6967d-121">This command lists the **BackupPolicy** objects on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="6967d-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6967d-122">PARAMETERS</span></span>

### <span data-ttu-id="6967d-123">-BackupPolicyName</span><span class="sxs-lookup"><span data-stu-id="6967d-123">-BackupPolicyName</span></span>
<span data-ttu-id="6967d-124">A beolvasott biztonságimásolat-házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6967d-124">Specifies the name of the backup policy to get.</span></span>
<span data-ttu-id="6967d-125">Ha nem adja meg ezt a paramétert, ez a parancsmag minden házirendet megkapja.</span><span class="sxs-lookup"><span data-stu-id="6967d-125">If you do not specify this parameter, this cmdlet gets all policies.</span></span>

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

### <span data-ttu-id="6967d-126">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="6967d-126">-DeviceName</span></span>
<span data-ttu-id="6967d-127">Annak a StorSimple-eszköznek a nevét adja meg, amelyen létre szeretné hozni a biztonsági házirendet.</span><span class="sxs-lookup"><span data-stu-id="6967d-127">Specifies the name of the StorSimple device on which to create the backup policy.</span></span>

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

### <span data-ttu-id="6967d-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="6967d-128">-Profile</span></span>
<span data-ttu-id="6967d-129">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="6967d-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="6967d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6967d-130">CommonParameters</span></span>
<span data-ttu-id="6967d-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6967d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6967d-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6967d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6967d-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6967d-133">INPUTS</span></span>

### <span data-ttu-id="6967d-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="6967d-134">None</span></span>

## <span data-ttu-id="6967d-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6967d-135">OUTPUTS</span></span>

### <span data-ttu-id="6967d-136">IList \<BackupPolicy\> , BackupPolicyDetails</span><span class="sxs-lookup"><span data-stu-id="6967d-136">IList\<BackupPolicy\>, BackupPolicyDetails</span></span>
<span data-ttu-id="6967d-137">Ez a parancsmag **BackupPolicyDetails** -objektumot ad eredményül, ha a *BackupPolicyName* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="6967d-137">This cmdlet returns a **BackupPolicyDetails** object, if you specify the *BackupPolicyName* parameter.</span></span>
<span data-ttu-id="6967d-138">Ha nem adja meg ezt a paramétert, az eredmény **egy \<BackupPolicy\> IList** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="6967d-138">If you do not specify that parameter, it returns an **IList\<BackupPolicy\>** object.</span></span>

## <span data-ttu-id="6967d-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6967d-139">NOTES</span></span>

## <span data-ttu-id="6967d-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6967d-140">RELATED LINKS</span></span>

[<span data-ttu-id="6967d-141">Új – AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="6967d-141">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="6967d-142">Remove-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="6967d-142">Remove-AzureStorSimpleDeviceBackupPolicy</span></span>](./Remove-AzureStorSimpleDeviceBackupPolicy.md)

[<span data-ttu-id="6967d-143">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="6967d-143">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)


