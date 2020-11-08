---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94016210"
---
# <span data-ttu-id="d7e0c-101">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="d7e0c-101">New-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="d7e0c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d7e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e0c-103">Access-vezérlő rekordot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-103">Creates an access control record.</span></span>

## <span data-ttu-id="d7e0c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d7e0c-104">SYNTAX</span></span>

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d7e0c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d7e0c-105">DESCRIPTION</span></span>
<span data-ttu-id="d7e0c-106">A **New-AzureStorSimpleAccessControlRecord** parancsmag létrehoz egy Access-vezérlő rekordot.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-106">The **New-AzureStorSimpleAccessControlRecord** cmdlet creates an access control record.</span></span>
<span data-ttu-id="d7e0c-107">A **AccessControlRecord** objektum segítségével konfigurálhatók a kötetek.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-107">You can use an **AccessControlRecord** object to configure volumes.</span></span>

## <span data-ttu-id="d7e0c-108">Példák</span><span class="sxs-lookup"><span data-stu-id="d7e0c-108">EXAMPLES</span></span>

### <span data-ttu-id="d7e0c-109">Példa 1: Access Controlaccess-vezérlő rekord létrehozása és várakozás a resultaccess vezérlőre</span><span class="sxs-lookup"><span data-stu-id="d7e0c-109">Example 1: Create an Access Controlaccess control record and wait for the resultaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

<span data-ttu-id="d7e0c-110">Ez a parancs létrehoz egy Acr10 nevű Access-vezérlő rekordot a Iqn10 nevű iSCSI-kezdeményezőhöz.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-110">This command creates an access control record named Acr10 for the iSCSI initiator named Iqn10.</span></span>
<span data-ttu-id="d7e0c-111">Ez a parancs a *WaitForComplete* paramétert adja meg, ezért a parancs mindaddig megvárja, amíg a művelet be nem fejeződik, majd egy **TaskStatusInfo** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-111">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="d7e0c-112">2. példa: Access-Controlaccess vezérlő recordaccess-vezérlő létrehozása</span><span class="sxs-lookup"><span data-stu-id="d7e0c-112">Example 2: Create an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

<span data-ttu-id="d7e0c-113">Ez a parancs létrehoz egy Acr11 nevű Access-vezérlő rekordot a Iqn11 nevű iSCSI-kezdeményezőhöz.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-113">This command creates an access control record named Acr11 for the iSCSI initiator named Iqn11.</span></span>
<span data-ttu-id="d7e0c-114">Ez a parancs nem adja meg a *WaitForComplete* paramétert, ezért a parancs elindítja a feladatot, majd egy **TaskResponse** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-114">This command does not specify the *WaitForComplete* parameter, and, therefore, the command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="d7e0c-115">A feladat állapotának megtekintéséhez használja a **Get-AzureStorSimpleTask** parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-115">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="d7e0c-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d7e0c-116">PARAMETERS</span></span>

### <span data-ttu-id="d7e0c-117">-ACRName</span><span class="sxs-lookup"><span data-stu-id="d7e0c-117">-ACRName</span></span>
<span data-ttu-id="d7e0c-118">Az Access-vezérlő rekord nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-118">Specifies a name for the access control record.</span></span>

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

### <span data-ttu-id="d7e0c-119">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="d7e0c-119">-IQNInitiatorName</span></span>
<span data-ttu-id="d7e0c-120">Megadja annak az iSCSI-kezdeményezőnek az iSCSI-minősített nevét (IQN), amelyhez ez a parancsmag hozzáférést biztosít a kötethez.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-120">Specifies the iSCSI qualified name (IQN) of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7e0c-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="d7e0c-121">-Profile</span></span>
<span data-ttu-id="d7e0c-122">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="d7e0c-123">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="d7e0c-123">-WaitForComplete</span></span>
<span data-ttu-id="d7e0c-124">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-124">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="d7e0c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e0c-125">CommonParameters</span></span>
<span data-ttu-id="d7e0c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d7e0c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e0c-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7e0c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e0c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7e0c-128">INPUTS</span></span>

### <span data-ttu-id="d7e0c-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="d7e0c-129">None</span></span>

## <span data-ttu-id="d7e0c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d7e0c-130">OUTPUTS</span></span>

### <span data-ttu-id="d7e0c-131">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="d7e0c-131">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="d7e0c-132">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-132">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="d7e0c-133">Ha nem adja meg ezt a paramétert, az eredmény egy **TaskResponse** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="d7e0c-133">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="d7e0c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d7e0c-134">NOTES</span></span>

## <span data-ttu-id="d7e0c-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d7e0c-135">RELATED LINKS</span></span>

[<span data-ttu-id="d7e0c-136">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="d7e0c-136">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="d7e0c-137">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="d7e0c-137">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="d7e0c-138">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="d7e0c-138">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="d7e0c-139">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="d7e0c-139">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


