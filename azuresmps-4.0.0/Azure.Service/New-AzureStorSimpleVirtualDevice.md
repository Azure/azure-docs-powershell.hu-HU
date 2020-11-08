---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015511"
---
# <span data-ttu-id="1aa03-101">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="1aa03-101">New-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="1aa03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1aa03-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa03-103">Virtuális StorSimple eszközt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1aa03-103">Creates a virtual StorSimple device.</span></span>

## <span data-ttu-id="1aa03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1aa03-104">SYNTAX</span></span>

### <span data-ttu-id="1aa03-105">CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1aa03-105">CreateNewStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="1aa03-106">UseExistingStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1aa03-106">UseExistingStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1aa03-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1aa03-107">DESCRIPTION</span></span>
<span data-ttu-id="1aa03-108">A **New-AzureStorSimpleVirtualDevice** parancsmag virtuális StorSimple eszközt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1aa03-108">The **New-AzureStorSimpleVirtualDevice** cmdlet creates a virtual StorSimple device.</span></span>
<span data-ttu-id="1aa03-109">Adja meg az eszköz nevét.</span><span class="sxs-lookup"><span data-stu-id="1aa03-109">Specify a device name for the device.</span></span>
<span data-ttu-id="1aa03-110">Adja meg a virtuális hálózat virtuális hálózat-és alhálózati adatait ugyanazon előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="1aa03-110">Specify virtual network and subnet details for the virtual network in the same subscription.</span></span>
<span data-ttu-id="1aa03-111">A Geo-nek egyeznie kell azzal a GEO-val, amelybe a StorSimple erőforrás jön létre.</span><span class="sxs-lookup"><span data-stu-id="1aa03-111">The geo should match the geo in which the StorSimple resource is created.</span></span>
<span data-ttu-id="1aa03-112">Ha a virtuális eszközhöz meglévő tárolási fiókot szeretne használni, adja meg a nevet.</span><span class="sxs-lookup"><span data-stu-id="1aa03-112">To use an existing storage account for this virtual device, specify the name.</span></span>
<span data-ttu-id="1aa03-113">Ha új tárolási fiókot szeretne létrehozni ehhez a virtuális eszközhöz, adja meg a *StorageAccountName* és a *CreateNewStorageAccount* paramétert is.</span><span class="sxs-lookup"><span data-stu-id="1aa03-113">To create a new storage account for this virtual device, specify both the *StorageAccountName* and the *CreateNewStorageAccount* parameters.</span></span>

## <span data-ttu-id="1aa03-114">Példák</span><span class="sxs-lookup"><span data-stu-id="1aa03-114">EXAMPLES</span></span>

### <span data-ttu-id="1aa03-115">Példa 1: virtuális eszköz létrehozása új fiókkal és meglévő hálózattal</span><span class="sxs-lookup"><span data-stu-id="1aa03-115">Example 1: Create a virtual device with a new account and an existing network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

<span data-ttu-id="1aa03-116">Ez a parancs létrehoz egy virtuális eszközt, amely egy új tárolási fiókot és egy meglévő virtuális hálózatot használ.</span><span class="sxs-lookup"><span data-stu-id="1aa03-116">This command creates a virtual device that uses a new storage account and an existing virtual network.</span></span>

### <span data-ttu-id="1aa03-117">2. példa: virtuális eszköz létrehozása meglévő fiókkal és virtuális hálózattal</span><span class="sxs-lookup"><span data-stu-id="1aa03-117">Example 2: Create a virtual device with an existing account and virtual network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

<span data-ttu-id="1aa03-118">Ez a parancs létrehoz egy virtuális eszközt, amely egy meglévő tárterület-fiókot és egy meglévő virtuális hálózatot használ.</span><span class="sxs-lookup"><span data-stu-id="1aa03-118">This command creates a virtual device that uses an existing storage account and an existing virtual network.</span></span>

## <span data-ttu-id="1aa03-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1aa03-119">PARAMETERS</span></span>

### <span data-ttu-id="1aa03-120">-CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1aa03-120">-CreateNewStorageAccount</span></span>
<span data-ttu-id="1aa03-121">Jelzi, hogy ez a parancsmag új tárterület-fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1aa03-121">Indicates that this cmdlet creates a new storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa03-122">-PersistAzureVMOnFailrue</span><span class="sxs-lookup"><span data-stu-id="1aa03-122">-PersistAzureVMOnFailrue</span></span>
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

### <span data-ttu-id="1aa03-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="1aa03-123">-Profile</span></span>
<span data-ttu-id="1aa03-124">Azt az Azure-profilt adja meg, amelyből a parancsmag olvasható.</span><span class="sxs-lookup"><span data-stu-id="1aa03-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1aa03-125">Ha nem ad meg profilt, a parancsmag a helyi alapértelmezett profilból olvassa be a szöveget.</span><span class="sxs-lookup"><span data-stu-id="1aa03-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1aa03-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1aa03-126">-StorageAccountName</span></span>
<span data-ttu-id="1aa03-127">A tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1aa03-127">Specifies the name of a storage account.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa03-128">-SubNetName</span><span class="sxs-lookup"><span data-stu-id="1aa03-128">-SubNetName</span></span>
<span data-ttu-id="1aa03-129">A virtuális alhálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1aa03-129">Specifies the name of a virtual subnet.</span></span>

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

### <span data-ttu-id="1aa03-130">-VirtualDeviceName</span><span class="sxs-lookup"><span data-stu-id="1aa03-130">-VirtualDeviceName</span></span>
<span data-ttu-id="1aa03-131">A virtuális eszköz nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1aa03-131">Specifies a name for the virtual device.</span></span>

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

### <span data-ttu-id="1aa03-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="1aa03-132">-VirtualNetworkName</span></span>
<span data-ttu-id="1aa03-133">A virtuális hálózat nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1aa03-133">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aa03-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa03-134">CommonParameters</span></span>
<span data-ttu-id="1aa03-135">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1aa03-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa03-136">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aa03-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa03-137">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1aa03-137">INPUTS</span></span>

## <span data-ttu-id="1aa03-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1aa03-138">OUTPUTS</span></span>

### <span data-ttu-id="1aa03-139">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="1aa03-139">String</span></span>
<span data-ttu-id="1aa03-140">Ez a parancsmag a virtuális eszközt létrehozó feladat AZONOSÍTÓját számítja ki.</span><span class="sxs-lookup"><span data-stu-id="1aa03-140">This cmdlet returns the ID of the job that creates the virtual device.</span></span>
<span data-ttu-id="1aa03-141">Ezt az azonosítót használva követheti nyomon az eredményeket az Get-AzureStorSimpleJob parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="1aa03-141">You can use this ID to track the progress using the Get-AzureStorSimpleJob cmdlet.</span></span>

## <span data-ttu-id="1aa03-142">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1aa03-142">NOTES</span></span>

## <span data-ttu-id="1aa03-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1aa03-143">RELATED LINKS</span></span>

[<span data-ttu-id="1aa03-144">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="1aa03-144">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="1aa03-145">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="1aa03-145">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


