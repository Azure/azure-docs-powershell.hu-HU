---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 0f8d9860f04112c197b91907a7622683069c3589
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94180761"
---
# <span data-ttu-id="bad05-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bad05-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="bad05-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bad05-102">SYNOPSIS</span></span>
<span data-ttu-id="bad05-103">Tárol egy tárolt hozzáférés-házirendet egy Azure Storage Queue-hoz.</span><span class="sxs-lookup"><span data-stu-id="bad05-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="bad05-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bad05-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bad05-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bad05-105">DESCRIPTION</span></span>
<span data-ttu-id="bad05-106">A **set-AzStorageQueueStoredAccessPolicy** parancsmag az Azure tárterület-várólistájának tárolt hozzáférési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="bad05-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="bad05-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bad05-107">EXAMPLES</span></span>

### <span data-ttu-id="bad05-108">1. példa: tárolt hozzáférési házirend beállítása a várólistában teljes hozzáféréssel</span><span class="sxs-lookup"><span data-stu-id="bad05-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="bad05-109">Ez a parancs a Policy07 nevű Access-házirendet állítja be a MyQueue nevű tárterület-várólistára.</span><span class="sxs-lookup"><span data-stu-id="bad05-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="bad05-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bad05-110">PARAMETERS</span></span>

### <span data-ttu-id="bad05-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="bad05-111">-Context</span></span>
<span data-ttu-id="bad05-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bad05-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bad05-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="bad05-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bad05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bad05-114">-DefaultProfile</span></span>
<span data-ttu-id="bad05-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bad05-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad05-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bad05-116">-ExpiryTime</span></span>
<span data-ttu-id="bad05-117">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="bad05-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad05-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="bad05-118">-NoExpiryTime</span></span>
<span data-ttu-id="bad05-119">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="bad05-119">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad05-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="bad05-120">-NoStartTime</span></span>
<span data-ttu-id="bad05-121">Jelzi, hogy ez a parancsmag a $Null kezdési időpontját állítja be.</span><span class="sxs-lookup"><span data-stu-id="bad05-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad05-122">– Engedély</span><span class="sxs-lookup"><span data-stu-id="bad05-122">-Permission</span></span>
<span data-ttu-id="bad05-123">A tárolt elérési házirend engedélyeinek megadása a tárolási várólista eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="bad05-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="bad05-124">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="bad05-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad05-125">-Házirend</span><span class="sxs-lookup"><span data-stu-id="bad05-125">-Policy</span></span>
<span data-ttu-id="bad05-126">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bad05-126">Specifies the name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad05-127">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="bad05-127">-Queue</span></span>
<span data-ttu-id="bad05-128">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="bad05-128">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bad05-129">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="bad05-129">-StartTime</span></span>
<span data-ttu-id="bad05-130">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="bad05-130">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad05-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bad05-131">-Confirm</span></span>
<span data-ttu-id="bad05-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bad05-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad05-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bad05-133">-WhatIf</span></span>
<span data-ttu-id="bad05-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bad05-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bad05-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bad05-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bad05-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad05-136">CommonParameters</span></span>
<span data-ttu-id="bad05-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bad05-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bad05-138">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bad05-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad05-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bad05-139">INPUTS</span></span>

### <span data-ttu-id="bad05-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bad05-140">System.String</span></span>

### <span data-ttu-id="bad05-141">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bad05-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="bad05-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bad05-142">OUTPUTS</span></span>

### <span data-ttu-id="bad05-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bad05-143">System.String</span></span>

## <span data-ttu-id="bad05-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bad05-144">NOTES</span></span>

## <span data-ttu-id="bad05-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bad05-145">RELATED LINKS</span></span>

[<span data-ttu-id="bad05-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bad05-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="bad05-147">Új – AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bad05-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="bad05-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bad05-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
