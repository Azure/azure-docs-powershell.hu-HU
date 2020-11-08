---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2cc10a1b72dc369aef08b84e7b8fe2128ff0ac33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182057"
---
# <span data-ttu-id="6515d-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="6515d-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="6515d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6515d-102">SYNOPSIS</span></span>
<span data-ttu-id="6515d-103">Tároló-várólista eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="6515d-103">Removes a storage queue.</span></span>

## <span data-ttu-id="6515d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6515d-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6515d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6515d-105">DESCRIPTION</span></span>
<span data-ttu-id="6515d-106">A **Remove-AzStorageQueue** parancsmag eltávolítja a tárolási várólistát.</span><span class="sxs-lookup"><span data-stu-id="6515d-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="6515d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="6515d-107">EXAMPLES</span></span>

### <span data-ttu-id="6515d-108">1. példa: tárterület-várólista eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="6515d-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="6515d-109">Ez a parancs eltávolítja a ContosoQueue01 nevű várólistát.</span><span class="sxs-lookup"><span data-stu-id="6515d-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="6515d-110">2. példa: több tárolási várólista eltávolítása</span><span class="sxs-lookup"><span data-stu-id="6515d-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="6515d-111">Ez a parancs eltávolítja az összes olyan várólistát, amelyen a contoso kezdetű nevek szerepelnek.</span><span class="sxs-lookup"><span data-stu-id="6515d-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="6515d-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6515d-112">PARAMETERS</span></span>

### <span data-ttu-id="6515d-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="6515d-113">-Context</span></span>
<span data-ttu-id="6515d-114">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6515d-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6515d-115">A tárolási környezet (New-AzStorageContext parancsmag) beolvasásához.</span><span class="sxs-lookup"><span data-stu-id="6515d-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6515d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6515d-116">-DefaultProfile</span></span>
<span data-ttu-id="6515d-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6515d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6515d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6515d-118">-Force</span></span>
<span data-ttu-id="6515d-119">Kényszeríti a parancsot, hogy a felhasználó megerősítésének kérése nélkül fusson.</span><span class="sxs-lookup"><span data-stu-id="6515d-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6515d-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6515d-120">-Name</span></span>
<span data-ttu-id="6515d-121">Az eltávolítandó várólista nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="6515d-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="6515d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6515d-122">-PassThru</span></span>
<span data-ttu-id="6515d-123">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="6515d-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6515d-124">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="6515d-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6515d-125">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="6515d-125">-Confirm</span></span>
<span data-ttu-id="6515d-126">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="6515d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6515d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6515d-127">-WhatIf</span></span>
<span data-ttu-id="6515d-128">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="6515d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6515d-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="6515d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6515d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6515d-130">CommonParameters</span></span>
<span data-ttu-id="6515d-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6515d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6515d-132">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6515d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6515d-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6515d-133">INPUTS</span></span>

### <span data-ttu-id="6515d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6515d-134">System.String</span></span>

### <span data-ttu-id="6515d-135">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6515d-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6515d-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6515d-136">OUTPUTS</span></span>

### <span data-ttu-id="6515d-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6515d-137">System.Boolean</span></span>

## <span data-ttu-id="6515d-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6515d-138">NOTES</span></span>

## <span data-ttu-id="6515d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6515d-139">RELATED LINKS</span></span>

[<span data-ttu-id="6515d-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="6515d-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="6515d-141">Új – AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="6515d-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
