---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 23066206607289d531f2e2eaa14f90660360a705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492978"
---
# <span data-ttu-id="d5451-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d5451-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="d5451-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d5451-102">SYNOPSIS</span></span>
<span data-ttu-id="d5451-103">Egy Azure-tárterülethez tartozó hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5451-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5451-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d5451-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="d5451-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d5451-105">DESCRIPTION</span></span>
<span data-ttu-id="d5451-106">A **Get-AzureRmStorageAccountKey** parancsmag a hozzáférési kulcsokat kapja meg egy Azure Storage-fiókban.</span><span class="sxs-lookup"><span data-stu-id="d5451-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="d5451-107">Példák</span><span class="sxs-lookup"><span data-stu-id="d5451-107">EXAMPLES</span></span>

### <span data-ttu-id="d5451-108">Példa 1: a tárolási fiók hozzáférési kulcsainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="d5451-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="d5451-109">Ez a parancs a megadott Azure Storage-fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5451-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="d5451-110">2. példa: speciális hozzáférési kulcs beszerzése tárterület-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="d5451-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="d5451-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d5451-111">PARAMETERS</span></span>

### <span data-ttu-id="d5451-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d5451-112">-Name</span></span>
<span data-ttu-id="d5451-113">Annak a tároló fióknak a nevét adja meg, amelyhez ez a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="d5451-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="d5451-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5451-114">-ResourceGroupName</span></span>
<span data-ttu-id="d5451-115">A tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5451-115">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="d5451-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5451-116">CommonParameters</span></span>
<span data-ttu-id="d5451-117">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d5451-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5451-118">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5451-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5451-119">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5451-119">INPUTS</span></span>

### <span data-ttu-id="d5451-120">Nincs</span><span class="sxs-lookup"><span data-stu-id="d5451-120">None</span></span>
<span data-ttu-id="d5451-121">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="d5451-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d5451-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5451-122">OUTPUTS</span></span>

## <span data-ttu-id="d5451-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d5451-123">NOTES</span></span>

## <span data-ttu-id="d5451-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5451-124">RELATED LINKS</span></span>

[<span data-ttu-id="d5451-125">Új – AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d5451-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)
