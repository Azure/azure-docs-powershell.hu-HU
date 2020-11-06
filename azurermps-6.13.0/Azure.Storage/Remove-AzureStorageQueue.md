---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
ms.openlocfilehash: 544d019547616ab7fc37804e150115eacc8a0224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492933"
---
# <span data-ttu-id="4d422-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4d422-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="4d422-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d422-102">SYNOPSIS</span></span>
<span data-ttu-id="4d422-103">Tároló-várólista eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="4d422-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d422-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d422-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d422-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d422-105">DESCRIPTION</span></span>
<span data-ttu-id="4d422-106">A **Remove-AzureStorageQueue** parancsmag eltávolítja a tárolási várólistát.</span><span class="sxs-lookup"><span data-stu-id="4d422-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="4d422-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4d422-107">EXAMPLES</span></span>

### <span data-ttu-id="4d422-108">1. példa: tárterület-várólista eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="4d422-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="4d422-109">Ez a parancs eltávolítja a ContosoQueue01 nevű várólistát.</span><span class="sxs-lookup"><span data-stu-id="4d422-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="4d422-110">2. példa: több tárolási várólista eltávolítása</span><span class="sxs-lookup"><span data-stu-id="4d422-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="4d422-111">Ez a parancs eltávolítja az összes olyan várólistát, amelyen a contoso kezdetű nevek szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="4d422-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="4d422-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d422-112">PARAMETERS</span></span>

### <span data-ttu-id="4d422-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4d422-113">-Context</span></span>
<span data-ttu-id="4d422-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d422-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="4d422-115">A tárolási környezet (New-AzureStorageContext parancsmag) beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="4d422-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4d422-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d422-116">-DefaultProfile</span></span>
<span data-ttu-id="4d422-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d422-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d422-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4d422-118">-Force</span></span>
<span data-ttu-id="4d422-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="4d422-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d422-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d422-120">-Name</span></span>
<span data-ttu-id="4d422-121">Az eltávolítandó várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d422-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d422-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4d422-122">-PassThru</span></span>
<span data-ttu-id="4d422-123">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="4d422-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4d422-124">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="4d422-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4d422-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4d422-125">-Confirm</span></span>
<span data-ttu-id="4d422-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4d422-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d422-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d422-127">-WhatIf</span></span>
<span data-ttu-id="4d422-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4d422-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d422-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4d422-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d422-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d422-130">CommonParameters</span></span>
<span data-ttu-id="4d422-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d422-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d422-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d422-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d422-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d422-133">INPUTS</span></span>

### <span data-ttu-id="4d422-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4d422-134">System.String</span></span>

### <span data-ttu-id="4d422-135">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4d422-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4d422-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d422-136">OUTPUTS</span></span>

### <span data-ttu-id="4d422-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d422-137">System.Boolean</span></span>

## <span data-ttu-id="4d422-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d422-138">NOTES</span></span>

## <span data-ttu-id="4d422-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d422-139">RELATED LINKS</span></span>

[<span data-ttu-id="4d422-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4d422-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="4d422-141">Új – AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="4d422-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
