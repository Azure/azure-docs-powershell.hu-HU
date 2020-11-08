---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f5620baf0cbd2f5c195b981787ac9def98851fe2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185802"
---
# <span data-ttu-id="ff3a0-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ff3a0-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ff3a0-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ff3a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3a0-103">Egy tárolt Access-házirend eltávolítása egy Azure-tárterület-várólistából.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="ff3a0-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ff3a0-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff3a0-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ff3a0-105">DESCRIPTION</span></span>
<span data-ttu-id="ff3a0-106">A **Remove-AzStorageQueueStoredAccessPolicy** parancsmag az Azure tárterület-várólistából távolítja el a tárolt hozzáférési házirendet.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="ff3a0-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ff3a0-107">EXAMPLES</span></span>

### <span data-ttu-id="ff3a0-108">1. példa: tárolt hozzáférési házirend eltávolítása a tárolási várólistából</span><span class="sxs-lookup"><span data-stu-id="ff3a0-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="ff3a0-109">Ez a parancs eltávolítja a Policy04 nevű Access-házirendet a MyQueue nevű tárterület-várólistából.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="ff3a0-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ff3a0-110">PARAMETERS</span></span>

### <span data-ttu-id="ff3a0-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ff3a0-111">-Context</span></span>
<span data-ttu-id="ff3a0-112">Az Azure tárolási környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ff3a0-113">A tárolási környezet eléréséhez használja az New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ff3a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff3a0-114">-DefaultProfile</span></span>
<span data-ttu-id="ff3a0-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff3a0-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff3a0-116">-PassThru</span></span>
<span data-ttu-id="ff3a0-117">Jelzi, hogy ez a parancsmag olyan **logikai** értéket ad eredményül, amely tükrözi a művelet sikerét.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ff3a0-118">Ez a parancsmag alapértelmezés szerint nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ff3a0-119">-Házirend</span><span class="sxs-lookup"><span data-stu-id="ff3a0-119">-Policy</span></span>
<span data-ttu-id="ff3a0-120">Annak a tárolt hozzáférési házirendnek a nevét adja meg, amelyre a parancsmag eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3a0-121">-Queue (várólista)</span><span class="sxs-lookup"><span data-stu-id="ff3a0-121">-Queue</span></span>
<span data-ttu-id="ff3a0-122">Az Azure Storage Queue nevet adja meg.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-122">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff3a0-123">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ff3a0-123">-Confirm</span></span>
<span data-ttu-id="ff3a0-124">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff3a0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff3a0-125">-WhatIf</span></span>
<span data-ttu-id="ff3a0-126">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff3a0-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ff3a0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff3a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3a0-128">CommonParameters</span></span>
<span data-ttu-id="ff3a0-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ff3a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3a0-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff3a0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3a0-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff3a0-131">INPUTS</span></span>

### <span data-ttu-id="ff3a0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ff3a0-132">System.String</span></span>

### <span data-ttu-id="ff3a0-133">Microsoft. Azure. commands. Common. Authentication. absztrakciók. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff3a0-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ff3a0-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ff3a0-134">OUTPUTS</span></span>

### <span data-ttu-id="ff3a0-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ff3a0-135">System.Boolean</span></span>

## <span data-ttu-id="ff3a0-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ff3a0-136">NOTES</span></span>

## <span data-ttu-id="ff3a0-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ff3a0-137">RELATED LINKS</span></span>

[<span data-ttu-id="ff3a0-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ff3a0-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ff3a0-139">Új – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff3a0-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ff3a0-140">Új – AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ff3a0-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ff3a0-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ff3a0-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
