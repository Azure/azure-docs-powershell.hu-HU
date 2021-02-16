---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: c0b283c7645426af9397fd675fde825ff0b5f087
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168563"
---
# <span data-ttu-id="9f20e-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9f20e-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="9f20e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f20e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f20e-103">Egy tárfiók nevének elérhetőségét ellenőrzi.</span><span class="sxs-lookup"><span data-stu-id="9f20e-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="9f20e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="9f20e-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f20e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="9f20e-105">DESCRIPTION</span></span>
<span data-ttu-id="9f20e-106">A **Get-AzStorageAccountNameAvailability** parancsmag ellenőrzi, hogy egy Azure Storage-fiók neve érvényes és használható-e.</span><span class="sxs-lookup"><span data-stu-id="9f20e-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="9f20e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="9f20e-107">EXAMPLES</span></span>

### <span data-ttu-id="9f20e-108">1. példa: Tárfiók nevének elérhetőségének ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="9f20e-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="9f20e-109">Ez a parancs ellenőrzi a ContosoStorage03 név elérhetőségét.</span><span class="sxs-lookup"><span data-stu-id="9f20e-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="9f20e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f20e-110">PARAMETERS</span></span>

### <span data-ttu-id="9f20e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f20e-111">-DefaultProfile</span></span>
<span data-ttu-id="9f20e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9f20e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f20e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9f20e-113">-Name</span></span>
<span data-ttu-id="9f20e-114">Annak a tárfióknak a nevét adja meg, amelybe ez a parancsmag ellenőriz.</span><span class="sxs-lookup"><span data-stu-id="9f20e-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="9f20e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f20e-115">CommonParameters</span></span>
<span data-ttu-id="9f20e-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f20e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f20e-117">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f20e-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f20e-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f20e-118">INPUTS</span></span>

### <span data-ttu-id="9f20e-119">System.String</span><span class="sxs-lookup"><span data-stu-id="9f20e-119">System.String</span></span>

## <span data-ttu-id="9f20e-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9f20e-120">OUTPUTS</span></span>

### <span data-ttu-id="9f20e-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="9f20e-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="9f20e-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="9f20e-122">NOTES</span></span>

## <span data-ttu-id="9f20e-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9f20e-123">RELATED LINKS</span></span>

[<span data-ttu-id="9f20e-124">Azure Storage Manager-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="9f20e-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


