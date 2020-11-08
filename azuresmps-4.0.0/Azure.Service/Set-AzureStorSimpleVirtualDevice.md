---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CE1C6576-234E-4891-9158-FA45B64B786C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41e8641b01dcb95a6b6939ff3551fe03b642ddf0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015435"
---
# <span data-ttu-id="c4c06-101">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="c4c06-101">Set-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="c4c06-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c4c06-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c06-103">StorSimple virtuális eszköz eszköz-konfigurációjának létrehozása vagy frissítése</span><span class="sxs-lookup"><span data-stu-id="c4c06-103">Creates or updates the device configuration of a StorSimple virtual device.</span></span>

## <span data-ttu-id="c4c06-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c4c06-104">SYNTAX</span></span>

```
Set-AzureStorSimpleVirtualDevice -DeviceName <String> -SecretKey <String> -AdministratorPassword <String>
 -SnapshotManagerPassword <String> [-TimeZone <TimeZoneInfo>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c4c06-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="c4c06-105">DESCRIPTION</span></span>
<span data-ttu-id="c4c06-106">A **set-AzureStorSimpleVirtualDevice** parancsmag létrehoz vagy frissít egy Azure StorSimple virtuális eszköz eszköz-konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="c4c06-106">The **Set-AzureStorSimpleVirtualDevice** cmdlet creates or updates the device configuration of an Azure StorSimple virtual device.</span></span>

## <span data-ttu-id="c4c06-107">Példák</span><span class="sxs-lookup"><span data-stu-id="c4c06-107">EXAMPLES</span></span>

### <span data-ttu-id="c4c06-108">Példa 1: virtuális eszköz frissítése</span><span class="sxs-lookup"><span data-stu-id="c4c06-108">Example 1: Update a virtual device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ==" -TimeZone $TimeZoneInfo
VERBOSE: ClientRequestId: e31f0d6b-451d-4c1d-b2f1-3fc84c13972c_PS
VERBOSE: ClientRequestId: df58db83-d563-4a2e-bbb4-9576f0e69ca6_PS
VERBOSE: ClientRequestId: 494a9f0d-79ee-4fde-ab4d-85ee5a357556_PS
VERBOSE: ClientRequestId: ce557cbf-174d-4301-93d4-5ffe082c8413_PS
VERBOSE: ClientRequestId: 31284dad-de2c-4758-a2ef-45962875bfa6_PS
VERBOSE: About to configure the device : win-ff93i74m1e1 ! 
VERBOSE: ClientRequestId: d9c66302-45d8-488a-adda-8ccf957f77d3_PS


TaskId       : 21f530c3-bc47-4591-8c4e-da4d694b751d
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: a94f972c-18ea-40b6-9401-2ad209c0c8b4_PS
AlertNotification              : Microsoft.WindowsAzure.Management.StorSimple.Models.AlertNotificationSettings
Chap                           : Microsoft.WindowsAzure.Management.StorSimple.Models.ChapSettings
DeviceProperties               : Microsoft.WindowsAzure.Management.StorSimple.Models.DeviceInfo
DnsServer                      : Microsoft.WindowsAzure.Management.StorSimple.Models.DnsServerSettings
InstanceId                     : d369ebb4-8b9a-47fc-9a6b-60f371e123ae
Name                           : 
NetInterfaceList               : {}
OperationInProgress            : None
RemoteMgmtSettingsInfo         : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteManagementSettings
RemoteMinishellSecretInfo      : Microsoft.WindowsAzure.Management.StorSimple.Models.RemoteMinishellSettings
SecretEncryptionCertThumbprint : 
Snapshot                       : Microsoft.WindowsAzure.Management.StorSimple.Models.SnapshotSettings
TimeServer                     : Microsoft.WindowsAzure.Management.StorSimple.Models.TimeSettings
Type                           : VirtualAppliance
VirtualApplianceProperties     : Microsoft.WindowsAzure.Management.StorSimple.Models.VirtualApplianceInfo
WebProxy                       : Microsoft.WindowsAzure.Management.StorSimple.Models.WebProxySettings

VERBOSE: Successfully updated configuration for device Contoso23 with id d369ebb4-8b9a-47fc-9a6b-60f371e123ae
```

<span data-ttu-id="c4c06-109">Az első parancs a **System. TimeZoneInfo** .net osztályt és a standard szintaxist használja a Pacific standard időzóna beszerzéséhez, valamint az objektum $TimeZoneInfo változóban való tárolásához.</span><span class="sxs-lookup"><span data-stu-id="c4c06-109">The first command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="c4c06-110">A második parancs frissíti a Contoso23 nevű eszközt az $TimeZoneInfo megadott időzóna használatához.</span><span class="sxs-lookup"><span data-stu-id="c4c06-110">The second command updates the device named Contoso23 to use the time zone specified in $TimeZoneInfo.</span></span>
<span data-ttu-id="c4c06-111">A parancshoz a virtuális eszköz konfigurációjának eléréséhez a titkos kulcs szükséges.</span><span class="sxs-lookup"><span data-stu-id="c4c06-111">The command requires the secret key to access the virtual device configuration.</span></span>

