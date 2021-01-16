---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4FB7E017-7D37-4EDB-BEC1-36629058B87C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 0f8d9860f04112c197b91907a7622683069c3589
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376108"
---
# <span data-ttu-id="ac3c5-101">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac3c5-101">Set-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="ac3c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac3c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ac3c5-103">Tárolt hozzáférési házirendet állít be egy Azure-tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-103">Sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="ac3c5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ac3c5-104">SYNTAX</span></span>

```
Set-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac3c5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ac3c5-105">DESCRIPTION</span></span>
<span data-ttu-id="ac3c5-106">A **Set-AzStorageQueueStoredAccessPolicy** parancsmag tárolt hozzáférési házirendet állít be egy Azure-tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-106">The **Set-AzStorageQueueStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="ac3c5-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ac3c5-107">EXAMPLES</span></span>

### <span data-ttu-id="ac3c5-108">1. példa: Tárolt hozzáférési házirend beállítása a várólistán teljes engedéllyel</span><span class="sxs-lookup"><span data-stu-id="ac3c5-108">Example 1: Set a stored access policy in the queue with full permission</span></span>
```
PS C:\> Set-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy07" -Permission arup
```

<span data-ttu-id="ac3c5-109">Ez a parancs beállítja a Házirend07 nevű hozzáférési házirendet a MyQueue nevű tárterület-várólistához.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-109">This command sets an access policy named Policy07 for storage queue named MyQueue.</span></span>

## <span data-ttu-id="ac3c5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac3c5-110">PARAMETERS</span></span>

### <span data-ttu-id="ac3c5-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ac3c5-111">-Context</span></span>
<span data-ttu-id="ac3c5-112">Egy Azure-tárterület környezetét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ac3c5-113">A tárterület környezetének lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ac3c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac3c5-114">-DefaultProfile</span></span>
<span data-ttu-id="ac3c5-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac3c5-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ac3c5-116">-ExpiryTime</span></span>
<span data-ttu-id="ac3c5-117">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvénytelenné válik.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="ac3c5-118">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ac3c5-118">-NoExpiryTime</span></span>
<span data-ttu-id="ac3c5-119">Azt jelzi, hogy a hozzáférési házirendnek nincs lejárati dátuma.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-119">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="ac3c5-120">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="ac3c5-120">-NoStartTime</span></span>
<span data-ttu-id="ac3c5-121">Azt jelzi, hogy ez a parancsmag beállítja a kezdési $Null.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-121">Indicates that this cmdlet sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="ac3c5-122">-Engedély</span><span class="sxs-lookup"><span data-stu-id="ac3c5-122">-Permission</span></span>
<span data-ttu-id="ac3c5-123">Engedélyeket ad meg a tárterület-várólistához való hozzáféréshez a tárolt hozzáférési házirendben.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-123">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="ac3c5-124">Fontos megjegyezni, hogy ez egy karakterlánc, például `rwd` (Olvasás, Írás és Törlés).</span><span class="sxs-lookup"><span data-stu-id="ac3c5-124">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="ac3c5-125">-Házirend</span><span class="sxs-lookup"><span data-stu-id="ac3c5-125">-Policy</span></span>
<span data-ttu-id="ac3c5-126">A tárolt hozzáférési házirend nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-126">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="ac3c5-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="ac3c5-127">-Queue</span></span>
<span data-ttu-id="ac3c5-128">Az Azure-társor nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-128">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="ac3c5-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ac3c5-129">-StartTime</span></span>
<span data-ttu-id="ac3c5-130">Azt az időt adja meg, amikor a tárolt hozzáférési házirend érvényessé válik.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-130">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="ac3c5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac3c5-131">-Confirm</span></span>
<span data-ttu-id="ac3c5-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac3c5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac3c5-133">-WhatIf</span></span>
<span data-ttu-id="ac3c5-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac3c5-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac3c5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac3c5-136">CommonParameters</span></span>
<span data-ttu-id="ac3c5-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac3c5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac3c5-138">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac3c5-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac3c5-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac3c5-139">INPUTS</span></span>

### <span data-ttu-id="ac3c5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ac3c5-140">System.String</span></span>

### <span data-ttu-id="ac3c5-141">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ac3c5-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ac3c5-142">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ac3c5-142">OUTPUTS</span></span>

### <span data-ttu-id="ac3c5-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ac3c5-143">System.String</span></span>

## <span data-ttu-id="ac3c5-144">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ac3c5-144">NOTES</span></span>

## <span data-ttu-id="ac3c5-145">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ac3c5-145">RELATED LINKS</span></span>

[<span data-ttu-id="ac3c5-146">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac3c5-146">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ac3c5-147">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac3c5-147">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="ac3c5-148">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac3c5-148">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)
