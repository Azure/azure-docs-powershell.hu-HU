---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueue.md
ms.openlocfilehash: 2cc10a1b72dc369aef08b84e7b8fe2128ff0ac33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165643"
---
# <span data-ttu-id="01e5e-101">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="01e5e-101">Remove-AzStorageQueue</span></span>

## <span data-ttu-id="01e5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01e5e-102">SYNOPSIS</span></span>
<span data-ttu-id="01e5e-103">Eltávolít egy tárterület-várólistát.</span><span class="sxs-lookup"><span data-stu-id="01e5e-103">Removes a storage queue.</span></span>

## <span data-ttu-id="01e5e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="01e5e-104">SYNTAX</span></span>

```
Remove-AzStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01e5e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="01e5e-105">DESCRIPTION</span></span>
<span data-ttu-id="01e5e-106">A **Remove-AzStorageQueue** parancsmag eltávolítja a tárterület-várólistát.</span><span class="sxs-lookup"><span data-stu-id="01e5e-106">The **Remove-AzStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="01e5e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="01e5e-107">EXAMPLES</span></span>

### <span data-ttu-id="01e5e-108">1. példa: Tárterület várólistájának eltávolítása név szerint</span><span class="sxs-lookup"><span data-stu-id="01e5e-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzStorageQueue "ContosoQueue01"
```

<span data-ttu-id="01e5e-109">Ez a parancs eltávolítja a ContosoQueue01 nevű várólistát.</span><span class="sxs-lookup"><span data-stu-id="01e5e-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="01e5e-110">2. példa: Több tárterület-várólisták eltávolítása</span><span class="sxs-lookup"><span data-stu-id="01e5e-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzStorageQueue "Contoso*" | Remove-AzStorageQueue
```

<span data-ttu-id="01e5e-111">Ez a parancs eltávolítja a Contoso névvel kezdődő összes várólistát.</span><span class="sxs-lookup"><span data-stu-id="01e5e-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="01e5e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01e5e-112">PARAMETERS</span></span>

### <span data-ttu-id="01e5e-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="01e5e-113">-Context</span></span>
<span data-ttu-id="01e5e-114">Az Azure-tárterület környezetét határozza meg.</span><span class="sxs-lookup"><span data-stu-id="01e5e-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="01e5e-115">A tárolási környezet lekértérte a New-AzStorageContext parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="01e5e-115">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="01e5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e5e-116">-DefaultProfile</span></span>
<span data-ttu-id="01e5e-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="01e5e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01e5e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="01e5e-118">-Force</span></span>
<span data-ttu-id="01e5e-119">A parancs futtatását kényszeríti felhasználói megerősítés kérése nélkül.</span><span class="sxs-lookup"><span data-stu-id="01e5e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="01e5e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="01e5e-120">-Name</span></span>
<span data-ttu-id="01e5e-121">Az eltávolítható várólistát adja meg.</span><span class="sxs-lookup"><span data-stu-id="01e5e-121">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="01e5e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01e5e-122">-PassThru</span></span>
<span data-ttu-id="01e5e-123">Azt jelzi, hogy ez a parancsmag egy **logikai** értéket ad vissza, amely tükrözi a művelet sikeres működését.</span><span class="sxs-lookup"><span data-stu-id="01e5e-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="01e5e-124">Alapértelmezés szerint ez a parancsmag nem ad vissza értéket.</span><span class="sxs-lookup"><span data-stu-id="01e5e-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="01e5e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01e5e-125">-Confirm</span></span>
<span data-ttu-id="01e5e-126">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="01e5e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e5e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e5e-127">-WhatIf</span></span>
<span data-ttu-id="01e5e-128">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="01e5e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01e5e-129">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="01e5e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e5e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e5e-130">CommonParameters</span></span>
<span data-ttu-id="01e5e-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01e5e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e5e-132">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01e5e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e5e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01e5e-133">INPUTS</span></span>

### <span data-ttu-id="01e5e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="01e5e-134">System.String</span></span>

### <span data-ttu-id="01e5e-135">Microsoft.Azure.Commands.Common.Authentication.Absztrakt.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="01e5e-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="01e5e-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="01e5e-136">OUTPUTS</span></span>

### <span data-ttu-id="01e5e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01e5e-137">System.Boolean</span></span>

## <span data-ttu-id="01e5e-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="01e5e-138">NOTES</span></span>

## <span data-ttu-id="01e5e-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="01e5e-139">RELATED LINKS</span></span>

[<span data-ttu-id="01e5e-140">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="01e5e-140">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="01e5e-141">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="01e5e-141">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)
