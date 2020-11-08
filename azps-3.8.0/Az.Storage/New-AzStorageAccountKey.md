---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: d63c948e59dbc05122c63b6688277a7015a42163
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013145"
---
# <span data-ttu-id="8366a-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8366a-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="8366a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8366a-102">SYNOPSIS</span></span>
<span data-ttu-id="8366a-103">Egy Azure-tárterülethez tartozó tárterület kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="8366a-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="8366a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8366a-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8366a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8366a-105">DESCRIPTION</span></span>
<span data-ttu-id="8366a-106">A **New-AzStorageAccountKey** parancsmag egy Azure-tárterülethez tartozó tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="8366a-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="8366a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="8366a-107">EXAMPLES</span></span>

### <span data-ttu-id="8366a-108">1. példa: a tárolási kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="8366a-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="8366a-109">Ez a parancs újra létrehoz egy tárterületet a megadott tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="8366a-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="8366a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8366a-110">PARAMETERS</span></span>

### <span data-ttu-id="8366a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8366a-111">-DefaultProfile</span></span>
<span data-ttu-id="8366a-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8366a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8366a-113">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="8366a-113">-KeyName</span></span>
<span data-ttu-id="8366a-114">Az újragenerálni kívánt kulcs megadása.</span><span class="sxs-lookup"><span data-stu-id="8366a-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="8366a-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="8366a-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8366a-116">key1</span><span class="sxs-lookup"><span data-stu-id="8366a-116">key1</span></span>
- <span data-ttu-id="8366a-117">azonosító2</span><span class="sxs-lookup"><span data-stu-id="8366a-117">key2</span></span>

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

### <span data-ttu-id="8366a-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8366a-118">-Name</span></span>
<span data-ttu-id="8366a-119">Annak a tárterület-fióknak a nevét adja meg, amelynek a tárolási kulcsát újra létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="8366a-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="8366a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8366a-120">-ResourceGroupName</span></span>
<span data-ttu-id="8366a-121">A tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="8366a-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="8366a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8366a-122">CommonParameters</span></span>
<span data-ttu-id="8366a-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8366a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8366a-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8366a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8366a-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8366a-125">INPUTS</span></span>

### <span data-ttu-id="8366a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8366a-126">System.String</span></span>

## <span data-ttu-id="8366a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8366a-127">OUTPUTS</span></span>

### <span data-ttu-id="8366a-128">Microsoft. Azure. Management. Storage. models. StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="8366a-128">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="8366a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8366a-129">NOTES</span></span>

## <span data-ttu-id="8366a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8366a-130">RELATED LINKS</span></span>

[<span data-ttu-id="8366a-131">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="8366a-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
