---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: e44ccbaae730554db35610ff1084e9740e873e53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504260"
---
# <span data-ttu-id="76f47-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="76f47-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="76f47-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="76f47-102">SYNOPSIS</span></span>
<span data-ttu-id="76f47-103">Egy Azure-tárterülethez tartozó tárterület kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="76f47-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76f47-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="76f47-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76f47-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="76f47-105">DESCRIPTION</span></span>
<span data-ttu-id="76f47-106">A **New-AzureRmStorageAccountKey** parancsmag egy Azure-tárterülethez tartozó tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="76f47-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="76f47-107">Példák</span><span class="sxs-lookup"><span data-stu-id="76f47-107">EXAMPLES</span></span>

### <span data-ttu-id="76f47-108">1. példa: a tárolási kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="76f47-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="76f47-109">Ez a parancs újra létrehoz egy tárterületet a megadott tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="76f47-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="76f47-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="76f47-110">PARAMETERS</span></span>

### <span data-ttu-id="76f47-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f47-111">-DefaultProfile</span></span>
<span data-ttu-id="76f47-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76f47-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f47-113">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="76f47-113">-KeyName</span></span>
<span data-ttu-id="76f47-114">Az újragenerálni kívánt kulcs megadása.</span><span class="sxs-lookup"><span data-stu-id="76f47-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="76f47-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="76f47-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76f47-116">key1</span><span class="sxs-lookup"><span data-stu-id="76f47-116">key1</span></span>
- <span data-ttu-id="76f47-117">azonosító2</span><span class="sxs-lookup"><span data-stu-id="76f47-117">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f47-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="76f47-118">-Name</span></span>
<span data-ttu-id="76f47-119">Annak a tárterület-fióknak a nevét adja meg, amelynek a tárolási kulcsát újra létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="76f47-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f47-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f47-120">-ResourceGroupName</span></span>
<span data-ttu-id="76f47-121">A tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="76f47-121">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f47-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f47-122">CommonParameters</span></span>
<span data-ttu-id="76f47-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="76f47-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f47-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76f47-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f47-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="76f47-125">INPUTS</span></span>

### <span data-ttu-id="76f47-126">System. String</span><span class="sxs-lookup"><span data-stu-id="76f47-126">System.String</span></span>

## <span data-ttu-id="76f47-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76f47-127">OUTPUTS</span></span>

### <span data-ttu-id="76f47-128">Microsoft. Azure. Management. Storage. models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="76f47-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="76f47-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="76f47-129">NOTES</span></span>

## <span data-ttu-id="76f47-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76f47-130">RELATED LINKS</span></span>

[<span data-ttu-id="76f47-131">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="76f47-131">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
