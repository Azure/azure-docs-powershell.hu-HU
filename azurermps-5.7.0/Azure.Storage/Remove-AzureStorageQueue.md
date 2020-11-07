---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
ms.openlocfilehash: b98b0ef6e8c4d47c32cab4ee891041e0820ea3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679010"
---
# <span data-ttu-id="e153b-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="e153b-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="e153b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e153b-102">SYNOPSIS</span></span>
<span data-ttu-id="e153b-103">Tároló-várólista eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e153b-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e153b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e153b-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e153b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e153b-105">DESCRIPTION</span></span>
<span data-ttu-id="e153b-106">A **Remove-AzureStorageQueue** parancsmag eltávolítja a tárolási várólistát.</span><span class="sxs-lookup"><span data-stu-id="e153b-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="e153b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e153b-107">EXAMPLES</span></span>

### <span data-ttu-id="e153b-108">1. példa: tárterület-várólista eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="e153b-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="e153b-109">Ez a parancs eltávolítja a ContosoQueue01 nevű várólistát.</span><span class="sxs-lookup"><span data-stu-id="e153b-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="e153b-110">2. példa: több tárolási várólista eltávolítása</span><span class="sxs-lookup"><span data-stu-id="e153b-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="e153b-111">Ez a parancs eltávolítja az összes olyan várólistát, amelyen a contoso kezdetű nevek szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="e153b-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="e153b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e153b-112">PARAMETERS</span></span>

### <span data-ttu-id="e153b-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="e153b-113">-Context</span></span>
<span data-ttu-id="e153b-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e153b-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="e153b-115">A tárolási környezet (New-AzureStorageContext parancsmag) beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="e153b-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="e153b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e153b-116">-Force</span></span>
<span data-ttu-id="e153b-117">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="e153b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e153b-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e153b-118">-Name</span></span>
<span data-ttu-id="e153b-119">Az eltávolítandó várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e153b-119">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="e153b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e153b-120">-PassThru</span></span>
<span data-ttu-id="e153b-121">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="e153b-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="e153b-122">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="e153b-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="e153b-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="e153b-123">-Confirm</span></span>
<span data-ttu-id="e153b-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="e153b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e153b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e153b-125">-WhatIf</span></span>
<span data-ttu-id="e153b-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="e153b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e153b-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e153b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e153b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e153b-128">CommonParameters</span></span>
<span data-ttu-id="e153b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e153b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e153b-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e153b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e153b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e153b-131">INPUTS</span></span>

### <span data-ttu-id="e153b-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e153b-132">IStorageContext</span></span>

<span data-ttu-id="e153b-133">A "környezet" paraméter elfogadja a "IStorageContext" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e153b-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e153b-134">Karakterlánc</span><span class="sxs-lookup"><span data-stu-id="e153b-134">String</span></span>

<span data-ttu-id="e153b-135">A "név" paraméter elfogadja a "string" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e153b-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e153b-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e153b-136">OUTPUTS</span></span>

### <span data-ttu-id="e153b-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e153b-137">System.Boolean</span></span>

## <span data-ttu-id="e153b-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e153b-138">NOTES</span></span>

## <span data-ttu-id="e153b-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e153b-139">RELATED LINKS</span></span>

[<span data-ttu-id="e153b-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="e153b-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="e153b-141">Új – AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="e153b-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
