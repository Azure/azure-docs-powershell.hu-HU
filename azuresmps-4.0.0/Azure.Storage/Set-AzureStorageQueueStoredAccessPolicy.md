---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: ''
schema: 2.0.0
ms.openlocfilehash: b273dbec3fda421574c8866a10eda0a8098513ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491783"
---
# <span data-ttu-id="a0de0-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0de0-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="a0de0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a0de0-102">SYNOPSIS</span></span>
<span data-ttu-id="a0de0-103">Tárol egy tárolt hozzáférés-házirendet egy Azure Storage Queue-hoz.</span><span class="sxs-lookup"><span data-stu-id="a0de0-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="a0de0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a0de0-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0de0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a0de0-105">DESCRIPTION</span></span>
<span data-ttu-id="a0de0-106">A **set-AzureStorageQueueStoredAccessPolicy** parancsmag az Azure tárterület-várólistájának tárolt hozzáférési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="a0de0-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="a0de0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a0de0-107">EXAMPLES</span></span>

### <span data-ttu-id="a0de0-108">1. példa: tárolt hozzáférés-házirend beállítása a várólistán</span><span class="sxs-lookup"><span data-stu-id="a0de0-108">Example 1: Set a stored access policy in the queue</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07"
```

<span data-ttu-id="a0de0-109">Ez a parancs a Policy07 nevű Access-házirendet állítja be a MyQueue nevű tárterület-várólistára.</span><span class="sxs-lookup"><span data-stu-id="a0de0-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="a0de0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a0de0-110">PARAMETERS</span></span>

### <span data-ttu-id="a0de0-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a0de0-111">-Context</span></span>
<span data-ttu-id="a0de0-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0de0-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a0de0-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a0de0-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a0de0-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a0de0-114">-ExpiryTime</span></span>
<span data-ttu-id="a0de0-115">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="a0de0-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="a0de0-116">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a0de0-116">-NoExpiryTime</span></span>
<span data-ttu-id="a0de0-117">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="a0de0-117">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="a0de0-118">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="a0de0-118">-NoStartTime</span></span>
<span data-ttu-id="a0de0-119">Jelzi, hogy ez a parancsmag a $Null kezdési időpontját állítja be.</span><span class="sxs-lookup"><span data-stu-id="a0de0-119">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="a0de0-120">– Engedély</span><span class="sxs-lookup"><span data-stu-id="a0de0-120">-Permission</span></span>
<span data-ttu-id="a0de0-121">A tárterület-várólistához való nyilvános hozzáférés szintjét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0de0-121">Specifies the level of public access to this storage queue.</span></span>

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

### <span data-ttu-id="a0de0-122">-Házirend</span><span class="sxs-lookup"><span data-stu-id="a0de0-122">-Policy</span></span>
<span data-ttu-id="a0de0-123">A tárolt hozzáférési házirendet adja meg, amely tartalmazza az e SAS-jogkivonat engedélyeit.</span><span class="sxs-lookup"><span data-stu-id="a0de0-123">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="a0de0-124">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="a0de0-124">-Queue</span></span>
<span data-ttu-id="a0de0-125">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a0de0-125">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="a0de0-126">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="a0de0-126">-StartTime</span></span>
<span data-ttu-id="a0de0-127">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="a0de0-127">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="a0de0-128">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a0de0-128">-Confirm</span></span>
<span data-ttu-id="a0de0-129">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a0de0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0de0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0de0-130">-WhatIf</span></span>
<span data-ttu-id="a0de0-131">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a0de0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0de0-132">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a0de0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0de0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0de0-133">CommonParameters</span></span>
<span data-ttu-id="a0de0-134">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a0de0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0de0-135">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0de0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0de0-136">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0de0-136">INPUTS</span></span>

## <span data-ttu-id="a0de0-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a0de0-137">OUTPUTS</span></span>

## <span data-ttu-id="a0de0-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a0de0-138">NOTES</span></span>

## <span data-ttu-id="a0de0-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a0de0-139">RELATED LINKS</span></span>

[<span data-ttu-id="a0de0-140">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0de0-140">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a0de0-141">Új – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0de0-141">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a0de0-142">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0de0-142">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
