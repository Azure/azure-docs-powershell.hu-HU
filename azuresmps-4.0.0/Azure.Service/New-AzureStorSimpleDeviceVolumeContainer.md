---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5605F11E-EEA0-4C32-8445-2E001D56BC47
online version: ''
schema: 2.0.0
ms.openlocfilehash: e364692858cf190b48b61f4d38fbf483d229ffb7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015520"
---
# <span data-ttu-id="aea14-101">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="aea14-101">New-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="aea14-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="aea14-102">SYNOPSIS</span></span>
<span data-ttu-id="aea14-103">Kötet tárolót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="aea14-103">Creates a volume container.</span></span>

## <span data-ttu-id="aea14-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="aea14-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainerName <String>
 -PrimaryStorageAccountCredential <StorageAccountCredentialResponse> -BandWidthRateInMbps <Int32>
 [-EncryptionEnabled <Boolean>] [-EncryptionKey <String>] [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="aea14-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="aea14-105">DESCRIPTION</span></span>
<span data-ttu-id="aea14-106">A **New-AzureStorSimpleDeviceVolumeContainer** parancsmag létrehoz egy kötet tárolót.</span><span class="sxs-lookup"><span data-stu-id="aea14-106">The **New-AzureStorSimpleDeviceVolumeContainer** cmdlet creates a volume container.</span></span>
<span data-ttu-id="aea14-107">Az új mennyiségi tárolóhoz társítania kell egy tárolási fiók hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="aea14-107">You must associate a storage account credential with the new volume container.</span></span>
<span data-ttu-id="aea14-108">A **Get-AzureStorSimpleStorageAccountCredential** parancsmaggal szerezhet be tárolási fiók hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="aea14-108">To obtain a storage account credential, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

## <span data-ttu-id="aea14-109">Példák</span><span class="sxs-lookup"><span data-stu-id="aea14-109">EXAMPLES</span></span>

### <span data-ttu-id="aea14-110">Példa 1: tároló létrehozása</span><span class="sxs-lookup"><span data-stu-id="aea14-110">Example 1: Create a container</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount" | New-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" -BandWidthRateInMbps 256
VERBOSE: ClientRequestId: 96a4ccd4-f2a9-4820-8bc8-e6b7b56dce0d_PS
VERBOSE: ClientRequestId: 90be20db-098a-4f2b-a6da-9da6f533a846_PS
VERBOSE: ClientRequestId: 410fd33a-8fa3-4ae5-a1bf-1b6da9b34ffc_PS
VERBOSE: Storage Access Credential with name ContosoAccount found! 
VERBOSE: ClientRequestId: 0a6d1008-ba1f-43b2-a424-9c86be2fb83b_PS
VERBOSE: ClientRequestId: 08f0d657-a130-4a25-8090-270c58b479dc_PS
VERBOSE: ClientRequestId: 0f3e894a-b031-467c-a258-41b74c89cf18_PS
5b192120-9df0-40ed-b75e-b4e728bd37ef
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
5b192120-9df0-40ed-b75e-b4e728bd37ef for tracking the task's status
```

<span data-ttu-id="aea14-111">Ez a parancs a **Get-AzureStorSimpleStorageAccountCredential** parancsmag használatával kapja meg a ContosoAccount nevű fiókhoz tartozó tárolási fiók hitelesítő adatait.</span><span class="sxs-lookup"><span data-stu-id="aea14-111">This command gets the storage account credential for the account named ContosoAccount by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>
<span data-ttu-id="aea14-112">A parancs a pipeline operátor segítségével továbbítja a hitelesítő adatokat az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="aea14-112">The command passes the credential to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="aea14-113">Ez a parancsmag az adott parancsmag hitelesítő adataival hozza létre a Container08 nevű tárolót a Contoso63-AppVm nevű eszközön.</span><span class="sxs-lookup"><span data-stu-id="aea14-113">This cmdlet uses the credential from that cmdlet to create the container named Container08 on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="aea14-114">Ez a parancs elindítja a feladatot, majd egy **TaskResponse** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="aea14-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="aea14-115">A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aea14-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="aea14-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="aea14-116">PARAMETERS</span></span>

### <span data-ttu-id="aea14-117">-BandWidthRateInMbps</span><span class="sxs-lookup"><span data-stu-id="aea14-117">-BandWidthRateInMbps</span></span>
<span data-ttu-id="aea14-118">A sávszélesség sebességének meghatározása másodpercenként (Mbps).</span><span class="sxs-lookup"><span data-stu-id="aea14-118">Specifies the bandwidth rate in megabits per second (Mbps).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CloudBandwidthInMbps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea14-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="aea14-119">-DeviceName</span></span>
<span data-ttu-id="aea14-120">Annak a StorSimple-eszköznek a nevét adja meg, amelybe a kötet tárolóját létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="aea14-120">Specifies the name of the StorSimple device on which to create the volume container.</span></span>

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

### <span data-ttu-id="aea14-121">-EncryptionEnabled</span><span class="sxs-lookup"><span data-stu-id="aea14-121">-EncryptionEnabled</span></span>
<span data-ttu-id="aea14-122">Azt jelzi, hogy engedélyezi-e a titkosítást.</span><span class="sxs-lookup"><span data-stu-id="aea14-122">Indicates whether to enable encryption.</span></span>

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

### <span data-ttu-id="aea14-123">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="aea14-123">-EncryptionKey</span></span>
<span data-ttu-id="aea14-124">A titkosítási kulcsot adja meg.</span><span class="sxs-lookup"><span data-stu-id="aea14-124">Specifies the encryption key.</span></span>

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

### <span data-ttu-id="aea14-125">-PrimaryStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="aea14-125">-PrimaryStorageAccountCredential</span></span>
<span data-ttu-id="aea14-126">A hitelesítő adatokat **StorageAccountCredential** objektumként adja meg az új mennyiségi tárolóhoz való társításhoz.</span><span class="sxs-lookup"><span data-stu-id="aea14-126">Specifies the credential, as a **StorageAccountCredential** object, to associate with the new volume container.</span></span>
<span data-ttu-id="aea14-127">Ha **StorageAccountCredential** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleStorageAccountCredential** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="aea14-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: (All)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aea14-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="aea14-128">-Profile</span></span>
<span data-ttu-id="aea14-129">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="aea14-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="aea14-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="aea14-130">-VolumeContainerName</span></span>
<span data-ttu-id="aea14-131">A létrehozandó mennyiségi tároló nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="aea14-131">Specifies the name of the volume container to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea14-132">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="aea14-132">-WaitForComplete</span></span>
<span data-ttu-id="aea14-133">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="aea14-133">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="aea14-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea14-134">CommonParameters</span></span>
<span data-ttu-id="aea14-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="aea14-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea14-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aea14-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea14-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="aea14-137">INPUTS</span></span>

### <span data-ttu-id="aea14-138">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="aea14-138">StorageAccountCredential</span></span>
<span data-ttu-id="aea14-139">Ez a parancsmag egy **PrimaryStorageAccountCredential** -objektumot fogad el a mennyiségi tárolóhoz való társításhoz.</span><span class="sxs-lookup"><span data-stu-id="aea14-139">This cmdlet accepts a **PrimaryStorageAccountCredential** object to associate with the volume container.</span></span>

## <span data-ttu-id="aea14-140">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="aea14-140">OUTPUTS</span></span>

### <span data-ttu-id="aea14-141">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="aea14-141">TaskStatusInfo</span></span>
<span data-ttu-id="aea14-142">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="aea14-142">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="aea14-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="aea14-143">NOTES</span></span>

## <span data-ttu-id="aea14-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="aea14-144">RELATED LINKS</span></span>

[<span data-ttu-id="aea14-145">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="aea14-145">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="aea14-146">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="aea14-146">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="aea14-147">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="aea14-147">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="aea14-148">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="aea14-148">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