### <span data-ttu-id="c4c06-112">2. példa: virtuális eszköz frissítése a csővezeték-kezelő használatával</span><span class="sxs-lookup"><span data-stu-id="c4c06-112">Example 2: Update a virtual device by using the pipeline operator</span></span>
```
PS C:\> [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleVirtualDevice -DeviceName "Contoso23" -SecretKey "wcZBlBGpCMf4USdSKyt/SQ=="
```

<span data-ttu-id="c4c06-113">Ez a parancs frissíti a Contoso23 nevű eszközt a parancs által létrehozott időzóna használatához.</span><span class="sxs-lookup"><span data-stu-id="c4c06-113">This command updates the device named Contoso23 to use the time zone that the command creates.</span></span>
<span data-ttu-id="c4c06-114">A parancshoz a virtuális eszköz konfigurációjának eléréséhez a titkos kulcs szükséges.</span><span class="sxs-lookup"><span data-stu-id="c4c06-114">The command requires the secret key to access the virtual device configuration.</span></span>
<span data-ttu-id="c4c06-115">Ez a parancs ugyanúgy működik, mint az előző példában, azzal a különbséggel, hogy a csővezeték-kezelő segítségével átadja az időzónát az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="c4c06-115">This command works the same way as the previous example, except that it passes the time zone to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="c4c06-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c4c06-116">PARAMETERS</span></span>

### <span data-ttu-id="c4c06-117">-AdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="c4c06-117">-AdministratorPassword</span></span>
<span data-ttu-id="c4c06-118">Annak a virtuális eszköznek a rendszergazdai jelszava, amelyet konfigurálni szeretne.</span><span class="sxs-lookup"><span data-stu-id="c4c06-118">Specifies the administrator password of the virtual device to configure.</span></span>

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

### <span data-ttu-id="c4c06-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="c4c06-119">-DeviceName</span></span>
<span data-ttu-id="c4c06-120">A konfigurálni kívánt virtuális eszköz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4c06-120">Specifies the name of the virtual device to configure.</span></span>

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

### <span data-ttu-id="c4c06-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="c4c06-121">-Profile</span></span>
<span data-ttu-id="c4c06-122">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="c4c06-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="c4c06-123">-SecretKey</span><span class="sxs-lookup"><span data-stu-id="c4c06-123">-SecretKey</span></span>
<span data-ttu-id="c4c06-124">A virtuális eszköz szolgáltatás-titkosítási kulcsát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4c06-124">Specifies a service encryption key for the virtual device.</span></span>
<span data-ttu-id="c4c06-125">Ez a kulcs akkor jön létre, ha az első fizikai eszköz van regisztrálva egy erőforrással.</span><span class="sxs-lookup"><span data-stu-id="c4c06-125">This key is generated when the first physical device is registered with a resource.</span></span>

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

### <span data-ttu-id="c4c06-126">-SnapshotManagerPassword</span><span class="sxs-lookup"><span data-stu-id="c4c06-126">-SnapshotManagerPassword</span></span>
<span data-ttu-id="c4c06-127">A Snapshot Manager jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4c06-127">Specifies the snapshot manager password.</span></span>

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

### <span data-ttu-id="c4c06-128">-Időzóna</span><span class="sxs-lookup"><span data-stu-id="c4c06-128">-TimeZone</span></span>
<span data-ttu-id="c4c06-129">Az eszközhöz tartozó időzónát adja meg.</span><span class="sxs-lookup"><span data-stu-id="c4c06-129">Specifies a time zone for the device.</span></span>
<span data-ttu-id="c4c06-130">**TimeZoneInfo** -objektumot a **GetSystemTimeZone ()** metódus segítségével hozhat létre.</span><span class="sxs-lookup"><span data-stu-id="c4c06-130">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="c4c06-131">A parancs például létrehoz egy időzóna információs objektumot a Pacific standard időpontjának: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="c4c06-131">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c06-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c06-132">CommonParameters</span></span>
<span data-ttu-id="c4c06-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c4c06-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c06-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4c06-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c06-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4c06-135">INPUTS</span></span>

### <span data-ttu-id="c4c06-136">TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="c4c06-136">TimeZoneInfo</span></span>
<span data-ttu-id="c4c06-137">Ezt a parancsmagot a **TimeZoneInfo** -objektum pipe-ra kapcsolhatja.</span><span class="sxs-lookup"><span data-stu-id="c4c06-137">You can pipe a **TimeZoneInfo** object to this cmdlet.</span></span>

## <span data-ttu-id="c4c06-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4c06-138">OUTPUTS</span></span>

### <span data-ttu-id="c4c06-139">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="c4c06-139">DeviceJobDetails</span></span>
<span data-ttu-id="c4c06-140">Ez a parancsmag a virtuális eszköz frissített eszközének adatait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="c4c06-140">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="c4c06-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c4c06-141">NOTES</span></span>

## <span data-ttu-id="c4c06-142">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4c06-142">RELATED LINKS</span></span>

[<span data-ttu-id="c4c06-143">Új – AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="c4c06-143">New-AzureStorSimpleVirtualDevice</span></span>](./New-AzureStorSimpleVirtualDevice.md)

[<span data-ttu-id="c4c06-144">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="c4c06-144">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)


