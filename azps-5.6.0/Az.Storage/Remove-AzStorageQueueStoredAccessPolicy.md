---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 88b142943e37009cf21b35bdaadfd209d1d74c86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923250"
---
# <span data-ttu-id="0931c-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0931c-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="0931c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0931c-102">SYNOPSIS</span></span>
<span data-ttu-id="0931c-103">Egy tárolt hozzáférési házirend eltávolítása egy Azure-tárterület-várólistáról.</span><span class="sxs-lookup"><span data-stu-id="0931c-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="0931c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0931c-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0931c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0931c-105">DESCRIPTION</span></span>
<span data-ttu-id="0931c-106">A **Remove-AzStorageQueueStoredAccessPolicy** parancsmag eltávolít egy tárolt hozzáférési házirendet egy Azure-tárterület-várólistáról.</span><span class="sxs-lookup"><span data-stu-id="0931c-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="0931c-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0931c-107">EXAMPLES</span></span>

### <span data-ttu-id="0931c-108">1. példa: Tárolt hozzáférési házirend eltávolítása egy társorból</span><span class="sxs-lookup"><span data-stu-id="0931c-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="0931c-109">Ez a parancs eltávolítja a Policy04 nevű hozzáférési házirendet a MyQueue nevű társorból.</span><span class="sxs-lookup"><span data-stu-id="0931c-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="0931c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0931c-110">PARAMETERS</span></span>

### <span data-ttu-id="0931c-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0931c-111">-Context</span></span>
<span data-ttu-id="0931c-112">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0931c-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0931c-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="0931c-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0931c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0931c-114">-DefaultProfile</span></span>
<span data-ttu-id="0931c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0931c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0931c-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0931c-116">-PassThru</span></span>
<span data-ttu-id="0931c-117">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="0931c-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="0931c-118">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="0931c-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="0931c-119">-Házirend</span><span class="sxs-lookup"><span data-stu-id="0931c-119">-Policy</span></span>
<span data-ttu-id="0931c-120">A parancsmag által eltávolított tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0931c-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0931c-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="0931c-121">-Queue</span></span>
<span data-ttu-id="0931c-122">Az Azure-társor nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0931c-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="0931c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0931c-123">-Confirm</span></span>
<span data-ttu-id="0931c-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0931c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0931c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0931c-125">-WhatIf</span></span>
<span data-ttu-id="0931c-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0931c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0931c-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0931c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0931c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0931c-128">CommonParameters</span></span>
<span data-ttu-id="0931c-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0931c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0931c-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0931c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0931c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0931c-131">INPUTS</span></span>

### <span data-ttu-id="0931c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="0931c-132">System.String</span></span>

### <span data-ttu-id="0931c-133">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0931c-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0931c-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0931c-134">OUTPUTS</span></span>

### <span data-ttu-id="0931c-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0931c-135">System.Boolean</span></span>

## <span data-ttu-id="0931c-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0931c-136">NOTES</span></span>

## <span data-ttu-id="0931c-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0931c-137">RELATED LINKS</span></span>

[<span data-ttu-id="0931c-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0931c-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="0931c-139">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="0931c-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0931c-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0931c-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="0931c-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0931c-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
