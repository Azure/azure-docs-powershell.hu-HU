---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: e6a6a35b5e744218c3afc6db396e875ad0acf242
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679649"
---
# <span data-ttu-id="93ad6-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="93ad6-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="93ad6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="93ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="93ad6-103">Eltávolít egy tárterület-fiókot az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="93ad6-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93ad6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="93ad6-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93ad6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="93ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="93ad6-106">A **Remove-AzureRmStorageAccount** parancsmag eltávolítja a tárolási fiókot az Azure-ról.</span><span class="sxs-lookup"><span data-stu-id="93ad6-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="93ad6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="93ad6-107">EXAMPLES</span></span>

### <span data-ttu-id="93ad6-108">1. példa: tárterület-fiók eltávolítása</span><span class="sxs-lookup"><span data-stu-id="93ad6-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="93ad6-109">Ez a parancs eltávolítja a megadott tárterület-fiókot.</span><span class="sxs-lookup"><span data-stu-id="93ad6-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="93ad6-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="93ad6-110">PARAMETERS</span></span>

### <span data-ttu-id="93ad6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="93ad6-111">-Force</span></span>
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

### <span data-ttu-id="93ad6-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="93ad6-112">-Name</span></span>
<span data-ttu-id="93ad6-113">Az eltávolítandó tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93ad6-113">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93ad6-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93ad6-114">-ResourceGroupName</span></span>
<span data-ttu-id="93ad6-115">Az eltávolítandó tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="93ad6-115">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93ad6-116">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="93ad6-116">-Confirm</span></span>
<span data-ttu-id="93ad6-117">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="93ad6-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ad6-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ad6-118">-WhatIf</span></span>
<span data-ttu-id="93ad6-119">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="93ad6-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93ad6-120">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="93ad6-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ad6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ad6-121">CommonParameters</span></span>
<span data-ttu-id="93ad6-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="93ad6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ad6-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ad6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ad6-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="93ad6-124">INPUTS</span></span>

### <span data-ttu-id="93ad6-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="93ad6-125">None</span></span>
<span data-ttu-id="93ad6-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="93ad6-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93ad6-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93ad6-127">OUTPUTS</span></span>

## <span data-ttu-id="93ad6-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="93ad6-128">NOTES</span></span>

## <span data-ttu-id="93ad6-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93ad6-129">RELATED LINKS</span></span>

[<span data-ttu-id="93ad6-130">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="93ad6-130">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="93ad6-131">Új – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="93ad6-131">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="93ad6-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="93ad6-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
