---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: 2000b2f50ac4c3c26f1e5dfbc5debe07ea9bd894
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843109"
---
# <span data-ttu-id="dafc5-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="dafc5-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="dafc5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dafc5-102">SYNOPSIS</span></span>
<span data-ttu-id="dafc5-103">Ellenőrzi a tárolási fiók nevének elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="dafc5-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="dafc5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dafc5-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dafc5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="dafc5-105">DESCRIPTION</span></span>
<span data-ttu-id="dafc5-106">A **Get-AzStorageAccountNameAvailability** parancsmag ellenőrzi, hogy érvényes-e az Azure-tárterület-fiók neve, és használható-e.</span><span class="sxs-lookup"><span data-stu-id="dafc5-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="dafc5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="dafc5-107">EXAMPLES</span></span>

### <span data-ttu-id="dafc5-108">1. példa: a tárterület-fióknév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="dafc5-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="dafc5-109">Ez a parancs ellenőrzi a ContosoStorage03 név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="dafc5-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="dafc5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dafc5-110">PARAMETERS</span></span>

### <span data-ttu-id="dafc5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafc5-111">-DefaultProfile</span></span>
<span data-ttu-id="dafc5-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dafc5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dafc5-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dafc5-113">-Name</span></span>
<span data-ttu-id="dafc5-114">A parancsmag által ellenőrzött tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="dafc5-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="dafc5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafc5-115">CommonParameters</span></span>
<span data-ttu-id="dafc5-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dafc5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafc5-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dafc5-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafc5-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dafc5-118">INPUTS</span></span>

### <span data-ttu-id="dafc5-119">System. String</span><span class="sxs-lookup"><span data-stu-id="dafc5-119">System.String</span></span>

## <span data-ttu-id="dafc5-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dafc5-120">OUTPUTS</span></span>

### <span data-ttu-id="dafc5-121">Microsoft. Azure. Management. Storage. models. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="dafc5-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="dafc5-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dafc5-122">NOTES</span></span>

## <span data-ttu-id="dafc5-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dafc5-123">RELATED LINKS</span></span>

[<span data-ttu-id="dafc5-124">Azure Storage Manager-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="dafc5-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


