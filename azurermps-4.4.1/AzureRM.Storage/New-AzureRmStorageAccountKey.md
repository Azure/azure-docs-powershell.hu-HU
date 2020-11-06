---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 76b7ea9eb4a248071025ef359d6bf0877b35fe89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505564"
---
# <span data-ttu-id="2773b-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2773b-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="2773b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2773b-102">SYNOPSIS</span></span>
<span data-ttu-id="2773b-103">Egy Azure-tárterülethez tartozó tárterület kulcsának újragenerálása.</span><span class="sxs-lookup"><span data-stu-id="2773b-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2773b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2773b-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2773b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2773b-105">DESCRIPTION</span></span>
<span data-ttu-id="2773b-106">A **New-AzureRmStorageAccountKey** parancsmag egy Azure-tárterülethez tartozó tárterületet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2773b-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="2773b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2773b-107">EXAMPLES</span></span>

### <span data-ttu-id="2773b-108">1. példa: a tárolási kulcs újragenerálása</span><span class="sxs-lookup"><span data-stu-id="2773b-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="2773b-109">Ez a parancs újra létrehoz egy tárterületet a megadott tárterület-fiókhoz.</span><span class="sxs-lookup"><span data-stu-id="2773b-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="2773b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2773b-110">PARAMETERS</span></span>

### <span data-ttu-id="2773b-111">-Kulcsnév</span><span class="sxs-lookup"><span data-stu-id="2773b-111">-KeyName</span></span>
<span data-ttu-id="2773b-112">Az újragenerálni kívánt kulcs megadása.</span><span class="sxs-lookup"><span data-stu-id="2773b-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="2773b-113">A paraméter elfogadható értékei a következők:</span><span class="sxs-lookup"><span data-stu-id="2773b-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2773b-114">key1</span><span class="sxs-lookup"><span data-stu-id="2773b-114">key1</span></span> 
- <span data-ttu-id="2773b-115">azonosító2</span><span class="sxs-lookup"><span data-stu-id="2773b-115">key2</span></span>

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

### <span data-ttu-id="2773b-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2773b-116">-Name</span></span>
<span data-ttu-id="2773b-117">Annak a tárterület-fióknak a nevét adja meg, amelynek a tárolási kulcsát újra létre szeretné hozni.</span><span class="sxs-lookup"><span data-stu-id="2773b-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="2773b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2773b-118">-ResourceGroupName</span></span>
<span data-ttu-id="2773b-119">A tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2773b-119">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="2773b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2773b-120">-DefaultProfile</span></span>
<span data-ttu-id="2773b-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2773b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2773b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2773b-122">CommonParameters</span></span>
<span data-ttu-id="2773b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2773b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2773b-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2773b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2773b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2773b-125">INPUTS</span></span>

## <span data-ttu-id="2773b-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2773b-126">OUTPUTS</span></span>

## <span data-ttu-id="2773b-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2773b-127">NOTES</span></span>

## <span data-ttu-id="2773b-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2773b-128">RELATED LINKS</span></span>

[<span data-ttu-id="2773b-129">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2773b-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)


