---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 94c5bc28ae381227366b5461b51a2da7fd6feccd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498119"
---
# <span data-ttu-id="1a17e-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1a17e-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="1a17e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1a17e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a17e-103">Egy tárolt Access-házirend eltávolítása egy Azure-tárterület-várólistából.</span><span class="sxs-lookup"><span data-stu-id="1a17e-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a17e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1a17e-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a17e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1a17e-105">DESCRIPTION</span></span>
<span data-ttu-id="1a17e-106">A **Remove-AzureStorageQueueStoredAccessPolicy** parancsmag az Azure tárterület-várólistából távolítja el a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="1a17e-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="1a17e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1a17e-107">EXAMPLES</span></span>

### <span data-ttu-id="1a17e-108">1. példa: tárolt hozzáférési házirend eltávolítása a tárolási várólistából</span><span class="sxs-lookup"><span data-stu-id="1a17e-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="1a17e-109">Ez a parancs eltávolítja a Policy04 nevű Access-házirendet a MyQueue nevű tárterület-várólistából.</span><span class="sxs-lookup"><span data-stu-id="1a17e-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="1a17e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1a17e-110">PARAMETERS</span></span>

### <span data-ttu-id="1a17e-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1a17e-111">-Context</span></span>
<span data-ttu-id="1a17e-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a17e-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1a17e-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="1a17e-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1a17e-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a17e-114">-PassThru</span></span>
<span data-ttu-id="1a17e-115">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="1a17e-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1a17e-116">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="1a17e-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1a17e-117">-Házirend</span><span class="sxs-lookup"><span data-stu-id="1a17e-117">-Policy</span></span>
<span data-ttu-id="1a17e-118">Annak a tárolt hozzáférési házirendnek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="1a17e-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a17e-119">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="1a17e-119">-Queue</span></span>
<span data-ttu-id="1a17e-120">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="1a17e-120">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a17e-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1a17e-121">-Confirm</span></span>
<span data-ttu-id="1a17e-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1a17e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a17e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a17e-123">-WhatIf</span></span>
<span data-ttu-id="1a17e-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1a17e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a17e-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1a17e-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a17e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a17e-126">CommonParameters</span></span>
<span data-ttu-id="1a17e-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1a17e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a17e-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a17e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a17e-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a17e-129">INPUTS</span></span>

### <span data-ttu-id="1a17e-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a17e-130">IStorageContext</span></span>

<span data-ttu-id="1a17e-131">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1a17e-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="1a17e-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1a17e-132">OUTPUTS</span></span>

### <span data-ttu-id="1a17e-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1a17e-133">System.Boolean</span></span>

## <span data-ttu-id="1a17e-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1a17e-134">NOTES</span></span>

## <span data-ttu-id="1a17e-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1a17e-135">RELATED LINKS</span></span>

[<span data-ttu-id="1a17e-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1a17e-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1a17e-137">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1a17e-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1a17e-138">Új – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1a17e-138">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="1a17e-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1a17e-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
