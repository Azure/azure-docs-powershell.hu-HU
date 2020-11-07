---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: 60e30de4d6d55007ec659a267b1d450ac1cfeff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839642"
---
# <span data-ttu-id="245bf-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="245bf-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="245bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="245bf-102">SYNOPSIS</span></span>
<span data-ttu-id="245bf-103">Ellenőrzi a tárolási fiók nevének elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="245bf-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="245bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="245bf-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="245bf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="245bf-105">DESCRIPTION</span></span>
<span data-ttu-id="245bf-106">A **Get-AzStorageAccountNameAvailability** parancsmag ellenőrzi, hogy érvényes-e az Azure-tárterület-fiók neve, és használható-e.</span><span class="sxs-lookup"><span data-stu-id="245bf-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="245bf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="245bf-107">EXAMPLES</span></span>

### <span data-ttu-id="245bf-108">1. példa: a tárterület-fióknév elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="245bf-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="245bf-109">Ez a parancs ellenőrzi a ContosoStorage03 név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="245bf-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="245bf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="245bf-110">PARAMETERS</span></span>

### <span data-ttu-id="245bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="245bf-111">-DefaultProfile</span></span>
<span data-ttu-id="245bf-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="245bf-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="245bf-113">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="245bf-113">-Name</span></span>
<span data-ttu-id="245bf-114">A parancsmag által ellenőrzött tárolási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="245bf-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="245bf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245bf-115">CommonParameters</span></span>
<span data-ttu-id="245bf-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="245bf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245bf-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="245bf-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245bf-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="245bf-118">INPUTS</span></span>

### <span data-ttu-id="245bf-119">System. String</span><span class="sxs-lookup"><span data-stu-id="245bf-119">System.String</span></span>

## <span data-ttu-id="245bf-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="245bf-120">OUTPUTS</span></span>

### <span data-ttu-id="245bf-121">Microsoft. Azure. Management. Storage. models. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="245bf-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="245bf-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="245bf-122">NOTES</span></span>

## <span data-ttu-id="245bf-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="245bf-123">RELATED LINKS</span></span>

[<span data-ttu-id="245bf-124">Azure Storage Manager-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="245bf-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


