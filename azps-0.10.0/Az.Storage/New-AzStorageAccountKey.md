---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: 70acc17513e60892baae1fe8ebc15776518b3f57
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843029"
---
# <span data-ttu-id="7ffa4-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7ffa4-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="7ffa4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="7ffa4-102">SYNOPSIS</span></span>
<span data-ttu-id="7ffa4-103">Egy Azure-tárterülethez tartozó tárterület kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="7ffa4-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="7ffa4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="7ffa4-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ffa4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="7ffa4-105">DESCRIPTION</span></span>
<span data-ttu-id="7ffa4-106">A **New-AzStorageAccountKey** parancsmag egy Azure-tárterülethez tartozó tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="7ffa4-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="7ffa4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="7ffa4-107">EXAMPLES</span></span>

### <span data-ttu-id="7ffa4-108">1. példa: a tárolási kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="7ffa4-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="7ffa4-109">Ez a parancs újra létrehoz egy tárterületet a megadott tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="7ffa4-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="7ffa4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="7ffa4-110">PARAMETERS</span></span>

### <span data-ttu-id="7ffa4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ffa4-111">-DefaultProfile</span></span>
<span data-ttu-id="7ffa4-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7ffa4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ffa4-113">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="7ffa4-113">-KeyName</span></span>
<span data-ttu-id="7ffa4-114">Az újragenerálni kívánt kulcs megadása.</span><span class="sxs-lookup"><span data-stu-id="7ffa4-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="7ffa4-115">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="7ffa4-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ffa4-116">key1</span><span class="sxs-lookup"><span data-stu-id="7ffa4-116">key1</span></span>
- <span data-ttu-id="7ffa4-117">azonosító2</span><span class="sxs-lookup"><span data-stu-id="7ffa4-117">key2</span></span>

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

### <span data-ttu-id="7ffa4-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="7ffa4-118">-Name</span></span>
<span data-ttu-id="7ffa4-119">Annak a tárterület-fióknak a nevét adja meg, amelynek a tárolási kulcsát újra létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="7ffa4-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="7ffa4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ffa4-120">-ResourceGroupName</span></span>
<span data-ttu-id="7ffa4-121">A tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="7ffa4-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="7ffa4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ffa4-122">CommonParameters</span></span>
<span data-ttu-id="7ffa4-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="7ffa4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ffa4-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ffa4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ffa4-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ffa4-125">INPUTS</span></span>

### <span data-ttu-id="7ffa4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7ffa4-126">System.String</span></span>

## <span data-ttu-id="7ffa4-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7ffa4-127">OUTPUTS</span></span>

### <span data-ttu-id="7ffa4-128">Microsoft. Azure. Management. Storage. models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7ffa4-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="7ffa4-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="7ffa4-129">NOTES</span></span>

## <span data-ttu-id="7ffa4-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7ffa4-130">RELATED LINKS</span></span>

[<span data-ttu-id="7ffa4-131">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7ffa4-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
