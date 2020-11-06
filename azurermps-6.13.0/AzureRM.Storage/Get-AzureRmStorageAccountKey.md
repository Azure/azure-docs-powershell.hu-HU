---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 08d997caef7280d922a01dbea127bd4db64cd28f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491855"
---
# <span data-ttu-id="442df-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="442df-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="442df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="442df-102">SYNOPSIS</span></span>
<span data-ttu-id="442df-103">Egy Azure-tárterülethez tartozó hozzáférési kulcsokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="442df-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="442df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="442df-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="442df-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="442df-105">DESCRIPTION</span></span>
<span data-ttu-id="442df-106">A **Get-AzureRmStorageAccountKey** parancsmag a hozzáférési kulcsokat kapja meg egy Azure Storage-fiókban.</span><span class="sxs-lookup"><span data-stu-id="442df-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="442df-107">Példák</span><span class="sxs-lookup"><span data-stu-id="442df-107">EXAMPLES</span></span>

### <span data-ttu-id="442df-108">Példa 1: a tárolási fiók hozzáférési kulcsainak beolvasása</span><span class="sxs-lookup"><span data-stu-id="442df-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="442df-109">Ez a parancs a megadott Azure Storage-fiók kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="442df-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="442df-110">2. példa: speciális hozzáférési kulcs beszerzése tárterület-fiókhoz</span><span class="sxs-lookup"><span data-stu-id="442df-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="442df-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="442df-111">PARAMETERS</span></span>

### <span data-ttu-id="442df-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442df-112">-DefaultProfile</span></span>
<span data-ttu-id="442df-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="442df-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="442df-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="442df-114">-Name</span></span>
<span data-ttu-id="442df-115">Annak a tároló fióknak a nevét adja meg, amelyhez ez a parancsmag kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="442df-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="442df-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="442df-116">-ResourceGroupName</span></span>
<span data-ttu-id="442df-117">A tárolási fiókot tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="442df-117">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="442df-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442df-118">CommonParameters</span></span>
<span data-ttu-id="442df-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="442df-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442df-120">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="442df-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442df-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="442df-121">INPUTS</span></span>

### <span data-ttu-id="442df-122">System. String</span><span class="sxs-lookup"><span data-stu-id="442df-122">System.String</span></span>

## <span data-ttu-id="442df-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="442df-123">OUTPUTS</span></span>

### <span data-ttu-id="442df-124">Microsoft. Azure. Management. Storage. models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="442df-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="442df-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="442df-125">NOTES</span></span>

## <span data-ttu-id="442df-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="442df-126">RELATED LINKS</span></span>

[<span data-ttu-id="442df-127">Új – AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="442df-127">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)


