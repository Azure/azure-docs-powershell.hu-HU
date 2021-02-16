---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f5620baf0cbd2f5c195b981787ac9def98851fe2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165642"
---
# <span data-ttu-id="35627-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="35627-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="35627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35627-102">SYNOPSIS</span></span>
<span data-ttu-id="35627-103">Eltávolít egy tárolt hozzáférési házirendet egy Azure-tárterület-várólistáról.</span><span class="sxs-lookup"><span data-stu-id="35627-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="35627-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="35627-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35627-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="35627-105">DESCRIPTION</span></span>
<span data-ttu-id="35627-106">A **Remove-AzStorageQueueStoredAccessPolicy** parancsmag eltávolít egy tárolt hozzáférési házirendet egy Azure-tárterület-várólistáról.</span><span class="sxs-lookup"><span data-stu-id="35627-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="35627-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="35627-107">EXAMPLES</span></span>

### <span data-ttu-id="35627-108">1. példa: Tárolt hozzáférési házirend eltávolítása egy társorból</span><span class="sxs-lookup"><span data-stu-id="35627-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="35627-109">Ez a parancs eltávolítja a Policy04 nevű hozzáférési házirendet a MyQueue nevű társorból.</span><span class="sxs-lookup"><span data-stu-id="35627-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="35627-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35627-110">PARAMETERS</span></span>

### <span data-ttu-id="35627-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="35627-111">-Context</span></span>
<span data-ttu-id="35627-112">Egy Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="35627-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="35627-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="35627-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="35627-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35627-114">-DefaultProfile</span></span>
<span data-ttu-id="35627-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35627-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35627-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35627-116">-PassThru</span></span>
<span data-ttu-id="35627-117">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="35627-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="35627-118">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="35627-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="35627-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="35627-119">-Policy</span></span>
<span data-ttu-id="35627-120">A parancsmag által eltávolított tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35627-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="35627-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="35627-121">-Queue</span></span>
<span data-ttu-id="35627-122">Az Azure-társor nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="35627-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="35627-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35627-123">-Confirm</span></span>
<span data-ttu-id="35627-124">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="35627-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35627-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35627-125">-WhatIf</span></span>
<span data-ttu-id="35627-126">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="35627-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35627-127">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="35627-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35627-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35627-128">CommonParameters</span></span>
<span data-ttu-id="35627-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35627-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35627-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35627-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35627-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35627-131">INPUTS</span></span>

### <span data-ttu-id="35627-132">System.String</span><span class="sxs-lookup"><span data-stu-id="35627-132">System.String</span></span>

### <span data-ttu-id="35627-133">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="35627-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="35627-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35627-134">OUTPUTS</span></span>

### <span data-ttu-id="35627-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35627-135">System.Boolean</span></span>

## <span data-ttu-id="35627-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="35627-136">NOTES</span></span>

## <span data-ttu-id="35627-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35627-137">RELATED LINKS</span></span>

[<span data-ttu-id="35627-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="35627-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="35627-139">New-AzstorageContext</span><span class="sxs-lookup"><span data-stu-id="35627-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="35627-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="35627-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="35627-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="35627-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
