---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: C50959BB-7481-4898-BF4B-C5ABF8758473
online version: ''
schema: 2.0.0
ms.openlocfilehash: e2c06455004afbd15235f59164034abc2147964b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016453"
---
# <span data-ttu-id="5b67e-101">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="5b67e-101">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="5b67e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5b67e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b67e-103">Kötet-tároló eltávolítása egy StorSimple-eszközről.</span><span class="sxs-lookup"><span data-stu-id="5b67e-103">Removes a volume container from a StorSimple device.</span></span>

## <span data-ttu-id="5b67e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5b67e-104">SYNTAX</span></span>

```
Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainer <DataContainer>
 [-WaitForComplete] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5b67e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5b67e-105">DESCRIPTION</span></span>
<span data-ttu-id="5b67e-106">A **Remove-AzureStorSimpleDeviceVolumeContainer** parancsmag eltávolítja a mennyiségi tároló objektumot egy StorSimple-eszközről.</span><span class="sxs-lookup"><span data-stu-id="5b67e-106">The **Remove-AzureStorSimpleDeviceVolumeContainer** cmdlet removes a volume container object from a StorSimple device.</span></span>
<span data-ttu-id="5b67e-107">Ez a parancsmag csak akkor kér megerősítést, ha az *erő* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b67e-107">This cmdlet prompts you for confirmation unless you specify the *Force* parameter.</span></span>

## <span data-ttu-id="5b67e-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5b67e-108">EXAMPLES</span></span>

### <span data-ttu-id="5b67e-109">1. példa: tároló eltávolítása a csővezeték használatával</span><span class="sxs-lookup"><span data-stu-id="5b67e-109">Example 1: Remove a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" | Remove-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -Force
VERBOSE: ClientRequestId: 0efbb4fc-ceb0-4311-bc49-0e08161d0a37_PS
VERBOSE: ClientRequestId: bf5b615f-47e3-4868-91b6-f2d12217a302_PS
VERBOSE: ClientRequestId: 5590c87e-0602-4197-b6c3-cf58b0e7a7b3_PS
VERBOSE: ClientRequestId: b33c71ac-c345-44ff-8213-d7fdf9f8480a_PS
VERBOSE: ClientRequestId: 903d42ef-58f4-4e89-ba7f-5f234262356d_PS
VERBOSE: About to create a job to remove your Volume container! 
VERBOSE: ClientRequestId: 2279575f-5115-4344-9c6f-9ef599bd203e_PS
e9ddec89-67ac-4e2e-a2ed-820de3547bb0
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
e9ddec89-67ac-4e2e-a2ed-820de3547bb0 for tracking the task's status
VERBOSE: Volume container with name: Container08 is found.
```

<span data-ttu-id="5b67e-110">Ez a parancs a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmag segítségével a Container08 nevű kötet tárolóját kapja a Contoso63-AppVm nevű eszközön.</span><span class="sxs-lookup"><span data-stu-id="5b67e-110">This command gets the volume container named Container08 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="5b67e-111">A parancs a pipeline operátor segítségével átadja a kötet tárolóját az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="5b67e-111">The command passes the volume container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5b67e-112">Ez a parancs elindítja a feladatot a tároló eltávolításához, majd egy **TaskResponse** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="5b67e-112">This command starts the task to remove the container, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="5b67e-113">A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5b67e-113">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>
<span data-ttu-id="5b67e-114">Ez a parancs az *erő* paramétert adja meg, ezért nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5b67e-114">This command specifies the *Force* parameter, so it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="5b67e-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5b67e-115">PARAMETERS</span></span>

### <span data-ttu-id="5b67e-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5b67e-116">-DeviceName</span></span>
<span data-ttu-id="5b67e-117">Annak a StorSimple-eszköznek a nevét adja meg, amelybe az eltávolítandó kötetet el szeretné helyezni.</span><span class="sxs-lookup"><span data-stu-id="5b67e-117">Specifies the name of the StorSimple device on which to the volume container to remove exists.</span></span>

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

### <span data-ttu-id="5b67e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5b67e-118">-Force</span></span>
<span data-ttu-id="5b67e-119">Azt jelzi, hogy ez a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5b67e-119">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="5b67e-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="5b67e-120">-Profile</span></span>
<span data-ttu-id="5b67e-121">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="5b67e-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="5b67e-122">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="5b67e-122">-VolumeContainer</span></span>
<span data-ttu-id="5b67e-123">Az eltávolítandó kötet tárolóját adja meg **DataContainer** objektumként.</span><span class="sxs-lookup"><span data-stu-id="5b67e-123">Specifies the volume container to remove, as a **DataContainer** object.</span></span>
<span data-ttu-id="5b67e-124">Ha **DataContainer** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleDeviceVolumeContainer** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="5b67e-124">To obtain a **DataContainer** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b67e-125">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="5b67e-125">-WaitForComplete</span></span>
<span data-ttu-id="5b67e-126">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="5b67e-126">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="5b67e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b67e-127">CommonParameters</span></span>
<span data-ttu-id="5b67e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5b67e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b67e-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b67e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b67e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b67e-130">INPUTS</span></span>

### <span data-ttu-id="5b67e-131">DataContainer</span><span class="sxs-lookup"><span data-stu-id="5b67e-131">DataContainer</span></span>
<span data-ttu-id="5b67e-132">Ez a parancsmag az eltávolítandó **DataContainer** -objektumot fogadja el.</span><span class="sxs-lookup"><span data-stu-id="5b67e-132">This cmdlet accepts a **DataContainer** object to remove.</span></span>

## <span data-ttu-id="5b67e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5b67e-133">OUTPUTS</span></span>

### <span data-ttu-id="5b67e-134">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="5b67e-134">TaskStatusInfo</span></span>
<span data-ttu-id="5b67e-135">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="5b67e-135">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="5b67e-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5b67e-136">NOTES</span></span>

## <span data-ttu-id="5b67e-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5b67e-137">RELATED LINKS</span></span>

[<span data-ttu-id="5b67e-138">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="5b67e-138">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="5b67e-139">Új – AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="5b67e-139">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


