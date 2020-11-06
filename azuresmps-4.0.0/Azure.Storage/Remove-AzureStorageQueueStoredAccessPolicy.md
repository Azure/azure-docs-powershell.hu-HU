---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
ms.openlocfilehash: 116dcc8967ab18d0b67cd3e4eeea91190c38930f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491672"
---
# <span data-ttu-id="a7a22-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a7a22-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="a7a22-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a7a22-102">SYNOPSIS</span></span>
<span data-ttu-id="a7a22-103">Egy tárolt Access-házirend eltávolítása egy Azure-tárterület-várólistából.</span><span class="sxs-lookup"><span data-stu-id="a7a22-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="a7a22-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a7a22-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7a22-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a7a22-105">DESCRIPTION</span></span>
<span data-ttu-id="a7a22-106">A **Remove-AzureStorageQueueStoredAccessPolicy** parancsmag az Azure tárterület-várólistából távolítja el a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="a7a22-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="a7a22-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a7a22-107">EXAMPLES</span></span>

### <span data-ttu-id="a7a22-108">1. példa: tárolt hozzáférési házirend eltávolítása a tárolási várólistából</span><span class="sxs-lookup"><span data-stu-id="a7a22-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="a7a22-109">Ez a parancs eltávolítja a Policy04 nevű Access-házirendet a MyQueue nevű tárterület-várólistából.</span><span class="sxs-lookup"><span data-stu-id="a7a22-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="a7a22-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a7a22-110">PARAMETERS</span></span>

### <span data-ttu-id="a7a22-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a7a22-111">-Context</span></span>
<span data-ttu-id="a7a22-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7a22-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a7a22-113">A tárolási környezet eléréséhez használja az New-AzureStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="a7a22-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a7a22-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7a22-114">-PassThru</span></span>
<span data-ttu-id="a7a22-115">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="a7a22-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a7a22-116">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="a7a22-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a7a22-117">-Házirend</span><span class="sxs-lookup"><span data-stu-id="a7a22-117">-Policy</span></span>
<span data-ttu-id="a7a22-118">A tárolt elérési házirendet adja meg, amely tartalmazza az ehhez a megosztott hozzáférés-aláírási tokenhez tartozó engedélyeket.</span><span class="sxs-lookup"><span data-stu-id="a7a22-118">Specifies the stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="a7a22-119">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="a7a22-119">-Queue</span></span>
<span data-ttu-id="a7a22-120">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="a7a22-120">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="a7a22-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="a7a22-121">-Confirm</span></span>
<span data-ttu-id="a7a22-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="a7a22-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7a22-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7a22-123">-WhatIf</span></span>
<span data-ttu-id="a7a22-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="a7a22-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7a22-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="a7a22-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7a22-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7a22-126">CommonParameters</span></span>
<span data-ttu-id="a7a22-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a7a22-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7a22-128">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7a22-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7a22-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7a22-129">INPUTS</span></span>

## <span data-ttu-id="a7a22-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a7a22-130">OUTPUTS</span></span>

## <span data-ttu-id="a7a22-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a7a22-131">NOTES</span></span>

## <span data-ttu-id="a7a22-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a7a22-132">RELATED LINKS</span></span>

[<span data-ttu-id="a7a22-133">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a7a22-133">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a7a22-134">Új – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a7a22-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a7a22-135">Új – AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a7a22-135">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a7a22-136">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a7a22-136">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
