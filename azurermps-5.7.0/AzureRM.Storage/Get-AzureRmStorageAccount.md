---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: e84bb0dd511f5534b8794327b68f2321efcdc130
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492980"
---
# <span data-ttu-id="3d1ad-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d1ad-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="3d1ad-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3d1ad-102">SYNOPSIS</span></span>
<span data-ttu-id="3d1ad-103">Megkapja a tárolási fiókot.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d1ad-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3d1ad-104">SYNTAX</span></span>

### <span data-ttu-id="3d1ad-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d1ad-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="3d1ad-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d1ad-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="3d1ad-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="3d1ad-107">DESCRIPTION</span></span>
<span data-ttu-id="3d1ad-108">A **Get-AzureRmStorageAccount** parancsmag egy erőforrás-csoportban vagy az előfizetésben megadott tárolási fiókot vagy minden tárolási fiókot kap.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="3d1ad-109">Példák</span><span class="sxs-lookup"><span data-stu-id="3d1ad-109">EXAMPLES</span></span>

### <span data-ttu-id="3d1ad-110">1. példa: megadott tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="3d1ad-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="3d1ad-111">Ez a parancs a megadott tárterület-fiókot kapja.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="3d1ad-112">2. példa: az erőforráscsoport minden tárolási fiókjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="3d1ad-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="3d1ad-113">Ez a parancs egy erőforráscsoport minden tárolási fiókját beilleszti.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="3d1ad-114">3. példa: az előfizetésben lévő összes tárterület-fiók beszerzése</span><span class="sxs-lookup"><span data-stu-id="3d1ad-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="3d1ad-115">Ez a parancs az előfizetésben szereplő összes tárolási fiókot beilleszti.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="3d1ad-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3d1ad-116">PARAMETERS</span></span>

### <span data-ttu-id="3d1ad-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3d1ad-117">-Name</span></span>
<span data-ttu-id="3d1ad-118">A beszerzéshez használandó tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-118">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d1ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d1ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="3d1ad-120">Annak a csoportnak a neve, amely a beszerzéshez használt tárolási fiókot tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d1ad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d1ad-121">CommonParameters</span></span>
<span data-ttu-id="3d1ad-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3d1ad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d1ad-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d1ad-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d1ad-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d1ad-124">INPUTS</span></span>

### <span data-ttu-id="3d1ad-125">Nincs</span><span class="sxs-lookup"><span data-stu-id="3d1ad-125">None</span></span>
<span data-ttu-id="3d1ad-126">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="3d1ad-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3d1ad-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3d1ad-127">OUTPUTS</span></span>

## <span data-ttu-id="3d1ad-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3d1ad-128">NOTES</span></span>

## <span data-ttu-id="3d1ad-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3d1ad-129">RELATED LINKS</span></span>

[<span data-ttu-id="3d1ad-130">Új – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d1ad-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="3d1ad-131">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d1ad-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="3d1ad-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3d1ad-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)
