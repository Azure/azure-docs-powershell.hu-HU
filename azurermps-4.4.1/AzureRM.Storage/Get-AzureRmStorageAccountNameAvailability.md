---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8ca5c33944882fde7e9bad2411df5f41dbe5f788
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495519"
---
# <span data-ttu-id="68e8b-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="68e8b-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="68e8b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="68e8b-102">SYNOPSIS</span></span>
<span data-ttu-id="68e8b-103">Ellenőrzi a tárolási fiók nevének elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="68e8b-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68e8b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="68e8b-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="68e8b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="68e8b-105">DESCRIPTION</span></span>
<span data-ttu-id="68e8b-106">A **Get-AzureRmStorageAccountNameAvailability** parancsmag ellenőrzi, hogy érvényes-e az Azure-tárterület-fiók neve, és használható-e.</span><span class="sxs-lookup"><span data-stu-id="68e8b-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="68e8b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="68e8b-107">EXAMPLES</span></span>

### <span data-ttu-id="68e8b-108">1. példa: a tárterület-fióknév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="68e8b-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="68e8b-109">Ez a parancs ellenőrzi a ContosoStorage03 név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="68e8b-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="68e8b-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="68e8b-110">PARAMETERS</span></span>

### <span data-ttu-id="68e8b-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="68e8b-111">-Name</span></span>
<span data-ttu-id="68e8b-112">A parancsmag által ellenőrzött tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="68e8b-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="68e8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68e8b-113">-DefaultProfile</span></span>
<span data-ttu-id="68e8b-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="68e8b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68e8b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68e8b-115">CommonParameters</span></span>
<span data-ttu-id="68e8b-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="68e8b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68e8b-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68e8b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68e8b-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="68e8b-118">INPUTS</span></span>

## <span data-ttu-id="68e8b-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="68e8b-119">OUTPUTS</span></span>

## <span data-ttu-id="68e8b-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="68e8b-120">NOTES</span></span>

## <span data-ttu-id="68e8b-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="68e8b-121">RELATED LINKS</span></span>

[<span data-ttu-id="68e8b-122">Azure Storage Manager-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="68e8b-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


