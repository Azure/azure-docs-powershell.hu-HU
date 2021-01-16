---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 3d1fd5fb49b90a7d1a149cf83e8ee19c9eed5272
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349554"
---
# <span data-ttu-id="98f7e-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="98f7e-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="98f7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="98f7e-103">Az aktuális előfizetés tárterületerőforrás-használatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="98f7e-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="98f7e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="98f7e-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98f7e-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="98f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="98f7e-106">A **Get-AzStorageUsage** parancsmag az aktuális előfizetéshez az Azure Storage-tárterület erőforrás-használatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="98f7e-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="98f7e-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="98f7e-107">EXAMPLES</span></span>

### <span data-ttu-id="98f7e-108">1. példa: A tárterület erőforrásainak kihasználtsága a megadott helyen</span><span class="sxs-lookup"><span data-stu-id="98f7e-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="98f7e-109">Ez a parancs az aktuális előfizetésben megadott hely tárterület-erőforrásainak használatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="98f7e-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="98f7e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98f7e-110">PARAMETERS</span></span>

### <span data-ttu-id="98f7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f7e-111">-DefaultProfile</span></span>
<span data-ttu-id="98f7e-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="98f7e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98f7e-113">-Location</span><span class="sxs-lookup"><span data-stu-id="98f7e-113">-Location</span></span>
<span data-ttu-id="98f7e-114">Azt jelzi, hogy tárterület-erőforrásokat kell-e használatba kapni a megadott helyen.</span><span class="sxs-lookup"><span data-stu-id="98f7e-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="98f7e-115">Ha nincs megadva, akkor a tárterület-erőforrásokat az előfizetés minden helyről használatba fogja kapni.</span><span class="sxs-lookup"><span data-stu-id="98f7e-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98f7e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f7e-116">CommonParameters</span></span>
<span data-ttu-id="98f7e-117">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98f7e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f7e-118">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f7e-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f7e-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98f7e-119">INPUTS</span></span>

### <span data-ttu-id="98f7e-120">System.String</span><span class="sxs-lookup"><span data-stu-id="98f7e-120">System.String</span></span>

## <span data-ttu-id="98f7e-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="98f7e-121">OUTPUTS</span></span>

### <span data-ttu-id="98f7e-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="98f7e-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="98f7e-123">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="98f7e-123">NOTES</span></span>

## <span data-ttu-id="98f7e-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="98f7e-124">RELATED LINKS</span></span>

[<span data-ttu-id="98f7e-125">Azure Storage Manager-parancsmagok</span><span class="sxs-lookup"><span data-stu-id="98f7e-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


