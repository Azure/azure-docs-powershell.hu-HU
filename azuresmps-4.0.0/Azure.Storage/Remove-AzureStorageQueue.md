---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54770fd564addf30e7c4ed058776857b823903e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491675"
---
# <span data-ttu-id="1ca8a-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="1ca8a-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="1ca8a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ca8a-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca8a-103">Tároló-várólista eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-103">Removes a storage queue.</span></span>

## <span data-ttu-id="1ca8a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ca8a-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ca8a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ca8a-105">DESCRIPTION</span></span>
<span data-ttu-id="1ca8a-106">A **Remove-AzureStorageQueue** parancsmag eltávolítja a tárolási várólistát.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="1ca8a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1ca8a-107">EXAMPLES</span></span>

### <span data-ttu-id="1ca8a-108">1. példa: tárterület-várólista eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="1ca8a-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="1ca8a-109">Ez a parancs eltávolítja a ContosoQueue01 nevű várólistát.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="1ca8a-110">2. példa: több tárolási várólista eltávolítása</span><span class="sxs-lookup"><span data-stu-id="1ca8a-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="1ca8a-111">Ez a parancs eltávolítja az összes olyan várólistát, amelyen a contoso kezdetű nevek szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="1ca8a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ca8a-112">PARAMETERS</span></span>

### <span data-ttu-id="1ca8a-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1ca8a-113">-Context</span></span>
<span data-ttu-id="1ca8a-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="1ca8a-115">A tárolási környezet (New-AzureStorageContext parancsmag) beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1ca8a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1ca8a-116">-Force</span></span>
<span data-ttu-id="1ca8a-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ca8a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1ca8a-118">-Name</span></span>
<span data-ttu-id="1ca8a-119">Az eltávolítandó várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-119">Specifies the name of the queue to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ca8a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ca8a-120">-PassThru</span></span>
<span data-ttu-id="1ca8a-121">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1ca8a-122">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1ca8a-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="1ca8a-123">-Confirm</span></span>
<span data-ttu-id="1ca8a-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ca8a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ca8a-125">-WhatIf</span></span>
<span data-ttu-id="1ca8a-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ca8a-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="1ca8a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ca8a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca8a-128">CommonParameters</span></span>
<span data-ttu-id="1ca8a-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ca8a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca8a-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ca8a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca8a-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ca8a-131">INPUTS</span></span>

## <span data-ttu-id="1ca8a-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ca8a-132">OUTPUTS</span></span>

## <span data-ttu-id="1ca8a-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ca8a-133">NOTES</span></span>

## <span data-ttu-id="1ca8a-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ca8a-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ca8a-135">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="1ca8a-135">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="1ca8a-136">Új – AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="1ca8a-136">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
