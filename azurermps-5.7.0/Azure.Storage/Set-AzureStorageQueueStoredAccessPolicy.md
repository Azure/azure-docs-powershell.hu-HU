---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 9a3a19b2e0773d1513ce57dc5fe7ca7502bb325d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93680843"
---
# <span data-ttu-id="3784f-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3784f-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="3784f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3784f-102">SYNOPSIS</span></span>
<span data-ttu-id="3784f-103">Tárol egy tárolt hozzáférés-házirendet egy Azure Storage Queue-hoz.</span><span class="sxs-lookup"><span data-stu-id="3784f-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3784f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3784f-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3784f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3784f-105">DESCRIPTION</span></span>
<span data-ttu-id="3784f-106">A **set-AzureStorageQueueStoredAccessPolicy** parancsmag az Azure tárterület-várólistájának tárolt hozzáférési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="3784f-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="3784f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="3784f-107">EXAMPLES</span></span>

### <span data-ttu-id="3784f-108">1. példa: tárolt hozzáférési házirend beállítása a várólistában teljes hozzáféréssel</span><span class="sxs-lookup"><span data-stu-id="3784f-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="3784f-109">Ez a parancs a Policy07 nevű Access-házirendet állítja be a MyQueue nevű tárterület-várólistára.</span><span class="sxs-lookup"><span data-stu-id="3784f-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="3784f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3784f-110">PARAMETERS</span></span>

### <span data-ttu-id="3784f-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="3784f-111">-Context</span></span>
<span data-ttu-id="3784f-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3784f-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3784f-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="3784f-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3784f-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3784f-114">-ExpiryTime</span></span>
<span data-ttu-id="3784f-115">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="3784f-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3784f-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3784f-116">-NoExpiryTime</span></span>
<span data-ttu-id="3784f-117">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="3784f-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="3784f-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="3784f-118">-NoStartTime</span></span>
<span data-ttu-id="3784f-119">Jelzi, hogy ez a parancsmag a $Null kezdési időpontját állítja be.</span><span class="sxs-lookup"><span data-stu-id="3784f-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="3784f-120">– Engedély</span><span class="sxs-lookup"><span data-stu-id="3784f-120">-Permission</span></span>
<span data-ttu-id="3784f-121">A tárolt elérési házirend engedélyeinek megadása a tárolási várólista eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="3784f-121">Specifies permissions in the stored access policy to access the storage queue.</span></span>

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

### <span data-ttu-id="3784f-122">-Házirend</span><span class="sxs-lookup"><span data-stu-id="3784f-122">-Policy</span></span>
<span data-ttu-id="3784f-123">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3784f-123">Specifies the name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3784f-124">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="3784f-124">-Queue</span></span>
<span data-ttu-id="3784f-125">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="3784f-125">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3784f-126">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="3784f-126">-StartTime</span></span>
<span data-ttu-id="3784f-127">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="3784f-127">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3784f-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3784f-128">-Confirm</span></span>
<span data-ttu-id="3784f-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3784f-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3784f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3784f-130">-WhatIf</span></span>
<span data-ttu-id="3784f-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3784f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3784f-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3784f-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3784f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3784f-133">CommonParameters</span></span>
<span data-ttu-id="3784f-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3784f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3784f-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3784f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3784f-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3784f-136">INPUTS</span></span>

### <span data-ttu-id="3784f-137">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3784f-137">IStorageContext</span></span>

<span data-ttu-id="3784f-138">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3784f-138">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="3784f-139">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="3784f-139">String</span></span>

<span data-ttu-id="3784f-140">A "várólista" paraméter a folyamat "string" típusú értékét fogadja el.</span><span class="sxs-lookup"><span data-stu-id="3784f-140">Parameter 'Queue' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="3784f-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3784f-141">OUTPUTS</span></span>

### <span data-ttu-id="3784f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3784f-142">System.String</span></span>

## <span data-ttu-id="3784f-143">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3784f-143">NOTES</span></span>

## <span data-ttu-id="3784f-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3784f-144">RELATED LINKS</span></span>

[<span data-ttu-id="3784f-145">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3784f-145">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3784f-146">Új – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3784f-146">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="3784f-147">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3784f-147">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
