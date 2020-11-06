---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: e20caedc23dcd4d06336f3dddf80fdaf4a84cbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498596"
---
# <span data-ttu-id="7473e-101">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7473e-101">Set-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="7473e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7473e-102">SYNOPSIS</span></span>
<span data-ttu-id="7473e-103">Tárol egy tárolt hozzáférés-házirendet egy Azure Storage Queue-hoz.</span><span class="sxs-lookup"><span data-stu-id="7473e-103">Sets a stored access policy for an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7473e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7473e-104">SYNTAX</span></span>

```
Set-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7473e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7473e-105">DESCRIPTION</span></span>
<span data-ttu-id="7473e-106">A **set-AzureStorageQueueStoredAccessPolicy** parancsmag az Azure tárterület-várólistájának tárolt hozzáférési házirendjét állítja be.</span><span class="sxs-lookup"><span data-stu-id="7473e-106">The **Set-AzureStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="7473e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7473e-107">EXAMPLES</span></span>

### <span data-ttu-id="7473e-108">1. példa: tárolt hozzáférési házirend beállítása a várólistában teljes hozzáféréssel</span><span class="sxs-lookup"><span data-stu-id="7473e-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="7473e-109">Ez a parancs a Policy07 nevű Access-házirendet állítja be a MyQueue nevű tárterület-várólistára.</span><span class="sxs-lookup"><span data-stu-id="7473e-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="7473e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7473e-110">PARAMETERS</span></span>

### <span data-ttu-id="7473e-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="7473e-111">-Context</span></span>
<span data-ttu-id="7473e-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7473e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7473e-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="7473e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7473e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7473e-114">-DefaultProfile</span></span>
<span data-ttu-id="7473e-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7473e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7473e-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7473e-116">-ExpiryTime</span></span>
<span data-ttu-id="7473e-117">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="7473e-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="7473e-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="7473e-118">-NoExpiryTime</span></span>
<span data-ttu-id="7473e-119">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="7473e-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="7473e-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="7473e-120">-NoStartTime</span></span>
<span data-ttu-id="7473e-121">Jelzi, hogy ez a parancsmag a $Null kezdési időpontját állítja be.</span><span class="sxs-lookup"><span data-stu-id="7473e-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="7473e-122">– Engedély</span><span class="sxs-lookup"><span data-stu-id="7473e-122">-Permission</span></span>
<span data-ttu-id="7473e-123">A tárolt elérési házirend engedélyeinek megadása a tárolási várólista eléréséhez.</span><span class="sxs-lookup"><span data-stu-id="7473e-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="7473e-124">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (olvasásra, írásra és törlésre).</span><span class="sxs-lookup"><span data-stu-id="7473e-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="7473e-125">-Házirend</span><span class="sxs-lookup"><span data-stu-id="7473e-125">-Policy</span></span>
<span data-ttu-id="7473e-126">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7473e-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="7473e-127">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="7473e-127">-Queue</span></span>
<span data-ttu-id="7473e-128">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="7473e-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="7473e-129">-Kezdő időpont</span><span class="sxs-lookup"><span data-stu-id="7473e-129">-StartTime</span></span>
<span data-ttu-id="7473e-130">Azt az időpontot adja meg, amikor a tárolt hozzáférési házirend érvényes lesz.</span><span class="sxs-lookup"><span data-stu-id="7473e-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="7473e-131">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="7473e-131">-Confirm</span></span>
<span data-ttu-id="7473e-132">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="7473e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7473e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7473e-133">-WhatIf</span></span>
<span data-ttu-id="7473e-134">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="7473e-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7473e-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="7473e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7473e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7473e-136">CommonParameters</span></span>
<span data-ttu-id="7473e-137">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7473e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7473e-138">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7473e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7473e-139">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7473e-139">INPUTS</span></span>

### <span data-ttu-id="7473e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7473e-140">System.String</span></span>

### <span data-ttu-id="7473e-141">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7473e-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7473e-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7473e-142">OUTPUTS</span></span>

### <span data-ttu-id="7473e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7473e-143">System.String</span></span>

## <span data-ttu-id="7473e-144">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7473e-144">NOTES</span></span>

## <span data-ttu-id="7473e-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7473e-145">RELATED LINKS</span></span>

[<span data-ttu-id="7473e-146">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7473e-146">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="7473e-147">Új – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7473e-147">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="7473e-148">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7473e-148">Remove-AzureStorageQueueStoredAccessPolicy</span></span>](./Remove-AzureStorageQueueStoredAccessPolicy.md)
