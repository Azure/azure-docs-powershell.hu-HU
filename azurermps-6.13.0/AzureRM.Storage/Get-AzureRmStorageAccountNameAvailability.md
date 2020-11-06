---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 402e3fdfe108486cd356af8a20ea06793f533937
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502820"
---
# <span data-ttu-id="83b02-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="83b02-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="83b02-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="83b02-102">SYNOPSIS</span></span>
<span data-ttu-id="83b02-103">Ellenőrzi a tárolási fiók nevének elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="83b02-103">Checks the availability of a Storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83b02-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="83b02-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="83b02-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="83b02-105">DESCRIPTION</span></span>
<span data-ttu-id="83b02-106">A **Get-AzureRmStorageAccountNameAvailability** parancsmag ellenőrzi, hogy érvényes-e az Azure-tárterület-fiók neve, és használható-e.</span><span class="sxs-lookup"><span data-stu-id="83b02-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="83b02-107">Példák</span><span class="sxs-lookup"><span data-stu-id="83b02-107">EXAMPLES</span></span>

### <span data-ttu-id="83b02-108">1. példa: a tárterület-fióknév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="83b02-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="83b02-109">Ez a parancs ellenőrzi a ContosoStorage03 név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="83b02-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="83b02-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="83b02-110">PARAMETERS</span></span>

### <span data-ttu-id="83b02-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b02-111">-DefaultProfile</span></span>
<span data-ttu-id="83b02-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="83b02-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83b02-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="83b02-113">-Name</span></span>
<span data-ttu-id="83b02-114">A parancsmag által ellenőrzött tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="83b02-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="83b02-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b02-115">CommonParameters</span></span>
<span data-ttu-id="83b02-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="83b02-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b02-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b02-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b02-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="83b02-118">INPUTS</span></span>

### <span data-ttu-id="83b02-119">System. String</span><span class="sxs-lookup"><span data-stu-id="83b02-119">System.String</span></span>

## <span data-ttu-id="83b02-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="83b02-120">OUTPUTS</span></span>

### <span data-ttu-id="83b02-121">Microsoft. Azure. Management. Storage. models. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="83b02-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="83b02-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="83b02-122">NOTES</span></span>

## <span data-ttu-id="83b02-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="83b02-123">RELATED LINKS</span></span>

[<span data-ttu-id="83b02-124">Azure Storage Manager-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="83b02-124">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


