---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71CFCA9D-198E-481A-BB85-159477F25322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c050ea91cc85a89702fb6cf62f05779db7155e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94015858"
---
# <span data-ttu-id="ec968-101">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ec968-101">Set-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="ec968-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec968-102">SYNOPSIS</span></span>
<span data-ttu-id="ec968-103">Frissíti a IQN-rekordokat.</span><span class="sxs-lookup"><span data-stu-id="ec968-103">Updates the IQN of an access control record.</span></span>

## <span data-ttu-id="ec968-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec968-104">SYNTAX</span></span>

```
Set-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ec968-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec968-105">DESCRIPTION</span></span>
<span data-ttu-id="ec968-106">A **set-AzureStorSimpleAccessControlRecord** parancsmag frissíti egy meglévő hozzáférés-vezérlési rekord iSCSI-minősített nevét (IQN).</span><span class="sxs-lookup"><span data-stu-id="ec968-106">The **Set-AzureStorSimpleAccessControlRecord** cmdlet updates the iSCSI qualified name (IQN) of an existing access control record.</span></span>

## <span data-ttu-id="ec968-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ec968-107">EXAMPLES</span></span>

### <span data-ttu-id="ec968-108">Példa 1: hozzáférés-vezérlési rekord frissítése</span><span class="sxs-lookup"><span data-stu-id="ec968-108">Example 1: Update an access control record</span></span>
```
PS C:\>Set-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "IqnUpdated" -WaitForComplete
VERBOSE: ClientRequestId: e4766335-f302-40e0-93bf-fad7aa488ae6_PS
VERBOSE: ClientRequestId: cfdbbd67-6ba5-4238-b743-b88f604079b9_PS
VERBOSE: About to run a task to update your Access Control Record! 
VERBOSE: ClientRequestId: d5cf2793-0ab5-40ff-ab6f-43e21bc4c0a4_PS


JobId        : 89502523-52fc-4ce2-b2d4-cb8c6692fb60
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: cbd47519-3a3c-4365-b097-0fb7551c48ee_PS
GlobalId            : 
InitiatorName       : IqnUpdated
InstanceId          : 9bcfbc83-e196-4688-9016-827f51515c24
Name                : Acr10
OperationInProgress : None
VolumeCount         : 0
```

<span data-ttu-id="ec968-109">Ez a parancs frissíti a IqnUpdated nevű iSCSI-kezdeményező Acr10 nevű hozzáférés-vezérlési rekordját.</span><span class="sxs-lookup"><span data-stu-id="ec968-109">This command updates the access control record named Acr10 for the iSCSI initiator named IqnUpdated.</span></span>
<span data-ttu-id="ec968-110">Ez a parancs a *WaitForComplete* paramétert adja meg, ezért a parancs mindaddig megvárja, amíg a művelet be nem fejeződik, majd egy **TaskStatusInfo** objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="ec968-110">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="ec968-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec968-111">PARAMETERS</span></span>

### <span data-ttu-id="ec968-112">-ACRName</span><span class="sxs-lookup"><span data-stu-id="ec968-112">-ACRName</span></span>
<span data-ttu-id="ec968-113">A módosítandó hozzáférés-vezérlési rekord nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec968-113">Specifies a name of the access control record to modify.</span></span>

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

### <span data-ttu-id="ec968-114">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="ec968-114">-IQNInitiatorName</span></span>
<span data-ttu-id="ec968-115">Annak az iSCSI-kezdeményezőnek a IQN adja meg, amelyhez ez a parancsmag hozzáférést biztosít a kötethez.</span><span class="sxs-lookup"><span data-stu-id="ec968-115">Specifies the IQN of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

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

### <span data-ttu-id="ec968-116">-NewName</span><span class="sxs-lookup"><span data-stu-id="ec968-116">-NewName</span></span>
<span data-ttu-id="ec968-117">Új név megadása a hozzáférés-vezérlési rekordhoz.</span><span class="sxs-lookup"><span data-stu-id="ec968-117">Specifies a new name for access control record.</span></span>

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

### <span data-ttu-id="ec968-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="ec968-118">-Profile</span></span>
<span data-ttu-id="ec968-119">Egy Azure-profilt ad meg.</span><span class="sxs-lookup"><span data-stu-id="ec968-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ec968-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="ec968-120">-WaitForComplete</span></span>
<span data-ttu-id="ec968-121">Azt jelzi, hogy ez a parancsmag a művelet befejezését várja, mielőtt a vezérlőt visszaadja a Windows PowerShell-konzolnak.</span><span class="sxs-lookup"><span data-stu-id="ec968-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="ec968-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec968-122">CommonParameters</span></span>
<span data-ttu-id="ec968-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec968-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec968-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec968-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec968-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec968-125">INPUTS</span></span>

### <span data-ttu-id="ec968-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="ec968-126">None</span></span>

## <span data-ttu-id="ec968-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec968-127">OUTPUTS</span></span>

### <span data-ttu-id="ec968-128">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="ec968-128">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="ec968-129">Ez a parancsmag **TaskStatusInfo** -objektumot ad eredményül, ha a *WaitForComplete* paramétert adja meg.</span><span class="sxs-lookup"><span data-stu-id="ec968-129">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="ec968-130">Ha nem adja meg ezt a paramétert, az eredmény egy **TaskResponse** -objektumot ad eredményül.</span><span class="sxs-lookup"><span data-stu-id="ec968-130">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="ec968-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec968-131">NOTES</span></span>

## <span data-ttu-id="ec968-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec968-132">RELATED LINKS</span></span>

[<span data-ttu-id="ec968-133">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ec968-133">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="ec968-134">Új – AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ec968-134">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="ec968-135">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="ec968-135">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)


