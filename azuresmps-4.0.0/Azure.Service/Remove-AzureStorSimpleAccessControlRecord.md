---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016096"
---
# <span data-ttu-id="87eda-101">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="87eda-101">Remove-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="87eda-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="87eda-102">SYNOPSIS</span></span>
<span data-ttu-id="87eda-103">Egy Access-vezérlő rekord törlése a szolgáltatás konfigurációjától</span><span class="sxs-lookup"><span data-stu-id="87eda-103">Deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="87eda-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="87eda-104">SYNTAX</span></span>

### <span data-ttu-id="87eda-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="87eda-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="87eda-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="87eda-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="87eda-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="87eda-107">DESCRIPTION</span></span>
<span data-ttu-id="87eda-108">A **Remove-AzureStorSimpleAccessControlRecord** parancsmag egy Access-vezérlő rekordot töröl a szolgáltatás konfigurációjától.</span><span class="sxs-lookup"><span data-stu-id="87eda-108">The **Remove-AzureStorSimpleAccessControlRecord** cmdlet deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="87eda-109">Példák</span><span class="sxs-lookup"><span data-stu-id="87eda-109">EXAMPLES</span></span>

### <span data-ttu-id="87eda-110">1. példa: Access-Controlaccess-vezérlő recordaccess-vezérlő eltávolítása</span><span class="sxs-lookup"><span data-stu-id="87eda-110">Example 1: Remove an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

<span data-ttu-id="87eda-111">Ez a parancs törli a Acr10 nevű Access-vezérlő rekordot.</span><span class="sxs-lookup"><span data-stu-id="87eda-111">This command deletes the access control record named Acr10.</span></span>
<span data-ttu-id="87eda-112">Ez a parancs a *WaitForComplete* paramétert adja meg, ezért a parancs mindaddig megvárja, amíg a művelet be nem fejeződik, majd egy **TaskStatusInfo** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="87eda-112">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="87eda-113">2. példa: Access-Controlaccess rekordok eltávolítása a pipelineAccess Controlaccess Controlaccess-vezérlő segítségével</span><span class="sxs-lookup"><span data-stu-id="87eda-113">Example 2: Remove an Access Controlaccess control record by using the pipelineAccess Controlaccess controlaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

<span data-ttu-id="87eda-114">Ez a parancs a **Get-AzureStorSimpleAccessControlRecord** segítségével beolvassa a Acr10 nevű **AccessControlRecord** , majd a pipeline operátor segítségével átadja az objektumot az aktuális parancsmagnak.</span><span class="sxs-lookup"><span data-stu-id="87eda-114">This command uses the **Get-AzureStorSimpleAccessControlRecord** to get the **AccessControlRecord** named Acr10, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="87eda-115">A parancs elindítja azt a műveletet, amely eltávolítja a **AccessControlRecord** objektumot, majd egy **TaskResponse** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="87eda-115">The command starts the operation that removes the **AccessControlRecord** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="87eda-116">A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="87eda-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="87eda-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="87eda-117">PARAMETERS</span></span>

### <span data-ttu-id="87eda-118">-ACR</span><span class="sxs-lookup"><span data-stu-id="87eda-118">-ACR</span></span>
<span data-ttu-id="87eda-119">Egy törölni kívánt **AccessControlRecord** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="87eda-119">Specifies an **AccessControlRecord** object to delete.</span></span>
<span data-ttu-id="87eda-120">Ha **AccessControlRecord** objektumot szeretne beolvasni, használja a **Get-AzureStorSimpleAccessControlRecord** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="87eda-120">To obtain an **AccessControlRecord** object, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87eda-121">-ACRName</span><span class="sxs-lookup"><span data-stu-id="87eda-121">-ACRName</span></span>
<span data-ttu-id="87eda-122">A törlendő hozzáférés-szabályozási rekord nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="87eda-122">Specifies a name of the access control record to delete.</span></span>

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

### <span data-ttu-id="87eda-123">-Force</span><span class="sxs-lookup"><span data-stu-id="87eda-123">-Force</span></span>
<span data-ttu-id="87eda-124">Azt jelzi, hogy ez a parancsmag nem kér megerősítést.</span><span class="sxs-lookup"><span data-stu-id="87eda-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="87eda-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="87eda-125">-Profile</span></span>
<span data-ttu-id="87eda-126">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="87eda-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="87eda-127">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="87eda-127">-WaitForComplete</span></span>
<span data-ttu-id="87eda-128">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="87eda-128">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="87eda-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87eda-129">CommonParameters</span></span>
<span data-ttu-id="87eda-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="87eda-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87eda-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87eda-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87eda-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="87eda-132">INPUTS</span></span>

### <span data-ttu-id="87eda-133">AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="87eda-133">AccessControlRecord</span></span>
<span data-ttu-id="87eda-134">Ez a parancsmag a **AccessControlRecord** -objektumot fogadja el.</span><span class="sxs-lookup"><span data-stu-id="87eda-134">This cmdlet accepts an **AccessControlRecord** object.</span></span>
<span data-ttu-id="87eda-135">A **AccessControlRecord** -objektumok az alábbi mezőket tartalmazzák:</span><span class="sxs-lookup"><span data-stu-id="87eda-135">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="87eda-136">**GlobalId** ( **karakterlánc** )</span><span class="sxs-lookup"><span data-stu-id="87eda-136">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="87eda-137">**InitiatorName** ( **karakterlánc** )</span><span class="sxs-lookup"><span data-stu-id="87eda-137">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="87eda-138">**InstanceId** ( **karakterlánc** )</span><span class="sxs-lookup"><span data-stu-id="87eda-138">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="87eda-139">**Name** ( **karakterlánc** )</span><span class="sxs-lookup"><span data-stu-id="87eda-139">**Name** ( **String** )</span></span> 
- <span data-ttu-id="87eda-140">**OperationInProgress** ( **OperationInProgress** )</span><span class="sxs-lookup"><span data-stu-id="87eda-140">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="87eda-141">**VolumeCount** ( **int** )</span><span class="sxs-lookup"><span data-stu-id="87eda-141">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="87eda-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="87eda-142">OUTPUTS</span></span>

### <span data-ttu-id="87eda-143">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="87eda-143">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="87eda-144">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="87eda-144">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="87eda-145">Ha nem adja meg ezt a paramétert, az eredmény egy **TaskResponse** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="87eda-145">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="87eda-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="87eda-146">NOTES</span></span>

## <span data-ttu-id="87eda-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="87eda-147">RELATED LINKS</span></span>

[<span data-ttu-id="87eda-148">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="87eda-148">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="87eda-149">Új – AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="87eda-149">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="87eda-150">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="87eda-150">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="87eda-151">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="87eda-151">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


