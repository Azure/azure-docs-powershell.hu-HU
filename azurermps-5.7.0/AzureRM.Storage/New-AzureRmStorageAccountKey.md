---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 651fdef0599a9a62de5d4bdfac8fc5e9105bb4dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500360"
---
# <span data-ttu-id="1d076-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1d076-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="1d076-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d076-102">SYNOPSIS</span></span>
<span data-ttu-id="1d076-103">Egy Azure-tárterülethez tartozó tárterület kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="1d076-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d076-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d076-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="1d076-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d076-105">DESCRIPTION</span></span>
<span data-ttu-id="1d076-106">A **New-AzureRmStorageAccountKey** parancsmag egy Azure-tárterülethez tartozó tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1d076-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="1d076-107">Példák</span><span class="sxs-lookup"><span data-stu-id="1d076-107">EXAMPLES</span></span>

### <span data-ttu-id="1d076-108">1. példa: a tárolási kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="1d076-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="1d076-109">Ez a parancs újra létrehoz egy tárterületet a megadott tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="1d076-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="1d076-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d076-110">PARAMETERS</span></span>

### <span data-ttu-id="1d076-111">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="1d076-111">-KeyName</span></span>
<span data-ttu-id="1d076-112">Az újragenerálni kívánt kulcs megadása.</span><span class="sxs-lookup"><span data-stu-id="1d076-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="1d076-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="1d076-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d076-114">key1</span><span class="sxs-lookup"><span data-stu-id="1d076-114">key1</span></span>
- <span data-ttu-id="1d076-115">azonosító2</span><span class="sxs-lookup"><span data-stu-id="1d076-115">key2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d076-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d076-116">-Name</span></span>
<span data-ttu-id="1d076-117">Annak a tárterület-fióknak a nevét adja meg, amelynek a tárolási kulcsát újra létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="1d076-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="1d076-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d076-118">-ResourceGroupName</span></span>
<span data-ttu-id="1d076-119">A tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d076-119">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="1d076-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d076-120">CommonParameters</span></span>
<span data-ttu-id="1d076-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d076-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d076-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d076-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d076-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d076-123">INPUTS</span></span>

### <span data-ttu-id="1d076-124">Nincs</span><span class="sxs-lookup"><span data-stu-id="1d076-124">None</span></span>
<span data-ttu-id="1d076-125">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1d076-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d076-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d076-126">OUTPUTS</span></span>

## <span data-ttu-id="1d076-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d076-127">NOTES</span></span>

## <span data-ttu-id="1d076-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d076-128">RELATED LINKS</span></span>

[<span data-ttu-id="1d076-129">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1d076-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
